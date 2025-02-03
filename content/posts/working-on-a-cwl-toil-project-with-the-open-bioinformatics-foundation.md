---
author: yo
category:
  - google-summer-of-code
date: "2021-06-23T08:58:43+00:00"
guid: https://www.open-bio.org/?p=5711
tag:
  - cwl
  - gsoc
  - gsoc-2021
title: Working on a CWL-Toil project with the Open Bioinformatics Foundation
url: /2021/06/23/working-on-a-cwl-toil-project-with-the-open-bioinformatics-foundation/

---
_This is a guest post from Mihai Popescu, a GSoC student with CWL, which participates under the OBF umbrella. Cross-posted on the CWL forums: [https://cwl.discourse.group/t/working-on-a-cwl-toil-project-with-the-open-bioinformatics-foundation/390](https://cwl.discourse.group/t/working-on-a-cwl-toil-project-with-the-open-bioinformatics-foundation/390)_

I am Mihai Popescu, a second year master student at VU Amsterdam in [Parallel and Distributed Computer Systems](https://vuweb.vu.nl/en/education/master/parallel-and-distributed-computer-systems). I am happy that my GSoC proposal got accepted and that I have started working on the project. I attended some CWL meetings since I submitted the proposal and I got to know a small part of the community. I would like to thank my mentor Michael for introducing me to the CWL community and answering a lot of my questions about workflows.

The objective of my [2021 GSoC project](https://summerofcode.withgoogle.com/projects/#6469533377757184) is to implement data streaming for `toil-cwl-runner`, which is a way of running Toil using CWL. This project aims to implement data streaming to speed up the analysis by avoiding slow disk/storage IO and speeding up the start of tool execution when it isn’t required to wait for data to download. The main focus is to implement this first in AWS S3. [Toil](https://toil.readthedocs.io/en/latest/) is an open-source pure-Python workflow engine. [Common Workflow Language](https://www.commonwl.org/) (CWL) is an open standard for describing analysis workflows.

Sarah Wait Zaranek from [Arvados](https://arvados.org/) helped me get a real world CWL [workflow 1](https://github.com/arvados/arvados-tutorial/tree/main/WGS-processing) that uses streaming. It took a while to get used to the Arvados platform and I actually ran a much bigger workflow than intended on their “playground” public instance. I ended up using a single step from the workflow to keep it simple at the start and be able to run it locally on my computer. I’ve splitted it up into two individual components ( [first 1](https://github.com/mhpopescu/toil-gsoc-tests/blob/2561e007167834ca777de8e2f2a7e03fb65aab2f/bwamem.cwl) and [second](https://github.com/mhpopescu/toil-gsoc-tests/blob/2561e007167834ca777de8e2f2a7e03fb65aab2f/samtools-view.cwl)) so that I could test the streaming feature.

There are 2 runners in Toil: pure python `toil` and `toil-cwl-runner`. The `toil` runner has functionality for file streaming. The proposed solution to enable file streaming for `toil-cwl-runner` is to make use of named pipes. I tested to see if this would work by simulating the behavior. I started with a simple [example](https://github.com/mhpopescu/toil-gsoc-tests/blob/2561e007167834ca777de8e2f2a7e03fb65aab2f/fifo-cat.py) doing a `cat` command without toil, where the input file would be streamed using a named pipe. [Then](https://github.com/mhpopescu/toil-gsoc-tests/blob/2561e007167834ca777de8e2f2a7e03fb65aab2f/fifo-sam.py) I streamed the input for the samtools step that was in the splitted workflow. Then I streamed the input and the output for the same step, running a python toil [workflow](https://github.com/mhpopescu/toil-gsoc-tests/blob/2561e007167834ca777de8e2f2a7e03fb65aab2f/samtools-view-fifo-out.py).

Streaming the output looks similar to this:

```
def writeOutputToPipe(self, fin, foutStream, fileStore):
    with open(fin, 'rb') as fi:
        while True:
            data = fi.read()
            if not data:
                break
            foutStream.write(data)

```

And before running the job, another thread would start to run this function. Streaming the input is similar.

Now that I tested that using named pipes could help streaming the files, I would look at how to implement this in the source of `toil-cwl-runner` itself: `cwltoil.py`. There are a few steps for what to do next:

- Investigate the block of code that parses the CWL file
- Check if `streamable` option is set and then maybe create a new flag in internal `toil` file structures
- Investigate the block of code that downloads the file
- Add the streaming functionality when `streamable` option is set
