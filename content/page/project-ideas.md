---
author: sarthaksehgal
date: "2020-01-05T15:45:08+00:00"
guid: https://www.open-bio.org/?page_id=4453
title: Project Ideas
url: /events/gsoc/gsoc-project-ideas/

---
# Google Summer of Code 2022 Project Ideas

* * *

Shortcut to project ideas:

- [Configurable feature visualization to improve the user experience and performance of the feature viewer](#feature-viewer)
- [Space- and time-efficient data format for mass spectrometry data (OpenMS)](#openms-data-format)
- [Efficient data layout for mass spectrometry data (OpenMS)](#efficient-layout-openms)
- [GPU support for Toil-CWL-Runner (UCSC/CWL Project)](#gpu-cwl-toil)
- [Improving automated wrapping of C++ code in Python (OpenMS/autowrap)](#openms-autowrap)
- [Migration of Journal Policy Tracker backend to Express + GraphQL](#journal-tracker-express)
- [Journal tracker - finalise and deploy React front-end](#journal-tracker-css)
- [Genestorian: data refinement](#genestorian-data-refinement)
- [Citation and databasing functionality in luox](#citation-and-databasing-functionality-in-luox)

##### Cross-Project Ideas

OBF is an umbrella organization which represents many different programming languages used in bioinformatics. In addition to working with each of the “Bio\*” projects (listed below) we also accept “cross-project” ideas that cover multiple programming languages or projects. These collaborative ideas are broadly defined and can be thought of as “unfinished” — interested contributors should adapt the ideas to their own strengths and goals, and are responsible for the quality of the final proposed idea in their application.

**Feel free to propose your own entirely new idea.**

* * *

###### Configurable feature visualization to improve the user experience and performance of the feature viewer

**Project description**

Analyzing positional features/annotations in sequences is important in bioinformatics. Visualizing such data is quite a challenging task, considering the large amount of data to be displayed. The feature viewer is an open source javascript library developed to visualize biological data (referred to as features) mapped to a linear sequence (Paladin et al., 2020). For instance, it can be configured to visualize the location of protein domains or amino acid variations in a protein sequence. The feature viewer is being used in several popular bioinformatics resources such as neXtProt and COSMIC 3D.

Currently, the feature viewer supports limited configurability options in the features displayed, such as the color, shape and on-click behavior. This is too restrictive for some of the possible use cases of the feature viewer, where more flexibility is required in the display of features. One such instance is when different types of amino acid variants should be displayed in a color-specific manner in the same feature track.

The overall goal of this project is to improve the configurability of the feature viewer, such that it allows greater flexibility in the visualization of detailed biological data. Specific aims of the project are:

- Simplify the configuration of new tracks

  The current version of the feature viewer requires new tracks to be hard-coded. Implementing a solution allowing new tracks to be added or existing tracks to be modified or deleted would ease the use of the viewer.

- Add graphical representations of numerical features

  Protein sequences can have features/annotations which are numerical. For instance, the frequency observed in a population of amino acid variants at a specific position. Such numerical data can be visualized as graphs of different types, such as line graphs or histograms.

- Configure the visualization of certain features in a class of feature

  Currently all the features displayed on a single track have the same color and/or shape; interesting features can not be highlighted using a different color or shape.

- Improve the speed of display by first displaying a summary or message

  Currently all the data displayed has to be provided before display, which results in slow loading and rendering time when there are tens of thousands of features. In order to improve the user experience, it is possible to initially show a message summarizing the data and only fetch and display the data on-demand by the user.

- Enable the user to download a snapshot of the current display

  The user community has requested a download button which generates a snapshot of the feature viewer. This feature will allow users to include an image of the data displayed in the feature viewer in a publication or elsewhere.

**Project size**

- 350h

**Languages and skills needed**

- Javascript
- HTML/CSS
- Git/Github
- Optionally: Java

**Difficulty**

- Medium to Hard

**Estimated Length**

- 20 weeks

**Mentors**

- Kasun Samarasinghe (kasun.wijesiriwardana@unige.ch)
- Lydie Lane (lydie.lane@sib.swiss)

**Contributor benefits**

- Gain experience in developing configurable libraries
- Gain experience in handling large amounts of data in web applications
- Gain experience on web application user experience
- Gain experience in biological data such as gene, protein sequences

**How to apply**

- For information on how to apply, please contact mentors in the emails provided above.

* * *

###### Space- and time-efficient data format for mass spectrometry data (OpenMS)

**Project description**

OpenMS is a framework for computational mass spectrometry. Modern mass spectrometers produce large files (e.g., 100 GB) that can’t be easily stored or accessed in the established XML file format mzML. Recently, an update to mzML has been developed that uses HDF5 to store Blosc compressed spectra in binary format: called mzMLb.  
In this project, the student will add a reader and writer for the mzMLb file format to OpenMS. To some extent, code from the OpenMS reader and writer for the mzML file format can be reused, as well as inspiration can be taken from reference implementations by other parties.

**Project size**

- 350h

**Languages and skills needed**

- C++
- Git/GitHub
- Optionally: CMake

**Difficulty**

- Easy for experienced C++ programmers with good CMake and GitHub skills. Medium for experienced C++ programmers without CMake or GitHub skills.

**Estimated Length**

- 20 weeks

**Mentors**

- Timo Sachsenberg, GitHub: https://github.com/timosachsenberg
- Julianus Pfeuffer, GitHub: https://github.com/jpfeuffer
- Samuel Wein, GitHub: https://github.com/poshul

**Contributor Benefits**

- Gain experience working in a friendly team of developers.
- Get a glimpse into the exciting field of bioinformatics / computational mass spectrometry.
- Obtain detailed knowledge on HDF5, which is widely used to store large data efficiently.

**How to Apply**

- Please introduce yourself in our Gitter channel: [https://gitter.im/OpenMS/OpenMS](https://gitter.im/OpenMS/OpenMS) and get in contact with us prior to writing a proposal.

* * *

###### Efficient data layout for mass spectrometry data (OpenMS)

**Project description**

OpenMS is a framework for computational mass spectrometry. It features a wide range of algorithms and data structures to process and analyze mass spectra. For some very computationally demanding parts, we performed manual code conversion to make the layout of our data better fit the data access patterns of our algorithms. We observed the biggest speedup switching the data layout from an Array of Structs (AoS) to a Structure of Arrays (SoA).  
In this project, the GSoC contributor will adapt our core data structure for mass spectra to AoS. Ideally, the contributor should be using a modern C++ zero-cost abstraction (e.g., building on https://github.com/crosetto/SoAvsAoS) that makes the old code work without (or minimal) manual changes.

**Project size**

- 175h

**Languages and skills needed**

- C++
- Git/GitHub

**Difficulty**

- Medium: requires a good understanding of modern C++.

**Estimated Length**

- 12 weeks

**Mentors**

- Timo Sachsenberg, GitHub: timosachsenberg
- Hannes Roest, GitHub: hroest
- Julianus Pfeuffer, GitHub: jpfeuffer
- Aditya R Rudra, Github: adityaofficial10

**Contributor Benefits**

- Gain experience working in a friendly team of developers.
- Get a glimpse into the exciting field of bioinformatics / computational mass spectrometry.
- Learn and apply modern C++ features to a real-life project.

**How to Apply**

- Please introduce yourself in our Gitter channel: [https://gitter.im/OpenMS/OpenMS](https://gitter.im/OpenMS/OpenMS) and get in contact with us prior to writing a proposal.

* * *

###### GPU support for Toil-CWL-Runner (UCSC/CWL Project)

**Project description**

Teach the [TOIL workflow system](https://github.com/DataBiosphere/toil) how to support GPUs with [CWL](https://www.commonwl.org/user_guide/). Optionally this can be expanded to HPC clusters. This will enable researchers to run specialized workflows that need occasional GPU support efficiently on university computing clusters.

**Project size**

- Either 175 (basic support) or 350 hours (advanced job routing)

**Languages and skills needed**

- Python
- Optional: HPC, Clustering

**Difficulty**

- Medium, or easier if you have experience with HPC or clustering.

**Mentors**

- Michael Crusoe, [https://github.com/mr-c]( https://github.com/mr-c)
- Lon Blauvelt, [https://github.com/DailyDreaming]( https://github.com/DailyDreaming)

**Contributor Benefits**

- Exposure to workflow engines and distributed computing

**How to Apply**

- To get started, visit [https://github.com/DataBiosphere/toil](https://github.com/DataBiosphere/toil), review the readme and the contributing guidelines: [https://toil.readthedocs.io/en/master/contributing/contributing.html#contributing](https://toil.readthedocs.io/en/master/contributing/contributing.html#contributing)

* * *

###### Improving automated wrapping of C++ code in Python (OpenMS/autowrap)

**Project description**

Autowrap is a python package for the automated wrapping of whole C++ projects into Python via Cython. C++ developers basically need to provide a Cython header file for each C++ header file to specify what needs to be wrapped and how. It then analyses the syntax tree generated by the Cython parser for those “header” files and generates Cython source code for it. Cython then creates the necessary source code to be compiled with e.g. CPython to create a Python extension module to be imported by the end-user. While the wrappers created by autowrap are rather simple, passing templated and nested STL objects like vectors, maps, or tuples between Cython/Python and C++ with autogenerated code can become rather complex. Autowrap offers recursion for nested vectors but cannot handle mixed data structures yet. It also misses support for newer STL containers like tuples and only offers simple vector to (Python) list conversions, while numpy arrays, e.g. via the buffer protocol would sometimes be more suitable. We are seeking for a motivated GSoC contributor proficient in at least Python to tackle those improvements.

**Project size**

- 350h

**Languages and skills needed**

- Python (advanced knowledge, for code generation)
- Cython (basic knowledge, potentially possible to be acquired, syntax similar to Python; to be generated)
- C++ (basic knowledge, potentially possible to be acquired; to be wrapped)
- Git/GitHub

**Difficulty**

- Medium: requires a deep understanding of Python and in the beginning at least some basic knowledge about its differences to C++ (regarding memory management and typing)

**Estimated Length**

- 20 weeks

**Mentors**

- Julianus Pfeuffer, GitHub: jpfeuffer
- Axel Walter, GitHub: axelwalter
- Timo Sachsenberg, GitHub: timosachsenberg

**Contributor Benefits**

- Gain experience working in a friendly team of developers.
- Get a deep understanding of two very commonly used programming languages and how to interface between them.
- It is also possible to learn how to create your own Python package with C++ extensions.

**How to Apply**

- Please introduce yourself in our Gitter channel: [https://gitter.im/OpenMS/OpenMS](https://gitter.im/OpenMS/OpenMS) and get in contact with us prior to writing a proposal.

* * *

###### Migration of Journal Policy Tracker backend to Express + GraphQL

**Project description**

The **Journal Policy Tracker** is your go-to place where you can find all the open-source scientific journals and their policies. Currently the backend of this project is on Flask and SQLite3 along with SQLAlchemy as the ORM. This project aims to migrate the backend from Flask and SQL database to Express, GraphQL using [express-graphql](https://graphql.org/graphql-js/express-graphql/) and a NoSQL database like MongoDB.

At the end of the program, the mentee is expected to do a successful migration of the existing server to an Express & GraphQL based backend.

- Repository: [codeisscience/journal-policy-tracker-backend](https://github.com/codeisscience/journal-policy-tracker-backend/)
- Existing API documentation: [journal-policy-tracker.herokuapp.com/swagger](https://journal-policy-tracker.herokuapp.com/swagger/)

**Project size**

- 175h

**Languages and skills needed**

Required skills:

- JavaScript
- Express.js
- GraphQL
- MongoDB
- Documentation (Markdown knowledge preferred)

Useful skills:

- Deployent nodejs apps to Heroku
- Familiarity with testing frameworks like Jest, Chai, Mocha in-order to write unit tests, integration tests and e2e tests.

**Difficulty**

- Easy if you have experience with GraphQL
- Medium if you are familiar with Express.js

**Estimated Length**

- Flexible, depending on contributor needs

**Mentors**

- Pritish Samal, pritish.samal918@gmail.com
- Yo Yehudi, yochannah@gmail.com

**Contributor Benefits**

- Experience developing in backend js frameworks and GraphQL.

**How to Apply**

- Please always email all mentors in the same mail if you would like to ask questions or discuss the project.
- You can also join the Code is Science [Slack workspace](https://join.slack.com/t/codeisscience/shared_invite/zt-16g3i8hr7-6j~jd_6JddhjEUBq9YUkmQ).

* * *

###### Journal tracker - finalise and deploy React front-end

**Project description**

The **Journal Policy Tracker** is your go-to place where you can find all the open-source journals and their policies. Currently the Frontend of this project is on React and React Bootstrap. This project aims to finalise the frontend after GSoC 2021, add state management and a user dashboard, and decouple the Frontend from CSS Frameworks for layout and presentation using Grid and Flex in place.

Tasks:

1. Study the existing user-interface for the journal policy tracker
1. Add functionality to the existing website while developing the components
1. Migrate the existing frontend CSS libraries to vanilla CSS
1. Work on the user-management dashboard
1. Use context/Redux for state management

- Repository: [codeisscience/journal-policy-tracker-frontend](https://github.com/codeisscience/journal-policy-tracker-frontend/)
- Frontend Preview: [journal-policy-tracker.netlify.app](https://journal-policy-tracker.netlify.app/)

**Project size**

- 175h

**Languages and skills needed**

Required skills:

- JavaScript
- React.js
- CSS3
- HTML5
- Grid
- Flex box
- Documentation (Markdown knowledge preferred)

Useful skills:

- Familiarity with HTML5 and CSS3 semantics
- Familiarity with UI/UX
- Familiarity with Writing tests

**Difficulty**

- Easy if you have experience with Grid, Flex box, and CSS page layout
- Medium if you are familiar with CSS page layout

**Estimated Length**

- Flexible, depending on contributor needs

**Mentors**

- Isaac Miti, ikayztm@gmail.com
- Yo Yehudi, yochannah@gmail.com

**Contributor Benefits**

- Experience designing and developing front-end interfaces.

**How to Apply**

- Please visit the repo: [codeisscience/journal-policy-tracker-frontend](https://github.com/codeisscience/journal-policy-tracker-frontend/) and make at least one contribution, and email the mentors to discuss your project proposal.
- You can also join the Code is Science [Slack workspace](https://join.slack.com/t/codeisscience/shared_invite/zt-16g3i8hr7-6j~jd_6JddhjEUBq9YUkmQ).

* * *

###### Genestorian data refinement

**Project description**

[Genestorian](https://www.genestorian.org/) is a web application to manage a collection of [model organism](https://en.wikipedia.org/wiki/Model_organism) strains and [recombinant DNA](https://en.wikipedia.org/wiki/Recombinant_DNA) in a life sciences laboratory.

New DNA sequences (inside or outside cells) are **always** generated by combining existing sequences. Genestorian leverages existing [semantic web tools for synthetic biology](https://sbolstandard.org/) and [libraries for DNA visualisation](https://github.com/TeselaGen/openVectorEditor) to provide an intuitive interface where researchers can plan, document and revisit their experiments. [Here](https://www.genestorian.org/internship) you can find a short summary of the problem we are adressing, adapted for the non-biologists.

An important challenge for the project is to migrate data from spreadsheets, where most labs keep their collections, to the database. In this project, the intern will develop a first version of a tool to perform the data refinement required to migrate from spreadsheet to the database.

**Project size**

- 350h

**Required skills**

- Good knowledge of text processing in a programming language (preferably Python).
- Willingness to learn the biology concepts that underlie the data models.

**Useful skills**

- Experience with data refinement and approximate string matching.
- Willingness to interact with experimental researchers of which the data will be refined.

**Estimated Length**

- Flexible, depending on contributor needs

**Mentors**

- Manuel Lera Ramirez, manulera14@gmail.com
- Yo Yehudi, yo@openlifesci.org

**Expected outcome**

Development of a first version of a tool to perform the data refinement required to migrate from spreadsheets to the database. The task could focus only on the program for refinement, but also developing a web interface for migration is a possibility. In addition to mentorship, we will organise two half-day sessions with a professional Research Software Engineer for helping and advising the contributor, and for code review.

**Difficulty level**

Medium if you have experience with string matching, easier if you know a bit of biology.

**How to Apply**

- Please always email _all_ mentors in the same mail if you would like to ask questions or discuss the project.

* * *

###### Citation and databasing functionality in luox

luox is a free, open-access and open-source platform for documenting and reporting light-related quantities from a spectrum of light written in JavaScript and React running directly in the browser. It is targeted to biomedical researchers looking for a convenient way to make their research with light(ing) interventions reproducible. Researchers can request a DOI (digital object identifier) for an uploaded spectrum, which is stored in a compressed/hashed way in the URL. The goal of this project is to develop simple database functionality to luox such that the web interface displays the DOI for any spectra that have already been assigned a DOI.

- Platform: [https://luox.app/](https://luox.app/)
- Repository: [https://github.com/luox-app/luox](https://github.com/luox-app/luox)
- Article describing the platform: [https://doi.org/10.12688/wellcomeopenres.16595.2](https://doi.org/10.12688/wellcomeopenres.16595.2)

**Project size**

- 350h

**Required skills:**

- Good knowledge of programming in JavaScript
- Good knowledge of web development
- Version control with Git

**Useful skills:**

- Knowledge of DOIs (digital object identifiers)

**Estimated Length**

- Flexible, depending on contributor needs

**Mentors**

- Manuel Spitschan, manuel.spitschan@tuebingen.mpg.de
- Yo Yehudi, yo@openlifesci.org

**Expected outcome**

- Functionality to look up DOI from the compressed/hashed spectrum through a table
- Display of the associated DOI in the web interface

**Difficulty**

- Medium

**How to Apply**

- Please always email _all_ mentors in the same mail if you would like to ask questions or discuss the project.
