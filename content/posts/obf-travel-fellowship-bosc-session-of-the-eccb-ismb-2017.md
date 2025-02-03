---
author: cjfields
category:
  - blogroll
  - bosc/ismb
  - community
  - travel-fellowship
date: "2017-08-28T14:43:53+00:00"
guid: https://news.open-bio.org/?p=1746
summary: _This blog post is syndicated from a [post on Jonathan Sobel's blog](https://jonathansobel1.wordpress.com/2017/07/27/bosc-session-of-the-eccbismb-2017/), originally published July 27, 2017. Jonathan was supported by the ongoing [OBF travel fellowship program](https://github.com/OBF/obf-docs/blob/master/Travel_fellowships.md) to attend the 2017 Bioinformatics Open Source Conference (BOSC), held as part of the 2017 ISMB/ECCB meeting in Prague, Czech Republic, in July 2017._ _The OBF's Travel Fellowship program continues to help open source bioinformatics software developers with funding to attend conferences, workshops, or training events. The next call closes 15 December 2017._
tag:
  - bosc
  - bosc/ismb
  - community
  - travel-fellowship
title: OBF Travel Fellowship - BOSC session of the ECCB/ISMB 2017
url: /2017/08/28/obf-travel-fellowship-jonathan-sobel/

---
_This blog post is syndicated from a [post on Jonathan Sobel's blog](https://jonathansobel1.wordpress.com/2017/07/27/bosc-session-of-the-eccbismb-2017/), originally published July 27, 2017. Jonathan was supported by the ongoing [OBF travel fellowship program](https://github.com/OBF/obf-docs/blob/master/Travel_fellowships.md) to attend the 2017 Bioinformatics Open Source Conference (BOSC), held as part of the 2017 ISMB/ECCB meeting in Prague, Czech Republic, in July 2017._ _The OBF's Travel Fellowship program continues to help open source bioinformatics software developers with funding to attend conferences, workshops, or training events. The next call closes 15 December 2017._

As the lucky recipient of an [Open Bioinformatics Foundation (OBF)](/wiki/Main_Page) travel grant, I had the chance to attend to my first [Bio-informatics Open Source Conference (BOSC)](/wiki/BOSC_2017) in Prague the 21 and 22 July 2017.

![Pear](https://jonathansobel1.files.wordpress.com/2017/07/pear.png?w=164&h=117)

During the event, I discovered an amazing community of scientists and developers involved in the field of bioinformatics, with a strong open source mindset. “Sharing is caring” and I can tell these guys care a lot! The first day was quite technical with several talks about projects developed during the [code fest](/wiki/Codefest_2017) that happen just prior to the conference. I had the opportunity to discover the [FAIR principles](https://www.nature.com/articles/sdata201618) (Findability, Accessibility, Interoperability, and Reproducibility) of open data, and several tools aimed at simplifying bioinformatics workflow sharing, visualizing and production. These teams triggered my curiosity towards the [Common Workflow Language](http://www.commonwl.org/draft-3/UserGuide.html) (CWL) and data standards, notably [RABIX](http://rabix.io/), [GA4GH](http://ga4gh.org/#/) and [nextflow](https://www.nextflow.io/index.html). Several talks presented very useful tools such as [YAMP](https://github.com/alesssia/YAMP) (Yet Another Metagenomic Pipline!) or [MiltiQC](http://multiqc.info/) for next generation sequencing quality control, and [Open MS 2.0](https://www.openms.de/) for mass-spectrometry data analysis. One important topic of the day was the reproducibility of bioinformatics piplines and several talks were addressing this question with various approaches, such as containers (Dockers, [BioContainers](https://biocontainers.pro/)), [GNU Guix](https://www.gnu.org/software/guix/) or package repository such as [BioConda](https://bioconda.github.io/).

![logo](https://jonathansobel1.files.wordpress.com/2017/07/logo.png?w=339&h=168)

On the second day, I had the chance to present our [BeerDeCoded](http://www.genome.beer/) project in the Citizen Science session of the BOSC. I had the first slot in the morning with an audience of nearly 250 attendees. The beer topic is kind of holy in a geek environment. I had the pleasure to share several important message regarding science conducted outside of academia or industry, in a community laboratory space like [Hackuarium](http://www.hackuarium.ch/en/). I put some emphasis about science communication between fields and outside of our institutional scientific community. As experts, we have the responsibility to make our knowledge and our researches accessible to a wide audience, and this is exactly our goal with BeerDeCoded and Hackuarium. In addition, I could announce [the official release](https://github.com/beerdecoded/Beer_ITS_analysis) of our first results based on the metagenomic analysis of [39 beer samples](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA388541/). I was able to show our preliminary analysis. The BOSC community was really enthusiastic about the project and attendees tweeted quite a lot about it.

> Some background material for [@JonathanSobel1](https://twitter.com/JonathanSobel1)'s "BeerDeCoded" talk at [#BOSC2017](https://twitter.com/hashtag/BOSC2017?src=hash)![🍺](https://s0.wp.com/wp-content/mu-plugins/wpcom-smileys/twemoji/2/72x72/1f37a.png) [pic.twitter.com/O52PI6k1hT](https://t.co/O52PI6k1hT)
>
> — Madeleine Price Ball (@madprime) [July 23, 2017](https://twitter.com/madprime/status/889038522836975616)

> The scientific method reloaded: Analyse data, think, drink, repeat. [#BOSC2017](https://twitter.com/hashtag/BOSC2017?src=hash) [pic.twitter.com/JY0sLuXtzw](https://t.co/JY0sLuXtzw)
>
> — Bastian Greshake (@gedankenstuecke) [July 23, 2017](https://twitter.com/gedankenstuecke/status/889038120691392513)

> Work in progress for [@beerdecoded](https://twitter.com/beerdecoded) – really really want [@nanopore](https://twitter.com/nanopore) (so do we!) [#BOSC2017](https://twitter.com/hashtag/BOSC2017?src=hash) [#ISMBECCB](https://twitter.com/hashtag/ISMBECCB?src=hash) [pic.twitter.com/FplOglIpb0](https://t.co/FplOglIpb0)
>
> — BauhiniaGenome (@BauhiniaGenome) [July 23, 2017](https://twitter.com/BauhiniaGenome/status/889039041215303680)

In addition, I had some very interesting questions about the interest of breweries in BeerDeCoded, the potential fear of companies that citizen scientist decode their proprietary yeast strain or about the data integration of sequencing with GC/MS in order to study small molecules present in our beer data-set. Moreover, this talk will potentially trigger new collaborations with with Bérénice Batut from the [Galaxy training network](https://galaxyproject.org/teach/gtn/).  [Galaxy](https://usegalaxy.org/) is an open source, web-based platform for data intensive biomedical research. The Galaxy platform regroups a collection of bioinformatics tools and workflow that can be run without coding knowledge. This program is widely used by biologists to analyze their next generation sequencing data. BeerDeCoded will benefit from this collaboration with a specific instance of Galaxy to make the beer metagenomics accessible to anyone.

Later during this second day, I was impressed by several other talks. One of the greatest initiative is the work of the [H3ABioNet](http://www.h3abionet.org/), which aim at training bioinformaticians in Africa. I discovered the [Journal of open source software](http://joss.theoj.org/about) (JOSS) that facilitate the publication of bioinformatics software. Then, [BioThings](http://biothings.io/#) SDK and [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) presented their API and their knowledge base that allows retrieving efficiently some annotations of biological data. This day was as well the occasion to discuss about data sharing of human data (wearable, clinical, etc.) in order to improve precision medicine and the ethical implication. In addition, second-hand data usage and the problem of re-digitalization of published data in a non-machine readable format was evoked. Finally, Nick Loman gave the closing keynote presentation at BOSC. He gave a great talk about virus outburst surveillance using the Oxford nanopore minION sequencing technology, using two examples, namely Ebola outburst in Africa in 2015 and the Zika virus in Brazil.

In summary my first BOSC experience was very intense and highly interesting. I met with great scientists and developers and I learned about the newest open source software/library/API and practices in this field. I would like to thank once again the BOF committee for allowing me to join this great event and to give me the opportunity to present Hackuarium and the BeerDeCoded project.

> [#bosc2017](https://twitter.com/hashtag/bosc2017?src=hash) cheers! Thanks for this great conference [pic.twitter.com/m6oO8Wbbky](https://t.co/m6oO8Wbbky)
>
> — Jonathan Sobel (@JonathanSobel1) [July 23, 2017](https://twitter.com/JonathanSobel1/status/889229547102666752)

[![](http://feeds.wordpress.com/1.0/comments/jonathansobel1.wordpress.com/73/)](http://feeds.wordpress.com/1.0/gocomments/jonathansobel1.wordpress.com/73/)
