---
author: akeshavan
category:
  - blogroll
  - community
  - travel-fellowship
date: "2018-05-22T12:54:41+00:00"
guid: https://news.open-bio.org/?p=1946
summary: '_This is a guest blog post from [Anisha Keshavan](https://github.com/akeshavan), who was supported by the ongoing [Open Bioinformatics Foundation travel fellowship](https://github.com/OBF/obf-docs/blob/master/Travel_fellowships.md) program to attend the [2018 eLife Innovation Sprint](https://elifesciences.org/events/c40798c3/elife-innovation-sprint-2018) in Cambridge, May 2018. The OBF''s Travel Fellowship program continues to help open source bioinformatics software developers with funding to attend conferences or workshops. This was one of [three awards from our April 2018 travel fellowships call](https://news.open-bio.org/2018/05/25/travel-fellowships-april-2018/). The current call closes 15 August 2018, you might want to apply?_ It is hard for me to put into words the thrill, excitement, and inspiration I’m feeling after attending the 2 day eLife Innovation sprint on May 10th and 11th. The _**#eLifeSprint**_ ( [https://elifesciences.org/events/c40798c3/elife-innovation-sprint-2018](https://elifesciences.org/events/c40798c3/elife-innovation-sprint-2018)) in Cambridge, UK, brought together software developers, researchers, designers, and anyone who was passionate about leveraging web technology to advance open scientific communication. The goal: to save science from itself!'
tag:
  - code
  - community
  - conferences
  - travel-fellowship
title: 'Saving science from itself: A review of the 2018 eLife Innovation Sprint'
url: /2018/05/22/saving-science-from-itself-2018-elife-innovation-sprint/

---
_This is a guest blog post from [Anisha Keshavan](https://github.com/akeshavan), who was supported by the ongoing [Open Bioinformatics Foundation travel fellowship](https://github.com/OBF/obf-docs/blob/master/Travel_fellowships.md) program to attend the [2018 eLife Innovation Sprint](https://elifesciences.org/events/c40798c3/elife-innovation-sprint-2018) in Cambridge, May 2018. The OBF's Travel Fellowship program continues to help open source bioinformatics software developers with funding to attend conferences or workshops. This was one of [three awards from our April 2018 travel fellowships call](https://news.open-bio.org/2018/05/25/travel-fellowships-april-2018/). The current call closes 15 August 2018, you might want to apply?_ It is hard for me to put into words the thrill, excitement, and inspiration I’m feeling after attending the 2 day eLife Innovation sprint on May 10th and 11th. The _**#eLifeSprint**_ ( [https://elifesciences.org/events/c40798c3/elife-innovation-sprint-2018](https://elifesciences.org/events/c40798c3/elife-innovation-sprint-2018)) in Cambridge, UK, brought together software developers, researchers, designers, and anyone who was passionate about leveraging web technology to advance open scientific communication. The goal: to save science from itself!

What do I even mean by this? Well, let me explain how the process unfolds:

1. Get some background knowledge on your topic of interest, read a bunch of publications and about all the experiments and theories up to this point in time **_#readallthepubs_**
1. Think of a new scientific hypothesis or theory, design an experiment to test it
1. Write up _exactly_ what you did in your experiment, the results, and your interpretation **_#reproduceit_**
1. Show your write up to your peers and have them review it -- it’s their job to make sure what you did was legit, and that your results and  interpretation makes sense **_#sanitycheck_**
1. Share it with the scientific community and world, which adds to the growing pile of theories/evidence/background in 1. _**#sharetheknowledge**_

Sounds great. Why do we need to save science from itself?

_**#readallthepubs**_: Turns out, scientists are publishing SO MUCH that its nearly impossible to read and comprehend all the scientific literature out on the web. This is also called research debt (and here's a great article: [https://distill.pub/2017/research-debt/](https://distill.pub/2017/research-debt/) )

_**#reproduceit**_: You'd think computers would have made our lives easier because we can  automate data analyses, but actually reproducing an analysis is really difficult. Describing what the analysis code does in the methods section of a paper just doesn't cut it. And if another scientist can't reproduce an experiment, can we trust the original experiment's outcome?

**_#sanitycheck_**: Reviewing a paper well is a lot of work! Peer reviewers do this for free and anonymously, which sucks because they never get recognized for the work they put in. Understandably, its not a high priority to review papers in a timely manner, and this means that important research findings don't get published for a long time._**#sharetheknowledge**_: Now that a scientist has read all the background on their topic of interest, designed and ran a reproducible experiment, and revised their manuscript based on peer review, they submit their article to a journal so that other scientists all over the world can read it. Usually, they _pay_ the journal to publish their paper, and then other scientists also _pay_ the journal to read the paper (Yes, these journals make BANK $$$). If you and your institution can't pay all the fees, that's a bummer. In fact, its a bummer for all of science! Progress is majorly hindered when bright, intelligent scientists with something to contribute to a field don't have access to vital information because they can't pay publishers. For example, [a Liberian physician doesn't have access to Ebola research articles because each article costs half a weeks salary](https://www.nytimes.com/2015/04/08/opinion/yes-we-were-warned-about-ebola.html?_r=0). Information needs to be open to everyone, regardless of how much money you have.

Ok, so clearly science needs a major course correction. Enter: the 2018 eLife innovation sprint! In the following sections I'll list the project prototypes and links from the sprint that aim to correct one or more of the the four topics above.

## \#readallthepubs

 [https://appstract.pub](https://appstract.pub) :My team! We built a citizen science game to collect annotations on publications, so that we can run meta-analyses to summarize a large set of publications. You can compete with friends on the leaderboard, win badges, and contribute to science!![team appstract!](https://pbs.twimg.com/media/Dc7Gw6PWsAA7AQk.jpg)[WikiCiteViz](https://github.com/Samwalton9/WikiCiteVis):  A project to visualize citations, so you can see how a study has influenced other studies in the field.[Zotero Insights](https://github.com/Bubblbu/zotero-insights):  When you read papers, you can take notes in Zotero on a PDF. This project extracts all your notes (or annotations) and puts it into a machine-readable format, and creates reports and analyses of your notes![Citation Gecko](http://citationgecko.com/): a way to find more relevant papers to read using citation data, and finds papers you may have missed.[Abstract Babel](https://github.com/nlisgo/abstract-babel): what it sounds like! Translate abstracts to different languages . I don't speak any other languages, but they say the translations are solid!

[Funda](https://docs.google.com/presentation/d/1dM_HWimJ0SIfl9D3clhqKpxq04sLCVKOoNcxiHw0Myw/edit#slide=id.p): a project [roadmap](https://docs.google.com/document/d/1R8AdItJ6cVivrCm6zWuMykz_rrCoj_o7vSMzNUQ6F7E/edit) for teaching web literacy in South Africa.

## \#reproduceit

New technology has made our science experiments a little more complicated. We’re collecting a ton of data, and we write a lot of custom programs to crunch the numbers and make inferences. It turns out that sometimes what works on your computer won’t work on someone else’s! It can take a lot of CS skills to get the same analysis running on your computer, and that really slows us down. The following tools can help address this:[Reproducible computational research](https://github.com/popperized/open-comp-rsc-popper):a case study that shows reproducible computational neuroscience research using [Popper](http://falsifiable.us/) and [Sumatra](https://pythonhosted.org/Sumatra/) .[Project Trackbook](https://github.com/dat-land/project-trackbook):an open lab notebook that "gives researchers an interface to securely share and version control files in a _decentralized_ network".[Jupyter + Stencila](https://github.com/minrk/jupyter-dar/): combines some great tools: the [Stencila editor](http://stenci.la/), the [Jupyter notebook](http://jupyter.org/), and [mybinder](https://mybinder.org/), to create "interactive, reproducible, and transparent" scientific articles!

## \#sanitycheck

[Project Octopus](https://octopus-hypothesis.netlify.com/): This was probably the biggest group at the sprint, and covers both the _#sanitycheck_ and _#sharetheknowledge_. On the octopus platform, you'll be able to review other scientist's work, and get credit for doing so! You should also checkout the blog on their website, which does [a great job explaining in depth the problems we face in science, and how octopus can help](https://octopus-hypothesis.netlify.com/blog/2018/05/13/2018-05-13_fixingscience/).[PREreview](https://github.com/SamanthaHindle/preprint_JournalClub): " _Putting the ‘peer’ back into peer review!"_ Many scientists have started to upload their manuscripts to preprint servers, so that scientists can access the information before the lengthy peer-review and publication process. And this is really great for authors! For example, [here](https://arxiv.org/pdf/1805.05238.pdf) is a preprint on how preprints that are posted before conference submission garner more citations than those posted after. PREreview is a platform for the "collaborative writing of preprint reviews" :) I found a very useful blog post on their site on [guidelines for writing a preprint review](https://prereview.org/users/164141/articles/200820-prereview-guidelines-how-to-write-a-preprint-review).

## \#sharetheknowledge

[Project Octopus](https://octopus-hypothesis.netlify.com/): On the octopus platform, all published work will be open to everython, and as a scientist, you'll be able to "publish your hypotheses, methods, results and analyses in Octopus as you produce them, in whatever language you are most comfortable in".[Plaudit](http://sarabosshart.wixsite.com/plauditpub): It would be great if the value of the paper was not dependent on journal status, but instead on the quality of the work! Plaudit lets you publicly endorse an article, so that scientists don't have to worry about whether your article is published in a name brand journal, and it incentivizes open publishing and publishing preprints.

## Conclusions

Sometimes I feel really pessimistic about science, because of how inefficient and unfair it can be. But all the amazing participants at the eLifeSprint showed me that 1) SO many people care about these issues, 2) people have brilliant ideas and prototypes to address these issues, and 3) how many tools already exist, that I just didn't know about until I attended the sprint (I was excited to learn about the amazing [openaccessbutton.org](https://openaccessbutton.org) API). Overall I left feeling very optimistic about the future of science! Thanks to Naomi Penfold and eLife for organizing this amazing event, and especially, [thanks to OBF for the travel award](https://news.open-bio.org/2018/05/25/travel-fellowships-april-2018/) so that I could attend!
