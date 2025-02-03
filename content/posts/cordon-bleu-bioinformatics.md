---
author: saketkc
category:
  - bosc/ismb
  - travel-fellowship
cover:
  alt: cordon-bleu
  image: /wp-content/uploads/2019/08/cordon-bleu.jpg
date: "2019-08-25T18:08:26+00:00"
guid: https://www.open-bio.org/?p=3872
tag:
  - travel-fellowship
title: Cordon Bleu Bioinformatics
url: /2019/08/25/cordon-bleu-bioinformatics/

---
I attended the Bioinformatics Open Source Conference ( [BOSC](/events/bosc/) 2019) organized this year along with [ISMB/ECCB](https://www.iscb.org/ismbeccb2019) in Basel, Switzerland from July 21st-25th. BOSC 2019 was in multiple ways a lot of 'firsts' for me. I was attending my first ISMB/ECCB. It also happened to be my first time in Europe. It was the first time I was putting faces and voices to a lot of names. Like in most of the conferences these days, I met a lot of Twitter-verse friends for the very first time. And above all, this was my first ever BOSC.  I was funded in part by the Open Bioinformatics Foundation’s [Travel Award](/travel-awards/) and ISMB/ECCB’s Travel Fellowship. My travel and the learnings I summarize here would have been impossible without both.  

![](https://lh3.googleusercontent.com/2hnxxOt_KWFjNV-q51dGeodBwJQ_LjK9bom4AP2irMkBE1I6d5YE0eCZ_NrQqqT9_MCJAUAUnfV3cXMzj6CkySLpqdm6u8Pef25o76H9K4BPhMup6DwhNFN1Zf8mKd_fl63fKpCb)Nomi Harris introducing the 20th BOSC 2019 (Couldn't capture Nomi at this angle)

### **BOSC and me**

I had been trying to go to BOSC for around three years. I submitted three abstracts over the three years which were all accepted for a lightning talk. However, a lack of funding made it impossible for me to make it to  BOSC 2016 and BOSC 2018. I submitted my abstract for a poster and talk about [pysradb](https://github.com/saketkc/pysradb) that was selected for a lightning talk (a short five-minute talk) and a poster.  

### **ISMB/ECCB Single Cell Workshop**  

I arrived in Switzerland on July 19th, two days earlier than the official start date of the meeting and a day earlier than the Tutorial tracks.

OBF’s Travel award not only covered my ISMB registration but was also generous enough to cover the registration costs for Tutorial(s). ISMB/ECCB 2019 had multiple tutorial tracks spanning the fields of interpretation of deep learning in biology, computational drug discovery, statistical methods for single-cell RNA-seq, biological data visualization, biomarker discovery and tools for reproducible analysis. I decided to attend the tutorial on statistical methods for single-cell RNA-seq primarily to get an overview of the single-cell world, which is not very distant from my current research interest of deciphering translation regulation. The [tutorial](https://github.com/rhondabacher/ISMB2019_SingleCellTutorial) was very comprehensive and gave an overview of the technology, its nuances and the methods developed to tackle them. I expected it to be a bit more methods oriented, but it is difficult to have the best of everything for a diverse audience.   

### **Keynotes at ISMB**/ECCB

ISMB/ECCB being a large conference (owing to the fact that it is two conferences combined into one) is organized into multiple tracks. The upside of a large conference is that there is so much new to learn. An obvious downside is that it could be overwhelming. I followed an “on-the-day” optimization strategy where I would look up schedules for the talks for a day in the early morning. This would have been practically impossible without the ISMB’s conference app. Though there are traditional conference booklets, an app comes in handy in scheduling. Given the multitude of tracks involved, I would keep running from one room to other. The calm dusk at Rhine river came to the rescue after each day's heated effort, [quite literally](https://www.washingtonpost.com/climate-environment/2019/08/05/heres-how-hottest-month-recorded-history-unfolded-around-globe/),

I made sure I attended all the keynotes. Day 1 had Dr. Nikolaus Rajewsky’s keynote on how single-cell RNA-seq is making it easier to improve our understanding of gene regulation on a much granular scale in space and time. Day 2’s Keynote had Dr. William Noble walking us through the applied machine learning world in genomics: an embedding method for inferring the corresponding cells given two biological assays data and an imputation method for learning the latent representation of the epigenome. Day 3 had Dr. Alexis Battle talking about modeling the complex impact of common and rare genetic variation on gene expression. The field of Genomics is full of examples of missing ground truth. On Day 4, Dr. Christophe Dessimoz talked on “Challenges and rewards of benchmarking – how to cope with a biased, incomplete, or even entirely missing ground truth”. I had been aware of Dr.Christophe’s work through his paper on the [ortholog-paralog conjecture](http://doi.org/10.1371/journal.pcbi.1002514). Finally, Dr. Bonnie Berger’s keynote introduced me to the perils of data sharing in the genomic world and the solutions her lab has worked on over the years.

### **Poster Sessions**

The poster sessions were spread over 4 days of ISMB/ECCB. With approximately 1000 posters, it is overwhelming to digest all the information you obtain. I again relied on the ISMB/ECCB mobile app to shortlist ones that I really wanted to learn about. I am sure I still missed out on a bunch.

### **Keynote at BOSC**

Dr. Nicola Mulder’s keynote introduced us to the challenges faced by African countries, owing to their history of exploitation and inequitable scientific partnerships.

https://twitter.com/GigaScience/status/1154012905639206912?ref\_src=twsrc%5Etfw

[H3ABioNet](https://www.h3abionet.org) is a Pan-African bioinformatics network that is trying to address this challenge by making the controlled access data findable and interoperable for both data providers and users.

### **BOSC Takeaways**

BOSC happens over two days of the main conference that is often followed by another two days of [C](/wiki/Codefest) [oF](/events/bosc/collaborationfest/) [est](/wiki/Codefest). Unfortunately, I was not able to participate in CoFest. BOSC was packed with sessions on data crunching, data modeling and formats,  containers, open science, workflows and building open source communities. Besides these sessions there were also independent Birds of a Feather sessions (BoFs) which are informal self-organized meetups on [a myriad of topics](http://bit.ly/BOSC2019-bofs), spread over the two days. I participated in the “Reimaging the paper” BoF organized by Dr. Emmy Tsang of eLife Innovation. We discussed how the traditional model of publishing is limited in terms of reproducibility. The journals need to define a minimum standard for ensuring reproducibility, but defining what these gold standards should be, still remains a challenge in itself.

Summarizing all the talks at BOSC would be near impossible here. So I will describe the ones that got me super excited. The first one was by Dr. Malvika Sharan, on how promoting inclusiveness in Open Science communities requires an “open by design” approach where information sharing is scalable, the community is welcoming and supportive of newcomers and there are appropriate channels for skill transfer.

https://twitter.com/yoyehudi/status/1154384936893329408

Dr. Devon Ryan’s talk on [snakePipes](https://github.com/maxplanck-ie/snakepipes) was another talk that stuck around with me as it solves a critical problem that I have faced as a computational biology PhD student. A lot of data analysis requires mundane steps in analysis. snakesPipes is designed to make this useful for everyone with such a need, without forcing them to be familiar with CLI.

https://twitter.com/dpryan79/status/1154277950151372800?ref\_src=twsrc%5Etfw

If you are wondering what “eierlegendewollmilchsau” is, to the best of my knowledge (and memory), it translates to “has only advantages, satisfies all needs, meets all demands” and probably fits in well with the ideology behind snakePipes.

Mateusz Kuzak from Elixir in his talk “ELIXIR Europe on the Road to Sustainable Research Software” encouraged everyone to open source their work from day one. No, there is no evidence of your work being scooped if you choose to do so. Here is his advice:

https://twitter.com/morgantaschuk/status/1154326308203257857

I need to mention my fellow OBF Travel awardee Dr. Aziz Khan's efforts at building [ECRcentral](https://ecrcentral.org/) that helps early-stage researches find and discuss funding opportunities besides providing them a platform to share their experiences and mentor peers. As an early stage researcher myself, I have found the resources there extremely useful.


Finally, a project that I will keep a lookout on is [Biotite](https://www.biotite-python.org/) by Patrick Kunzmann designed as a  comprehensive and efficient computational molecular biology library. But we already have [Biopython](https://biopython.org)? Well, yes and no. Extensive usage of numpy and cythonization results in reduced runtimes.  

![](https://lh4.googleusercontent.com/npS5DuQPIX_4hhHWCzDthPHDjRCykY8e4dAZeCkWxcP9G6i3C2nLMyELMo4QkXdGxgVwmyB7PzgfQNfq1gVXBRfYa0Tz2Ssjz3MzE04hIqrqxskrjGOKRZM1exhsmpvOndIq9BWt)Biotite and Biopython: Open source wins

![](https://lh3.googleusercontent.com/5s1J3ioUYM2APb1TziwU046t17pcbNVPSwZmazeWNPmTiEwsK-7U2LXjNLjWsP3m1MHnK4_oTTFSrFMKyQZ81-n7_uP9s_nL5agnZ2KxXHQEAEeHQBlu72FqPq7ZsMAPjcYKQ2Ys)Biotite's perfomance compared at multiple tasks

**My lightning talk at BOSC**

My schedule before leaving for ISMB/ECCB 2019 from Los Angeles was jam-packed. I did the grave mistake of overestimating my ability to make a presentation for a 5-minute lightning talk. You just have to talk for 5 minutes, but then you have **only** five minutes. My presentation was only complete the night before my actual talk and would not have been possible without the feedback of Meghna Verma, a PhD candidate at Virginia Tech. I met her also for the first time at ISMB. I had a lightning talk on Day 1 where I talked about [pysradb](https://f1000research.com/articles/8-532), which I built over the last year to help me in my Ph.D. project. In the future, I plan to not overestimate my abilities, they are not worth the potential ill-effects they can have.  

https://twitter.com/yoyehudi/status/1153969142665502720?ref\_src=twsrc%5Etfw

I also had a poster on pysradb on the day of my lightning talk. I got a lot of visitors and a bunch of feedback. I hope pysradb also gets more contributors in the days to come!  

![](https://lh3.googleusercontent.com/lLZ26IxGrCPVJRK-Khv_Ljy7hPpP_w6MiSOCl6qoJOqRUYbCHsOJfYuefKPsc0tgSPQizZAYnZtChcT4b3hzxqO1_6XX98jVFrntGnChIjNrkFhkQ-pCy9Yyj-Mgv0zNyqhxVA38)P-01: pysradb poster

### **Applying for BOSC Travel Award**  

If you are thinking of traveling to any event promoting open-source bioinformatics software development and open science in the biological research community, OBF covers up to USD 1000 and it is possible to request a higher amount. The [application process](/travel-awards/) is one of the smoothest I have ever come across!  

Application Deadlines: April 15, August 15, December 15 every year.

### **Applying for ISMB Travel Fellowship**  

ISCB also provides Travel Fellowships that can come in handy if your original source of funding is not sufficient. Switzerland travel was a bit expensive, so I had applied for a travel fellowship once I got an acceptance. If you are submitting to ISMB in the future, you will receive instructions via email if you want to apply for a Travel Fellowship. Both the OBF and ISMB applications are very easy to fill out.

### **Cordon Bleu?**

Though more often associated with a [dish](https://en.wikipedia.org/wiki/Cordon_bleu_(dish)), I chose the title of this post as such for the high quality of talks at ISMB/ECCB and BOSC. I learned a lot in the span of five days and look forward to participating in the future as well. Again, I can’t thank enough the Open Bioinformatics Foundation and ISMB/ECCB for making this cordon bleu experience possible.  

![](https://lh3.googleusercontent.com/2fp5QayJNDfcjc7XBlMiOTpYKkYmYY_tq_QI4gWo9BCdgo0lTzieGmH3Qa3MPUCkKf5CSKtAw_ZCZdwkXinl2bSuek7tFzGL5AKPDDvKpaIbaVfgWOa0Y5kmRzUdyo4RKDyNOEG0)Cordon Bleu - the dish



![](https://lh6.googleusercontent.com/fzuwof2uE2o3YR58i2-1pIf10d8HtdcujGxopihgSooY0YMaJ3V_53KY6J6xgts1hUgTGKtjlHA6bXfj70fejtzWdiXUYDGLii7wkqEIUYgDCqkYsp9mrPfPmX14tgl42hrJHv86)Dusk at the Rhine river, a few minutes walk away from the conference venue
