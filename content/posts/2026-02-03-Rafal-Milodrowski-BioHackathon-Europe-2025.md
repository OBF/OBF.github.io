---
author: milodrowski
date: 2026-02-04

category:
 - community
 - event-fellowship
 - travel-fellowship
tag:
 - community
 - event-fellowship
 - travel-fellowship

title: "BioHackathon Europe 2025: BUSCO genes, lakeside hacking, and open workflows"
url: /2026/02/03/2026-02-03-Rafal-Milodrowski-BioHackathon-Europe-2025/
---

The Open Bioinformatics Foundation (OBF) Event Fellowship program aims to promote diverse participation at events promoting open-source bioinformatics software development and open science practices in the biological research community. I was awarded an OBF Event Fellowship to attend BioHackathon Europe 2025, held 3–7 November at the Esplanade Resort & Spa in Bad Saarow, near Berlin, Germany.
I am a PhD student at the Jagiellonian University in Kraków, working with insect genomes and large-scale comparative datasets. BUSCO is part of my everyday toolkit, so spending a week contributing to a BUSCO-based phylogenomics workflow with an international team felt like a perfect fit. The fellowship covered my travel costs and made it possible for me to fully participate in the hackathon.
![View of Lake Scharmützelsee and the Esplanade Resort & Spa from the lakeside promenade.](static/img/2026/2026-02-04-hotel.jpg)

## A hackathon by the lake

BioHackathon Europe took over a lakeside hotel that turned into a giant shared office for a week: meeting rooms full of laptops and whiteboards, and a steady flow of coffee and conversations. Mornings started with a short plenary, followed by focused hacking sessions in the project rooms. Evenings were more relaxed, with social activities, ad‑hoc debugging sessions, and lots of informal discussions about tools, data and careers.



## Project #03: benchmarking BUSCO genes for phylogenomics

I joined project #03, “Automatic workflow for benchmarking BUSCO genes for phylogenomics”. BUSCO lineage datasets are widely used to assess genome completeness and to extract putatively single-copy orthologs for phylogenetic analyses. However, once you look across many genomes at once, especially in groups with whole‑genome duplications, it quickly becomes clear that many BUSCO loci are not truly single copy. Our project aims to make this complexity visible and manageable.
The goal for the week was to turn existing scripts and a prototype workflow into a robust Snakemake pipeline that starts from BUSCO output and ends with phylogenomic trees. The workflow includes steps for multiple‑sequence alignment and trimming, gene‑tree inference, detection of in‑ and out‑paralogs, and construction of concatenated supermatrices and species trees that explicitly account for paralogy.

![Morning meeting  on zoom and coding session.](static/img/2026/2026-02-04-meeting.jpg)

## My role: testing and debugging 

Coming from a background of running Snakemake pipelines on HPC systems, I focused on the “does this actually run for a new user?” side of the project. A surprising amount of hackathon time can disappear into environment issues, so as a team we invested early in getting a clean, reproducible setup with conda and Snakemake  with clearly pinned software versions.
My main contribution was to run the pipeline on a curated set of genomes and report back where things broke or behaved unexpectedly. This included checking intermediate outputs (alignments, gene trees, paralog reports), tracking down missing dependencies, and helping to standardise file naming conventions for genome FASTA files and BUSCO output directories. These details may sound minor, but they are crucial when scaling up to dozens or hundreds of genomes.

![Schema of the pipeline used in our project](static/img/2026/2026-02-04-pipeline.jpg)

## Community and mid‑week reporting

A highlight of the week was the mid‑week reporting session, where each project prepared a short poster and gave lightning updates. Walking around the room, it was impressive to see the variety of topics being tackled in parallel: workflows, training materials, AI‑readiness, data standards and more. Presenting our BUSCO project forced us to summarise why this workflow matters, not just how it works.
The poster session also helped to connect with people from other projects who use BUSCO or phylogenomics in their own work. Several visitors were interested in applying the workflow to their clades, and their questions helped us clarify which configuration options and outputs will be most useful for future users.

![Photo of me and our mid‑week reporting poster.](static/img/2026/2026-02-04-poster.jpg)

## Take‑home messages

The week left me with a few key lessons:
**- Reproducible workflows are a collective effort.** Agreeing on file naming, pinning software versions and writing documentation takes time, but doing it together during a hackathon pays off immediately.
**- “Single‑copy” genes are often more complicated than they look.** The preliminary results we explored during the week highlight just how common paralogy is, even in supposedly universal BUSCO sets.
**- Hackathons are great for collaboration across time zones.** Our work in Bad Saarow connected with contributions from an Australian outpost of the project, with progress passed back and forth through shared repositories and notes.
**- Open tools lower the entry barrier.** By investing in a polished, documented workflow instead of a one‑off analysis, we make it easier for others to reuse and extend our work.

## What comes next

The work we began at BioHackathon Europe 2025 will continue as the team refines the workflow, runs it on additional clades and prepares it for broader release. For my own research, I am excited to apply the BUSCO phylogenomics pipeline to insect genomes and to compare patterns of paralogy across groups with very different genome architectures. I expect this will directly improve the robustness of the phylogenies I use in my PhD.

![Official BioHackathon Europe 2025 group picture in the courtyard.](static/img/2026/2026-02-04-people.jpg)

---

## Acknowledgements

I am very grateful to the Open Bioinformatics Foundation for the Event Fellowship that made my participation in BioHackathon Europe 2025 possible, and to the organisers from ELIXIR for creating such a welcoming environment. I would also like to thank the BUSCO phylogenomics project leads and all my teammates for their patience, good humour and willingness to explain things one more time when the logs got confusing. Finally, I appreciate the support of my home institution and colleagues in Kraków, who made it easier for me to step away from local duties for a week of focused hacking.
Thank you, OBF!

---
