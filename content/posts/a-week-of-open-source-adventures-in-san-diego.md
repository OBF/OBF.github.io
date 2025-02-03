---
author: lindsayrutter
category:
  - community
  - development
  - obf
  - travel-fellowship
cover:
  alt: hackers-meeting-lindsay - 1
  image: /wp-content/uploads/2019/03/hackers-meeting-lindsay-1.jpg
date: "2019-03-13T11:19:53+00:00"
guid: https://news.open-bio.org/?p=2167
tag:
  - travel-fellowship
title: A week of open source adventures in San Diego
url: /2019/03/13/a-week-of-open-source-adventures-in-san-diego/

---
_This is a guest blog post from Lindsay Rutter, who was supported by the ongoing [Open Bioinformatics Foundation travel fellowship program](https://github.com/OBF/obf-docs/blob/master/Travel_fellowships.md) to attend a [National Center for Biotechnology Information (NCBI) hackathon](https://ncbiinsights.ncbi.nlm.nih.gov/2018/11/09/ncbi-sdsu-virus-hunting-data-science-hackathon-january-2019/) and the [Plant and Animal Genome Conference (PAG)](https://www.intlpag.org/2019/). The OBF’s Travel Fellowship program continues to help open source bioinformatics software developers with funding to attend conferences or workshops. The current call closes on 15 April 2019. If you are hoping to attend an open source / open science bioinformatics even and travel costs are a barrier, we encourage you to apply for one of our $1000 travel fellowships._

I would like to thank the Open Bioinformatics Foundation (OBF) for promoting open source bioinformatics. Many people believe that transparency in science and software helps us procure the most we can out of increasingly large biological datasets. Your support allowed me to embark on a week-long "open source adventure" in San Diego, where I participated in a data science hackathon and introduced my new software package at a conference workshop.

I was up early the first morning for the same reason anyone would be when visiting sunny Southern California - to hunt for viruses computationally! It was great to participate in my third [National Center for Biotechnology Information (NCBI) hackathon](https://ncbiinsights.ncbi.nlm.nih.gov/2018/11/09/ncbi-sdsu-virus-hunting-data-science-hackathon-january-2019/). The three-day event was hosted by the Computational Sciences Research Center at San Diego State University and our mission was to develop virological indices using 141,000 metagenomic datasets from the [NCBI Sequence Read Archive (SRA)](https://www.ncbi.nlm.nih.gov/sra). Improving the usability of the sheer volumes of data publicly available on the NCBI SRA could potentially facilitate important public health analyses. Hackathon participants split into nine working groups to build a scientific pipeline for metadata processing and novel virus discovery in the cloud infrastructure. Data preparation teams filtered assembled contigs, supervised machine learning teams cleaned metadata, and phylogenetic association teams clustered any matches. Contigs that did not map to known viruses were sent to teams that mapped domains and open reading frames with virus gene families. Based on these results, certain contigs were then sent to "viral dark matter" teams that identified novel viral contigs.

\[caption id="attachment\_2181" align="aligncenter" width="640"\]![](https://news.open-bio.org/wp-content/uploads/2019/03/hackathon1-1024x768.jpg) Hackers meeting. (Image shared by [Joan Martí-Carreras](http://joanmarticarreras.com))\[/caption\]

\[caption id="attachment\_2183" align="aligncenter" width="640"\]![](https://news.open-bio.org/wp-content/uploads/2019/03/hackathon2-1024x768.jpg) Hackers at work (Image shared by [Ben Busby](https://twitter.com/DCGenomics))\[/caption\]

There is a lot of problem-solving in hackathons. A lot of divergent thinking. Some sinking or swimming. This particular hackathon was even more animated than usual because all forty participants were working toward the same end pipeline and teams needed to pitch new prototypes to other teams each time a problem was encountered. Hackathon participants ranged from unseasoned students to computational virology experts and travelled from around the world. In the "viral dark matter" team that I led, one teammate flew in from Australia and another teammate flew in from Columbia. Many of us have used version control platforms to _remotely_ collaborate with peers when writing code, but collaborating with people from different experience levels and backgrounds _all together in the same room_ is a unique environment that I believe fosters creativity.

\[caption id="attachment\_2184" align="aligncenter" width="640"\]![](https://news.open-bio.org/wp-content/uploads/2019/03/hackathonScribbles1-1024x768.jpg) Defining virus indices (Image shared by [Ben Busby](https://twitter.com/DCGenomics))\[/caption\]

In the end, we produced eight free software artifacts, which are available on [GitHub](https://github.com/NCBI-Hackathons/VirusDiscoveryProject). Annotations and associated metadata will also be freely available in a Jupyter notebook-driven API. Many participants believed the event provided evidence that hackathon settings can be effective for demonstration projects indexing large datasets. We celebrated our work each evening by enjoying delicious food at nearby restaurants. Dinner topics ranged from ancient viruses beneath Arctic ice to synthetic viruses to future virus-hunting hackathons. The daily time reserved for casual discussion with other hackers is a great attribute of NCBI hackathons.

\[caption id="attachment\_2185" align="aligncenter" width="640"\]![](https://news.open-bio.org/wp-content/uploads/2019/03/socialHackathon-1024x768.jpg) Hackers know how to have fun, even when separated from their computers! (Image shared by [Ben Busby](https://twitter.com/DCGenomics)).\[/caption\]

The [Plant and Animal Genome Conference (PAG)](https://www.intlpag.org/2019/) commenced the day after the hackathon ended. The conference encourages forum on recent developments and future plans for plant and animal genome projects, an internationally important topic. I was invited to give a talk during their annual workshop ["Big Data: Manage your data before your data kills you"](https://pag.confex.com/pag/xxvii/meetingapp.cgi/Session/5455). Indeed, big datasets can almost feel like numerical avalanches that we should run away from, but the workshop encouraged attendees to transcend such grim thinking and instead was motivated to spark discussions on how we can properly create, interpret, and share such large datasets.

\[caption id="attachment\_2187" align="aligncenter" width="640"\]![](https://news.open-bio.org/wp-content/uploads/2019/03/bigDataWorkshop-999x1024.png) Twitter feeds for the Big Data workshop.\[/caption\]

One speaker discussed guidelines on how to effectively manage and document large datasets. Another speaker tackled a modern bioinformatics nightmare: The maize community had strict rules for gene naming that were rigorously followed for decades until about ten years ago when scientists began assigning names to genes that already had names. Now, the same gene could have multiple names across multiple databases. The speaker suggested developing and abiding by nomenclature committees to fight the problem.

\[caption id="attachment\_2188" align="alignright" width="165"\]![](https://news.open-bio.org/wp-content/uploads/2019/03/logo.png) Hexagonal representation for the bigPint package.\[/caption\]

I presented my open-source software package called [bigPint](https://lindsayrutter.github.io/bigPint/), which provides interactive visualization methods for large datasets. I was excited to demonstrate the visualization toolkit to a room full of biologists because I think it can be useful for people possessing all levels of statistical background. Scientists need to apply normalization techniques and models to analyze their datasets but this can be difficult for people with little statistical knowledge. Visualization is inherently intuitive and can be used in a complementary fashion with models to allow scientists to better understand which analytical approaches may be the most suitable for their data. I think the workshop all together was aimed at democratizing data. Making data more accessible to more people. Making data easier to share.

After the conference, everyone seemed to want to go to "Charlie’s". I imagined Charlie was a well-liked and kind intellect who was hosting everyone and who I should probably want to meet, but eventually realized it was just a popular restaurant connected to the conference hotel. I am still glad I went. I met up with the NCBI hackathon organizer Ben and a fellow hacker Jan, two-spirited and sharp-witted individuals who have contributed vastly toward open science. I know firsthand that many hackathon organizers are working hard to increase the inclusiveness at their events. If you are interested in open source software development but are worried whether you will "measure up" or "fit in", keep in mind that many hackathons do not require advanced computer skills and are a great way to network with other enthusiasts while building those very skills in a supportive environment. One of the most valuable parts of this fellowship was the opportunity to reconnect with old and connect with new open science enthusiasts, and I hope the community continues to grow and diversify in the years to come. Thank you again to the OBF for supporting such a meaningful theme.
