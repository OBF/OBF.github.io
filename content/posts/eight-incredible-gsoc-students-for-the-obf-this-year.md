---
author: yo
category:
  - google-summer-of-code
  - uncategorized
cover:
  alt: ""
  image: /wp-content/uploads/2021/06/image-8.png
date: "2021-06-17T17:05:36+00:00"
guid: https://www.open-bio.org/?p=5693
tag:
  - gsoc
title: Eight incredible GSoC students for the OBF this year ☀️
url: /2021/06/17/eight-incredible-gsoc-students-for-the-obf-this-year-☀️/

---
![sixteen grinning faces of GSoC mentors and students for the OBF.](/wp-content/uploads/2021/06/image-8-1024x591.png)OBF students and mentors at an OBF kickoff call

Every year the OBF applies to participate as a mentoring organisation for [Google Summer of Code](https://summerofcode.withgoogle.com/), a paid work experience program where students get the chance to do paid work on an open source project and open source organisations host the students to work on their projects. This year, eight projects have participated under the OBF umbrella - read more about these fantastic students and their work below:

## Enabling and prototyping JavaScript visualization in QT-based viewer TOPPView

**Student:** Dhanmoni Nath  
**Mentors:** Julianus Pfeuffer, Timo Sachsenberg

OpenMS’ TOPPView tool is used for mass-spectrometry data analysis. However, TOPPView is lacking some often requested high-level summary views of results that are produced by OpenMS’ other tools. Although we have other open-source libraries that provide this feature, they are written in JavaScript, and re-implementing them in C++ to integrate into TOPPView would be tedious.

This project aims to solve this problem by enabling JavaScript visualizations in TOPPView using Qt’s QtWebEngine module.

[https://summerofcode.withgoogle.com/projects/?sp-page=2#4803704407982080](https://summerofcode.withgoogle.com/projects/?sp-page=2#4803704407982080)

## GtfBase - A curated resource of multispecies genomic regions

**Student:** Tanishq Gupta  
**Mentors:** Saket Choudhary, Amal Thomas

Each genome has some common features: exons that make the mRNA, CDS, and UTRs. There are a lot of resources available that provide access to these features in the form of General Transfer Format (GTF) files.  
While GTF files are by themselves comprehensive, a lot of analysis is focused on individual features and these analyses often rely on a BED file, a more focused variant of GTFs. Though it is trivial to obtain a BED file from GTF, currently there are no resources that provide ready access to BED files.

We have a collection of scripts currently available as part of gencode\_regions repository: [https://github.com/saketkc/gencode\_regions](https://github.com/saketkc/gencode_regions) that tries to address this gap. For GSoC2021, our goal is to generalize these scripts into a usable tool that can be used to generate BED files for a variety of use cases and serve as a readily updated database of BED files that will keep in sync with ENSEMBL’s GTF releases.

[https://summerofcode.withgoogle.com/projects/#5730763485478912](https://summerofcode.withgoogle.com/projects/#5730763485478912)

## Developing WellcomeML further for the visualisation of academic research data

**Student:** Federica Trevisan  
**Mentors**: Jeff Uren, Elizabeth Gallagher, Antonio Campello

WellcomeML is a python library with functions that use machine learning for reading, processing, embedding, extracting entities and classifying academic text data like publications, grants, and other documents. However, the visualisation modules of WellcomeML are scarce and the need of developing further visualisation features for the library has emerged.

In this specific case the objective is to create a standard interactive visualisation tool for the outputs of [wellcomeml.ml.clustering](https://github.com/wellcometrust/WellcomeML/issues/221). The current state of the art of WellcomeML provides an ad-hoc visualisation built from scratch for each algorithm applied. In this way the codebase is very specific to the single algorithm function and doesn’t provide a standardized output for the visualisation of the results.

The aim of this GSoC project is then to standardize the way the results are presented; an interactive dashboard, function or class for showing the clustering results for each project in a self explanatory way.

[https://summerofcode.withgoogle.com/projects/#4986101921480704](https://summerofcode.withgoogle.com/projects/#4986101921480704)

## Development of a user interface to visualise VEP data using neXtProt tools

**Student:** Shrey Sachdeva  
**Mentors:** Kasun Samarasinghe, Lydie Lane

Several open source tools, such as the Ensembl Variant Effect Predictor (VEP), have been developed to predict the structural and functional effects of variants.

The VEP tool has a number of plugins, including a neXtProt plugin that was released as a command line. The goal of this project is to develop a user interface using the neXtProt tools, to visualise the predicted variant effect output for all variants within a neXtProt entry.

[https://summerofcode.withgoogle.com/projects/#5720209559650304](https://summerofcode.withgoogle.com/projects/#5720209559650304)

## Implementations of AVX-512 functions

**Student:** Kunwar Maheep Singh  
**Mentors:** Evan Nemerson, Jun Aruga

SIMD instruction intrinsics provide users with extreme control over vectorization of code, but the problem with using them is that they are not very portable. This is because different vendors provide their own API’s to match the instruction sets implemented in their hardware. e.g. MMX, SSE2, AVX-512, etc. on Intel x86, Altivec and VSX on PowerPC, and NEON, MVE, and SVE/SVE2 on ARM.

SIMDe is a header only library which provides portable implementations of various SIMD APIs on unsupported hardware using instructions which are available, minimizing or even eliminating performance losses.

AVX-512 has added many new types of instructions like conflict detection and prefetch which give more vectorizing potential to developers. A combination of these new instructions with new compilers can help vectorize code which could not be vectorized before.

The aim of this project is to implement multiple families of AVX-512 intrinsics for SIMDe.

[https://summerofcode.withgoogle.com/projects/#4790187072159744](https://summerofcode.withgoogle.com/projects/#4790187072159744)

## Implementation of NEON functions in SIMDe

**Student:** Atharva Nimbalkar  
**Mentors:** Evan Nemerson, Zhi An Ng

SIMD stands for Single Instruction Multiple Data. It’s a class of parallel computers that performs the same instruction on multiple data points simultaneously. SIMD can be very advantageous to multimedia applications.

SIMDe is a library that provides portable implementations of SIMD Intrinsics on hardware that don’t natively support them, while still taking advantage of SIMD when possible. It allows you to call NEON functions on x86, or SSE functions on ARM, etc.

This project aims to add portable implementations of many more NEON functions  
in SIMDe. Along with native fallbacks for other popular architectures, which would allow NEON SIMD intrinsics to be used on WASM, AVX-512 etc.

[https://summerofcode.withgoogle.com/projects/#4927690232037376](https://summerofcode.withgoogle.com/projects/#4927690232037376)

## Design and implementation of Code is Science front-end using ReactJS

**Student**: Isaac Miti  
**Mentors**: Yo Yehudi, João Paulo Tiz

The Code is science website is currently built using vanilla HTML, CSS and JavaScript with Ruby as part of its backend. The current frontend needs to be redesigned and updated.

This project aims to design and develop the code is science frontend using ReactJS UI library. The project development will follow frontend best practices using Google’s Material Design guidelines.

[https://summerofcode.withgoogle.com/projects/#4963542471540736](https://summerofcode.withgoogle.com/projects/#4963542471540736)

## Data streaming in scientific workflows, implementation for Toil

**Student:** Mihai Popescu  
**Mentors:** Michael R. Crusoe, Lon Blauvelt

Toil is an open-source Python workflow engine that lets people write data analysis pipelines in Python, CWL, and WDL. Toil has support for common workflow language (CWL), an open standard for describing analysis workflows.

This project aims to implement data streaming to speed up the analysis by avoiding slow disk/storage IO and speeding up the start of tool execution when it isn’t required to wait for data to download. The main focus is to implement this first in AWS S3.

[https://summerofcode.withgoogle.com/projects/6469533377757184](https://summerofcode.withgoogle.com/projects/6469533377757184)
