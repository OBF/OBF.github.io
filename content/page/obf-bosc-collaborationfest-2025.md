---
author: hmenager
cover:
  alt: CoFest-2022
  image: https://open-bio.org/wp-content/uploads/2022/08/image4.jpg
date: "2025-02-16T09:35:44+00:00" #creation date
title: ISMB CollaborationFest 2025
url: /events/bosc-2025/ismb-collaborationfest-2025/
aliases:
  - /events/bosc/collaborationfest/
bosc: yes
---

ISMB CollaborationFest 2025 will be a collaborative work event at which participants work together to contribute code, documentation, training materials, and challenging analysis problems and use cases. If you are interested in learning and contributing in an intensely collaborative environment, then CollaborationFest is for you. Bring your own project ideas or come ready to collaborate with others on their projects!

![Participants at CoFest 2024](/wp-content/uploads/2025/01/cofest2024-1.jpeg)

BOSC has organized CollaborationFests (aka CoFests) every year before or after ISMB since 2010 (see, for example, [the 2024 CoFest page](https://open-bio.org/events/bosc-2024/obf-bosc-collaborationfest-2024/).). This year, we are excited to hold **CollaborationFest as part of ISMB/ECCB, opening it to all registered ISMB/ECCB participants**. The organizers are affiliated with four different COSIs: BOSC, Bio-Ontologies and Knowledge Representation (BOKR), Function COSI, and 3DSIG.

### Dates

Wednesday July 23 to Thursday July 24 (the last two days of ISMB/ECCB 2025).

### How to sign up

{{< columns >}}

Due to space constraints, participation in CollaborationFest is limited. To indicate your interest, [register for ISMB/ECCB 2025](https://www.iscb.org/ismbeccb2025/register) by June 20 and **sign up for CollaborationFest as an “add-on” during the registration proces**s. We will contact you by June 23 to gather additional information to help organize the event. Last-minute walk-ins may be possible if space allows.

Limited remote participation will be possible, but engagement opportunities will depend on the people and projects active on the day. A video feed from the room will be available, but joining will require you to be a registered (virtual or in-person) ISMB/ECCB participant.

{{< column >}}

![Lunch at CoFest 2023](/wp-content/uploads/2023/08/CoFest2023-lunch-1-736x1024.png)

{{< endcolumns >}}

### CollaborationFest News and Activities

As we get closer to ISMB/ECCB 2025 and the CollaborationFest, we will add relevant news and activities here. Note that some of
these activities are on dynamically updated Github pages, and will only be fully ready "the day of", or shortly before.

#### 1. Genomic Safe Harbor Sites in Zebrafish

This challenge invites participants to identify potential genomic safe harbor (GSH) sites in the zebrafish genome using an
integrative omics approach.

https://github.com/parnaljoshi/gsh-zebrafish-hackathon

#### 2. How much funding per protein?

Quantifying the financial investment in specific areas of biomedical research is challenging. While NIH funding is extensive,
directly attributing grant dollars to individual proteins studied is non-trivial. Approximating the dollar amount of funding
allocated to the proteins help us to:

* Assess funding distribution across different biological targets.
* Identify potentially under-funded or over-concentrated areas of protein research.
* Track the financial trajectory of research on specific proteins over time.
* Provide researchers and funding agencies with data about financial resource allocation at the protein level.


https://github.com/anphan0828/funding-per-protein-hackathon

#### 3. Enhancing Protein Knowledge Curation using Gene Ontology Annotations and Large Language Models for Community Literature Submissions

Data-driven biomedical discovery depends on effective data curation - a time-consuming process that involves identifying relevant literature, extracting experimental knowledge, and validating information into structured formats suitable for databases like UniProt.

The emergence of generative AI and large language models (LLMs) presents new opportunities to assist human-driven data curation workflows. These technologies can support curators in searching ontologies and extracting knowledge from scientific literature, potentially streamlining the entire curation process.

**Objective**

Learn how to manually assign Gene Ontology terms or develop innovative approaches using LLM tools to enhance the curation workflow, enabling efficient and accurate extraction of experimental data from scientific literature.

https://github.com/anphan0828/ISMB_CollaborationFest_EBI

#### 4.  BioPython-GPU: Accelerate BioPython MSA-GPU Protein Aligner

Integrate drop in GPU-accelerated MMseq2 into biopython for acceleration.

https://github.com/collaborativebioinformatics/GPU_MSA_Integration

#### 5. Integrate iCn3D viewer with Jalview MSA

Jalview shows MSA and structure alignment with Jmol. Jalview could also link to iCn3D to show MSA together with structure alignment.
https://github.com/jiywang3/Integrate-iCn3D-viewer-with-Jalview-MSA

#### 6. The world’s biomedical knowledge in less than a gram: introducing the PGP incubator

The PGPincubator is an effort to create a distribution of open data, tools, workflows, AI models, and learning materials that support validation, benchmarking, and education in bioinformatics and biomedicine for precision health and (pre-clinical) biomedical AI. In addition, the incubator is a distributed network of physical computing infrastructure used to test components included in the distribution, such as validating genomics workflows or benchmarking AI models.

To help hatch this network, PGPincubator is creating a network (using Tailscale) of “h-grams.” A h-gram is 1-4 microSD cards (3-4 weigh about a gram!) each flashed with a bootable operating system image and pre-loaded with data and tools. The PGPincubator open source project develops and maintains the scripts, process documentation and data resources required to build/test the h-gram image. These h-grams can then be booted on compatible commodity PC hardware. The operating system (Ubuntu) is pre-configured to act as a server suitable for home, office or lab and is accessed by other devices through a browser. Each h-gram will be pre-loaded with hundreds of gigabytes of openly licensed infrastructure software, bioinformatics tools, genomic datasets, AI models, and learning resources, making them ideal for education, validation, and benchmarking in biomedical research.

We'll be demoing how to use the PGPincubator live!
https://github.com/PGPinformatics/PGPincubator

#### 7. Collaborative development of gRINN (get Residue Interaction Energies and Networks) for interaction energy based analysis of biomolecular simulation trajectories

This project focuses on enhancing gRINN, a Python tool for analyzing protein energy networks from molecular dynamics simulations. gRINN calculates amino acid interaction energies from GROMACS trajectories and constructs Protein Energy Networks to identify key residues in protein communication pathways.

We invite contributors to test the tool with diverse protein systems, identify bugs, develop tutorials, and optimize performance. Testers, developers, and documentation contributors at all skill levels are welcome.

https://github.com/osercinoglu/grinn-ismb-2025

#### 8. Improving how we describe and discover Bioinformatics tools

Bioconductor hosts over 3,000 R packages, but finding the right one can be challenging. biocEDAM is an experimental tool that uses large language models and the EDAM ontology to suggest meaningful package tags.

At CoFest, we’ll work on integrating Gemini (a free, key‑free option) and testing the tool on more packages. We also welcome input on Model Context Protocols (MCPs), exploring how they might help surface package metadata in the future.

Who should join: R developers, ontology experts, LLM/NLP enthusiasts, and anyone with domain knowledge keen to improve software discoverability.

https://github.com/mblue9/biocedam-cofest-2025

### 9.  Extracting metadata from proteomics publications

Many proteomics studies share raw data, but their experimental details remain buried in free-text methods and supplementary tables, making reuse and meta-analysis difficult. This project invites you to build models or pipelines that extract structured metadata—like organism, instrument, or disease—from paper abstracts and methods sections, using a gold-standard training set and clear evaluation tools.

You'll work with a curated training set of 100+ annotated papers and compare your results to a GPT-o4-mini baseline. In the second phase, test your model on recent, unannotated publications to assess generalizability.

Ideal for: NLP practitioners, proteomics researchers, or anyone interested in making scientific metadata more accessible and machine-readable.

https://github.com/SparkyDaBear/Intelligent_MetaData_ISMB_collaboration_fest_2025



### Code of Conduct

As part of ISMB/ECCB 2025, CollaborationFest 2025 is covered by the [ISCB Code of Ethics and Professional Conduct](https://www.iscb.org/iscb-policy-statements/iscb-code-of-ethics-and-professional-conduct).
