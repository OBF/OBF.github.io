---
author: "Aditya Karna"
date: 2026-08-05
draft: true
category:
 - community
 - event-fellowship
 - travel-fellowship
cover:
  image: /img/2026/2026-08-05-aditya-karna-bosc-talk.jpg
  alt: "Aditya Karna presenting FedViz at BOSC ISMB 2026"

tag:
 - community
 - event-fellowship
 - travel-fellowship

title: "From FedViz to BOSC: My First Look into an Open Bioinformatics Community"
url: /2026/08/05/2026-08-05-aditya-karna-fedviz-bosc/
---

**_The_** [**_Open Bioinformatics Foundation (OBF) Event Fellowship program_**](/travel-awards) **_aims to promote diverse participation at events promoting open-source bioinformatics software development and open science practices in the biological research community. Aditya Karna,_** _**an undergraduate student at Springfield College**_, **_was awarded an OBF Event Fellowship to attend_** _**the**_ **_[Bioinformatics Open Source Conference (BOSC) 2026](https://www.open-bio.org/events/bosc-2026/)_**.
![Aditya Karna presenting FedViz at BOSC ISMB 2026](/img/2026/2026-08-05-aditya-karna-bosc-talk.jpg)

Attending BOSC/ISMB 2026 in Washington, D.C with support from the Open Bioinformatics Foundation Event fellowship was a very rewarding milestone for me. This was my first time being in a space where open-source software, biology, data infrastructure, and the research community all came together in one place. I had followed some of these ideas from the outside before, but being there in person made the work feel much more real.

Presenting FedViz at BOSC/ISMB 2026 in Washington, D.C.

I came to BOSC to present [FedViz](https://github.com/collaborativebioinformatics/FedViz), a project I worked on around federated biomedical data. The basic idea behind FedViz is simple: before different sites try to train models together using federated learning, we should first ask whether their data is actually ready to be used together. Different biobanks and cohorts may collect different variables, describe them differently, or have missing information in different places. If we ignore that stage and jump directly to modeling, we may build systems that look technically impressive but are not actually reliable.

In our work, we looked at metadata across 14 international cohorts and indexed 11,511 unique variables. Out of those, only 120 variables appeared in at least eight cohorts, which gave an immediate model-ready surface of about 1.04%. That number stayed with me because it made the problem very clear. The hard part is not only training a model. A lot of difficulty comes earlier, from understanding what is available, what is missing, and what can realistically be compared across sites.

![FedViz focused on metadata readiness before federated biomedical learning](/img/2026/2026-08-05-aditya-karna-fedviz-poster.jpg)

FedViz focused on metadata readiness before federated biomedical learning.

Presenting this at BOSC was both exciting and intimidating. It was different from explaining the project to classmates or working on it privately. At BOSC, the audience included people who actually build and maintain tools for biological research. That made me think more carefully about how to explain the motivation, not just the technical details. I also got to present the poster, which gave me more time to talk through the project and hear how people understood the problem. I remember walking into the session before my talk and realizing this was no longer just a project on my laptop. I had to explain why the problem mattered to people who work on real biomedical data systems. During the poster session, I also spent time looking at other posters on modeling, uncertainty, and biomedical data. Seeing how other researchers framed their problems helped me think about FedViz more clearly.

One thing I appreciated about BOSC was that the community did not treat open source as just putting code online. Many of the conversations were about sustainability, usability, and whether a tool can actually help other people do science. That was important for me to see. As a student, it is easy to focus on building a prototype or getting a result. BOSC reminded me that useful scientific software also needs trust, maintenance, and community around it.

![A poster connecting academia-industry hackathons with open biomedical data science](/img/2026/2026-08-05-aditya-karna-bosc-hackathon-poster.jpg)

A poster connecting academia-industry hackathons with open biomedical data science.

The conference also helped me think about FedViz beyond the hackathon stage. I left with a clearer sense that metadata readiness and site compatibility are not side issues. They are central to whether federated biomedical AI can work responsibly. If sites are not comparable, or if the assumptions are hidden, then even a good model can be built on weak ground.

The OBF event fellowship made this experience possible for me. As an undergraduate student without a large lab travel budget, attending a conference like BOSC would have been difficult on my own. The support allowed me to present my work, meet people in the open bioinformatics community, and see how research software is discussed by people who build these systems in practice.

I am thankful to the Open Bioinformatics Foundation for supporting my participation at BOSC/ISMB 2026. I am also thankful to the BOSC community, my collaborators on FedViz, and the people who gave feedback before and during the conference.

After BOSC, I am left with a better understanding of open bioinformatics as a community, not just a field. For me, FedViz is still an early step, but the experience helped me see why tools that make data assumptions visible can matter. Before federated learning can be useful across biomedical sites, we need better ways to understand readiness, compatibility, and trust. BOSC helped me see that this kind of infrastructure work belongs inside the open science conversation.
