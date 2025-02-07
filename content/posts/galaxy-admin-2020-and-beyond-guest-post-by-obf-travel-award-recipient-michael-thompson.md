---
author: mthompson
category:
  - community
  - travel-fellowship
cover:
  alt: Created with GIMP
  image: /wp-content/uploads/2020/03/e2.jpg
date: "2020-04-14T16:15:55+00:00"
guid: https://www.open-bio.org/?p=4626
tag:
  - galaxy
  - travel-fellowship
title: Galaxy Admin 2020 and beyond (guest post by OBF Travel Award recipient Michael Thompson)
url: /2020/04/14/galaxy-admin-2020/

---
_The [Open Bioinformatics Foundation (OBF)](https://www.open-bio.org) sponsors a Travel Fellowship program aimed at increasing diverse participation at events promoting Open Source bioinformatics software development and open science in the biological research community. Michael Thompson's participation at the_ [Galaxy Admin Training 2020](https://galaxyproject.org/events/2020-03-admin/) _workshop in Barcelona was supported by this fellowship. Find more information [here.](/travel-awards/)_

I had the opportunity to visit the [Barcelona Supercomputing Center (B.S.C)](https://www.bsc.es/) in Spain from 2nd \- 6th March 2020 to participate in the [Galaxy Admin Training 2020](https://galaxyproject.org/events/2020-03-admin/), organized by [Galaxy Europe](https://galaxyproject.eu/) and in partnership with [B.S.C](https://www.bsc.es/), [Elixir](https://elixir-europe.org/), and [de.NBI](https://www.denbi.de/).

### **Purpose**

The reason for attending was to gain the skill-set required to deploy and administer Galaxy within my university ( [Kwame Nkrumah University of Science and Technology](https://www.knust.edu.gh/)) which currently has a small group of students and researchers involved in Bioinformatics. I have had previous experience with HPC applications although this was my first for Galaxy. Our university’s deployment of Galaxy is also intended to be open to any researcher within my country, Ghana.

### **The Event**

The event was very well organized with training provided by Helena Rasche  (Galaxy Europe), Nate Coraor (Galaxy Project, Penn State University, U.S.A), Marius van den Beek (Galaxy Project, Penn State University, Europe), Saskia Hiltemann (Erasmus Medical Center, the Netherlands), and Nicola Soranzo (Earlham Institute).

The training materials are available [here](https://github.com/galaxyproject/admin-training).

On the first day, after registration, we dived straight into the setup/installation using Ansible. It was followed by a talk on the advanced setup of the system and configuration of tool-sheds. Later that day, we had a tour of the Barcelona Supercomputing Center to see [_MareNostrum_](https://www.bsc.es/marenostrum/marenostrum) – a supercomputer with a peak performance of 11.15 Petaflops.

![](/wp-content/uploads/2020/03/20200302_GalaxyAdminTraining_MN4_2-1024x576.jpeg)Participants receiving a lecture on the architecture of MareNostrum.

![](/wp-content/uploads/2020/03/20200302_GalaxyAdminTraining_MN4_3-1024x576.jpeg)A guided tour of MareNostrum.

The second day of the training hosted talks on deploying scientific tools using _Ephemeris_, configuring and using authentication methods, access to reference data for scientific analysis, configuring job scheduling, and connecting Galaxy to your existing HPC cluster.

On day three, we continued with more about job scheduling and connecting to compute clusters, connecting to remote clusters using Pulsar, storage management, making queries with _Gxadmin,_ and monitoring with _Telegraf_, _InfluxDB_ and _Grafana_.

![](/wp-content/uploads/2020/03/20200302_GalaxyAdminTraining_room-1024x576.jpeg)The training session.

The fifth day was about using interactive tools, development (deploying your own tools), build automation and advanced customization of the software (user interface). There was a session on Training As A Service (TiaaS) – a feature that allows you to create small groups of dedicated resources within Galaxy for running training sessions in a manner that isolates itself from the production work on the same platform.

On the last day, we had talks on how to deal with issues when they arise, management of different python versions, developing tools using _Planemo._ I had to leave before the very last talk about creating tutorials from the training resources provided.

### **Takeaways**

Every part of the event had hands-on training exercises. During these exercises, the trainers did a very good job of sharing their experiences. These experiences – what I call ‘street wisdom ‘– were useful in situating the exercises in real-life scenarios.

Particularly, I found the sessions on tool development, generating queries and monitoring very useful. The ability to integrate existing tools would enable the platform to support the different needs of the user community.  The monitoring and reporting utilities also provide an evidence-based and transparent approach to evaluating the usage of resources. This is important to demonstrate to our funders (the university in this case) how the facility is used and, when necessary, to make a case for upgrades or expansion.

Everything about Galaxy is Ansible! It is an example of very extensive use of automation without which management and maintenance would far more tedious. It enforces the DRY (Don’t Repeat Yourself) philosophy; the packaging and documentation of the entire software platform is an encouragement to use configuration management software extensively (and in all types of large software deployments).

Although a large number of the tools available on Galaxy are for use within the field of Bioinformatics, the platform has been designed to enable it to run almost any kind of tool. This means that one deployment of the platform can serve different scientific user groups if the available tools can be developed and integrated into the platform. To facilitate this, there is extensive tool development documentation. I find this particularly important in scenarios where there may not be a lot of resources (infrastructure, human, funding) to run different types of HPC platforms – some HPC/HTC installations out there are very limited, especially in developing countries. In my opinion, Galaxy alone, with a bit of effort in tool development, can be used to support a wide range of disciplines.

### **What Next**

The next few months will involve planning and organizing to deploy Galaxy for use locally. I am confident we would have some success stories and, hopefully, interesting use cases of the platform to share in another blog post later.

![](/wp-content/uploads/2020/03/e2-1024x611.jpg)Workshop participants at BSC.

### **Thanks to OBF!**

The opportunity to participate in the Galaxy Admin 2020 Training in Barcelona would not have been possible without the travel fellowship from OBF. I have had the opportunity to connect with different Galaxy Admins and to join a community of people enthusiastic about providing support to the scientific community. Many thanks to OBF!

**Me**

![](/wp-content/uploads/2020/03/Me.jpg)

I am an IT Manager at the University Information Technology Services (U.I.T.S) of the Kwame Nkrumah University of Science and Technology (K.N.U.S.T). I am also a member of the H3ABioNet project.
