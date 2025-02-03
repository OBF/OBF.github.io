---
author: pjotrp
category:
  - bioruby
  - google-summer-of-code
  - obf
date: "2015-04-01T15:21:30+00:00"
guid: http://news.open-bio.org/news/?p=1293
tag:
  - development
  - gsoc
title: GSoC project Sambamba published in scientific journal
url: /2015/04/01/gsoc-project-sambamba-published-in-scientific-journal/

---
_(This is a repost of a BLOG on Google Open Source news about Google's open source student programs and software releases)_

One of our goals with GSoC is to inspire young developers to participate in open source development, hopefully continuing well beyond the summer. Pjotr Prins from the Open Bioinformatics Foundation shared this story with us about a GSoC 2012 student who has continued leading the development of a software tool used in laboratories around the world. That tool, Sambamba, was recently featured in an Oxford University Press scientific journal.
The Open Bioinformatics Foundation (OBF) participated in Google Summer of Code (GSoC) in 2012 and again in 2014. One of our projects,Sambamba, enables users to rapidly process large sequence alignment files in the SAM, BAM and CRAM formats using parallel processing. Sambamba, which means “parallel” in Swahili, was recently the subject of a paper published in Bioinformatics Journal by GSoC alumnus Artem Tarasov. Since the tool is now used in DNA sequencing centres around the world, Artem has become well known in the bioinformatics community as Sambamba’s creator.

When we participated in GSoC 2012, we accepted five students, one of whom was Artem. His project was to “write the fastest parallelized BAM parser in D” as an alternative to the existing SAMtools software written in single-threaded C. I consider the D language to be particularly well-suited to bioinformatics given its modern hybrid OOP/functional syntax with close-to-the-metal performance optimizations.

Even before GSoC started that year, Artem was doing research and cranking out code. In his blog, he wrote about learning the D language, dealing with parallel executing code, and the sometimes-buggy compiler and garbage collector. The file formats he was working with are complicated and contain many assumptions, but he made wise choices which led to a very effective piece of software: people tend to rave about Sambamba when they use it the first time. Artem and I continued working on Sambamba after GSoC and before long, I found that he was the one mentoring me!

Since then, Artem has been invited to visit the Cuppen sequencing lab in the Netherlands where he added depth analysis to Sambamba. This is also when we started work on the manuscript for the Bioinformatics Journal. Later, the OBF was able to sponsor a second trip to the European Bioinformatics Institute in Cambridge, UK where he and I took part in a Codefest and met with other bioinformatics researchers and developers, including some OBF contributors.

Artem isn’t our only GSoC student who has continued making a difference in open source. Four of our five GSoC 2012 students are still active FOSS committers on GitHub, with three of them continuing in the bioinformatics space. Although GSoC can be competitive and we haven’t been accepted into the program every year, we’re grateful for the opportunities it has given us. Organizations like OBF and SciRuby are proof that GSoC and scientific projects work really well together. Without GSoC, Artem and I would probably not have ever met. He and I both hope to introduce more students to scientific open source projects in the future.
By Pjotr Prins, Sambamba GSoC Mentor
