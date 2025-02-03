---
author: peterc
category:
  - blogroll
  - code
  - community
  - development
  - google-summer-of-code
  - travel-fellowship
date: "2017-04-05T19:01:00+00:00"
guid: https://news.open-bio.org/?p=1585
summary: _This is a guest blog post from Anton Khodak, who was supported by the ongoing [Open Bioinformatics Foundation travel fellowship program](https://github.com/OBF/obf-docs/blob/master/Travel_fellowships.md) to attend a week long [Common Workflow Language (CWL)](http://www.commonwl.org/) workshop in London, November 2016. This was a natural continuation of Anton's work on [porting tools to the CWL](https://anton-khodak.github.io/argparse2cwl-blog/2016/08/11/gentle-introduction.html) as one of the [OBF's Google Summer of Code 2016 students](/2016/04/25/welcome-gsoc-2016-students/)._ _The OBF's Travel Fellowship program continues to help open source bioinformatics software developers with funding to attend conferences or workshops. The current call closes 15 April 2017 - if you're planning to attend the OBF's annual [Bioinformatics Open Source Conference (BOSC) 2017 in Prague](https://www.open-bio.org/wiki/BOSC_2017), you might want to apply?_
tag:
  - codefest
  - community
  - development
  - gsoc
  - travel-fellowship
title: OBF Travel Fellowship - CWL week in London
url: /2017/04/05/obf-travel-fellowship-anton-khodak/

---
_This is a guest blog post from Anton Khodak, who was supported by the ongoing [Open Bioinformatics Foundation travel fellowship program](https://github.com/OBF/obf-docs/blob/master/Travel_fellowships.md) to attend a week long [Common Workflow Language (CWL)](http://www.commonwl.org/) workshop in London, November 2016. This was a natural continuation of Anton's work on [porting tools to the CWL](https://anton-khodak.github.io/argparse2cwl-blog/2016/08/11/gentle-introduction.html) as one of the [OBF's Google Summer of Code 2016 students](/2016/04/25/welcome-gsoc-2016-students/)._ _The OBF's Travel Fellowship program continues to help open source bioinformatics software developers with funding to attend conferences or workshops. The current call closes 15 April 2017 - if you're planning to attend the OBF's annual [Bioinformatics Open Source Conference (BOSC) 2017 in Prague](/wiki/BOSC_2017), you might want to apply?_

# CWL week in London

( [Originally published Mar 17, 2017](https://anton-khodak.github.io/argparse2cwl-blog/2017/03/17/cwl-hackathon.html))

After the successful completion of my GSoC projects, I had been invited to meet my mentors [Michael R. Crusoe](https://orcid.org/0000-0002-2961-9670) and [Roman Valls Guimera](https://se.linkedin.com/in/romanvg) for the CWL work session that took place in London from the 1st to the 4th of November, 2016. I was thrilled by this opportunity, and though it took quite a while for me to organize this journey (my first solo voyage abroad), it was undoubtfully worth it.

I arrived in London a little earlier to take part in [Mozilla Festival 2016](https://mozillafestival.org/) together with Roman. At the festival, I presented my summer projects to people from the bioinformatics community who participated in Mozfest’s [Open Science Fair](https://app.mozillafestival.org/#_space-open-science).

The CWL week started a day later. The attendees were Michael (Common Workflow Language project), Roman (the Wolfson Wohl Cancer Research Centre), [Janko Simonovic](https://rs.linkedin.com/in/jsimonovic) and [Ivan Batic](https://rs.linkedin.com/in/ivanbatic) from Seven Bridges Genomics, [Niels Drost](https://orcid.org/0000-0001-9795-7981) from the Netherlands eScience Center, [Robert Sugar](https://uk.linkedin.com/in/robert-sugar-90b8b941) from Intel Health and Life Sciences, and myself. During these four days, I worked on polishing the tools I developed ( [argparse2tool](https://github.com/erasche/argparse2tool), [pypi2cwl](https://github.com/common-workflow-language/pypi2cwl), [cwl2argparse](https://github.com/common-workflow-language/cwl2argparse)) on the basis of the feedback from all the participants. We explored the question of pip installability, filed a bunch of [issues](https://github.com/common-workflow-language/gxargparse/issues?utf8=%E2%9C%93&q=%20is%3Aissue%20), tried applying argparse2tool to [khmer](https://github.com/dib-lab/khmer) scripts. Another thing we tackled was bug fixes for running [Toil](https://github.com/BD2KGenomics/toil) workflow engine on SLURM cluster. In addition, I learned about the inner workings of another important open-source implementation for CWL [bunny](https://github.com/rabix/bunny) directly from its creator Janko. During the CWL week, it was added to the community run continuous integration server and successfully [passed](https://twitter.com/commonwl/status/793767714049384448) the latest conformance tests.

Overall, it was a highly intensive and productive hackathon. I was very happy to meet my mentors and other people from the CWL community in person and to work with them for these few days. I could not imagine a better finish of my Google Summer of Code 2016 participation!

{{< figure align=alignnone width=978 src="https://news.open-bio.org/wp-content/uploads/2017/04/london%5Fcwl.jpg" alt="" >}}

P.S. A year after, I became a mentor on a CWL project myself! Check the idea here: [CWL reference implementation](https://obf.github.io/GSoC/ideas/#cwl-reference-implementation-cwltool).

P.P.S. Special thanks to [Open Bioinformatics Foundation](/) for awarding me with the travel fellowship and reimbursing with that a significant part of my travel expenses.

_(Above post contributed by Anton Khodak, [originally on his blog](https://anton-khodak.github.io/argparse2cwl-blog/2017/03/17/cwl-hackathon.html), with our introduction added.)_
