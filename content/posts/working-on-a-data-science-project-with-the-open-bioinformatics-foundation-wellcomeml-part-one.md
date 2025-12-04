---
author: yo
category:
  - google-summer-of-code
date: "2021-06-17T17:09:06+00:00"
guid: https://www.open-bio.org/?p=5695
tag:
  - gsoc
title: Working on a data science project with the Open Bioinformatics Foundation, WellcomeML - Part one
url: /2021/06/17/working-on-a-data-science-project-with-the-open-bioinformatics-foundation-wellcomeml-part-one/

---
_This post is guest-posted by Federica Trevisan, an OBF GSoC student with the Wellcome Trust. Cross-posted with Federica's blog:_ [https://federikovi.medium.com/my-google-summer-of-code-2021-c795dd0cc794](https://federikovi.medium.com/my-google-summer-of-code-2021-c795dd0cc794 )

# My Google Summer of Code 2021

Well yes, I am part of GSoC 2021 💻☀️

## What is Google Summer of Code

In a nutshell, [GSoC](https://summerofcode.withgoogle.com/) is a remote program founded in 2005, in which Google connects students and organisations during the summer break from classes. In this global program the students work with an open source organization on a 10 week programming project during their break from school. In this way students can gain technical experience on real projects by “flipping bits not burgers” _._ It’s also a competitive program; this year only the 27% of students who submitted at least a proposal got accepted.¹

![Girl selfie with GSoC shirt after attending Google Developer Days Krakow in 2017](https://miro.medium.com/max/1200/1*VcbPjJSKRG7gBedhocLFqg.jpeg)Selfie with GSoC shirt after attending Google Developer Days Krakow in 2017

I learned about the GSoC when I had the opportunity to participate as a Women Techmakers member at the Google Developer Days in Krakow, Poland in September 2017. It was a period in which I decided to change the path of my academic career by pursuing a masters degree in Data Science after a bachelor degree in Economics.

Yes, that’s me wearing a GSoC shirt in 2017 without knowing that I would actually participate in summer 2021. Things happen!

Maybe the most difficult part is choosing the right project to work for (the second one is surely writing a strong and structured proposal, that will be the topic of another post). There are many organizations, 199 this year, with various and appealing projects, the important thing is finding one (or three, the maximum number of proposals you can submit) that fits with the interests and in which you can actively contribute. I have chosen Open Bioinformatics Foundation as I’m really interested in Bioinformatics and nature-inspired computing.

## Open Bioinformatics Foundation

The [OBF](/) is an umbrella mentoring organization that promotes the practice and philosophy of open source software development within the biological research community. Under its umbrella there are other organizations that have projects involved in GSoC. The project I am taking part of is with the global charitable foundation **Wellcome Trust** with my super mentor [Antonio Campello](https://github.com/aCampello).

## **Developing WellcomeML further for the visualisation of academic research data**

The objective for my [GSoC 2021](https://summerofcode.withgoogle.com/projects/#4986101921480704) is to create a standard interactive visualisation tool for the results of the clustering algorithm present in the WellcomeML library. [WellcomeML](https://github.com/wellcometrust/WellcomeML) is a python package containing a set of utility functions that use machine learning for reading, processing, embedding and classifying academic text data like publications, grants, and other documents.

During the community bonding period in which I met the mentors, got introduced to the staff of OBF and the staff of WellcomeML I virtually met also the other students working on differents OBF projects. Me and my mentor Antonio brainstormed some ideas for the TODO list of the project by creating a [Kanban board](https://github.com/wellcometrust/WellcomeML/projects/2).

Since WellcomeML is mostly developed on UNIX/UNIX-based systems, installing and running on Windows is not as straightforward as we would expect. During the talk-with-mentors period before the proposal submission I already encountered an issue when running the WellcomeML library on my Windows laptop, that has been fixed [in this issue](https://github.com/wellcometrust/WellcomeML/issues/257) with the help of the mentors.
The correct way to install WellcomeML on Windows is:

```
pip install torch==1.5.1+cpu torchvision==0.6.1+cpu -f https://download.pytorch.org/whl/torch_stable.html
```

_and then_:

```
pip install wellcomeml[deep-learning]
```

Make sure you have the correct torch version before using pip!

After engaging with some of the mentors, other issues² have been fixed, which will make other people’s lives easier in the future for developing on Windows. Here below there are the additional steps to take for installing and testing WellcomeML on Windows.

**Requirements:**

- Updated Windows 10
- Visual Studio Build tools 2019 with Desktop Development with C++
- Python 3.8 installed at the root of your machine (the Makefile will look for it in C://Python38)
- Administration rights

**Installation:**

- Clone and fetch WellcomeML repository from GitHub
- Install Cygwin64
- Install make through Cygwin64 with `choco install make`
- From Cygwin64 change directory `cd` to the path of the folder where the Makefile is
- Run the following Makefile `make virtualenv`

**Testing:**

- `make test` running tests might take a bit of time on the first run, as you will need to download some models and build a few libraries.

Now that I have a tested and running library in my laptop I can’t wait to start building the visualisations for the clustering algorithms. 💻☀️

## Notes:

1. Statistics from GSoC’21: 1292 students were selected from a total of 4795.
[https://opensource.googleblog.com/2021/05/google-summer-of-code-2021-students-are.html](https://opensource.googleblog.com/2021/05/google-summer-of-code-2021-students-are.html)
1. Instruction for Windows thanks to [https://github.com/wellcometrust/WellcomeML/pull/302/files](https://github.com/wellcometrust/WellcomeML/pull/302/files)
