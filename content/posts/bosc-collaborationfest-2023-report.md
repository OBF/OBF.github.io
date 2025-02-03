---
author: jeremy.just
category:
  - bosc/ismb
  - cofest
  - community
  - events
  - general
cover:
  alt: CoFest_lunch_collage
  image: /wp-content/uploads/2023/09/CoFest_lunch_collage.jpg
date: "2023-09-29T22:08:37+00:00"
guid: https://www.open-bio.org/?p=7341
tag:
  - bosc
  - bosc/ismb
  - codefest
  - cofest
  - europe
title: BOSC CollaborationFest 2023 Report
url: /2023/09/29/bosc-collaborationfest-2023-report/

---
![](/wp-content/uploads/2023/10/CoFest2023_welcome.jpg)

**CollaborationFest**, CoFest for short, is a collaborative work event that has been held each of the past 13 years as a satellite event of BOSC. At these free events, held right before or after BOSC, participants  gather in small groups to exchange ideas and work together on projects including but not limited to hacking. Participants were encouraged to submit their project ideas in advance to facilitate collaboration.

[**CoFest 2023**](/events/bosc-2023/obf-bosc-collaborationfest-2023/) took place during the two days just before [BOSC](/2023/08/14/bosc-2023-report/), which was part of ISMB/ECCB 2023 in Lyon and online. It was the first in-person edition after several online-only CoFests, due to Covid pandemics. It was hosted by Jérémy Just at the nearby [_École Normale Supérieure de Lyon_](https://www.ens-lyon.fr/en/), which provided space and infrastructure, with funding from [_Complex Systems Institute_](https://www.ixxi.fr/?set_language=en) for lunches and coffee breaks. Free virtual machines were made available by the [_French Institute for Bioinformatics_](https://www.france-bioinformatique.fr/en/home/) and the [_Pôle scientifique de modélisation numérique_](https://www.ens-lyon.fr/PSMN/doku.php?id=en:accueil).

![](/wp-content/uploads/2023/09/project_list-1024x1024.jpg)List of the projects submitted in advance by the participants for BOSC CoFest 2023.

CoFest brought together 29 in-person participants as well as numerous online participants, experts in fields as diverse as plant biology and personalized medicine.

We were pleased to have many local and first-time attendees participate in this edition of CoFest.

A 360° webcam, kindly lent by [Elixir](https://elixir-europe.org/) for the CoFest, allowed remote attendees to see the whole meeting room during work sessions.

As in previous years, CoFest participants engaged in a wide variety of projects focused on topics such as the documentation of existing software, the review and discussion of novel technologies, the improvement of existing tools, and several FAIR-related projects.

In total, the participants worked on ten different projects, with tangible accomplishments for several subtasks of these projects. In addition, cross-project discussions facilitated progress on many projects, exchanging perspectives and pointers between participants. The synergies and discussions between the various groups were remarkable.

> **We would like to thank the entire [OBF community](/) for maintaining the positive atmosphere that makes such events a reproducible success!**

![](/wp-content/uploads/2023/09/CoFest_lunch_collage-1024x575.jpg)A few pictures of lunches during BOSC CoFest 2023, in the ENS gardens.

# Some advances made during CoFest 2023

(Many thanks to Hervé Ménager for keeping track of the projects during the CoFest, and for his warm encouragement during all the preparation for the event!)

## New features added to iCn3D protein viewer

### Proposal

[iCn3D](https://doi.org/10.1093/bioinformatics/btz502) is a web-based 3D structure viewer synchronizing 1D, 2D, and 3D view, _e.g._ [https://www.ncbi.nlm.nih.gov/Structure/icn3d/?mmdbid=1TUP&showanno=1&show2d=1](https://www.ncbi.nlm.nih.gov/Structure/icn3d/?mmdbid=1TUP&showanno=1&show2d=1). The 1D sequence view shows all kinds of annotations ( _e.g._ domains, SNPs, etc) in tracks. This project will show the start and end positions of exons in the sequence, and show the sequence of isoforms of the protein and their exons. Thus users can clearly see the exon skipping and potentially relate the exon skipping to the protein functions.

### What was done

During the CoFest, the [iCn3D viewer](https://www.ncbi.nlm.nih.gov/Structure/icn3d/) got a new feature to show isoforms and exons as tracks with the button "Add Track" in the "Sequences & Annotations" window via the menu "Analysis > Sequences & Annotations". One example is at [https://structure.ncbi.nlm.nih.gov/icn3d/share.html?pA3pPu7LxdiuZDVX7](https://structure.ncbi.nlm.nih.gov/icn3d/share.html?pA3pPu7LxdiuZDVX7):

![](https://lh6.googleusercontent.com/dA1--0Lbv64qwvLSA5dgZmrns9Wbm8yZqRrLWEIiRUiJqn0QgEcKZXXNnY_ScF2taDziqInDVv2u0eHgZuUs5ElMOb8STzZePrJbY0shxpo-a1EFfiAMQbGOOAtyWo_KIN9Ov7ZXGhQBGt5icf2wBFQ)

Users can also predict structures from sequences using ESMFold directly in iCn3D via the menu "File > Predict by Seq. > ESMFold". Other features of iCn3D are listed in its GitHub page: [https://github.com/ncbi/icn3d](https://github.com/ncbi/icn3d).

![](/wp-content/uploads/2023/09/9780596002992_internet_w290.jpg)The BLAST book from 2003 (cover).

## Updating the BLAST book

### Proposal

The [BLAST book](https://www.oreilly.com/library/view/blast/0596002998/), by Ian Korf, was published in 2003. It provides a lot of "recipes" for Blast searches in different contexts. Since then, however, the syntax of most tools from the Blast suite has changed, with the introduction of Blast+ in 2009. The wrapper currently distributed with Blast+ to convert the old syntax (blastall) has quite limited features. My idea is to update the command examples in the book to the new syntax, explain new options, and identify places that need more in-depth updating.

The main author, [Ian Korf](http://korflab.ucdavis.edu/Bios/bio_ian.html), had been contacted in advance: he's not against a new book about Blast, but he doesn't want to be involved. Two hard copies of Korf’s book will be available during CoFest.

### What was done

- Scoping discussion on Slack (when should we contact the original publisher?),
- Side-by-side option table ( _old_ vs _new_ options),
- Practical testing of old examples from the book using the new syntax.

### Future work

- Write down the updated examples as a [web page](https://github.com/jejust/blast_book_plus),
- Contact O’Reilly, the publisher of the book, and see if they are interested in a new edition. In any case, the updated examples will be available to the community on a webpage (GitHub or better).

[![](/wp-content/uploads/2023/09/biopython_logo_s.png)](https://biopython.org/)

## Progress on various Biopython projects

### Proposal

Peter Cock will be attending remotely, but as one of the regular Biopython contributors will try to match any newcomers with suitable projects/issues. He hopes to work on migrating the [Tutorial documentation](http://biopython.org/DIST/docs/tutorial/Tutorial.html) from LaTeX to RST to simplify and automate it for each release (see [PR 4371](https://github.com/biopython/biopython/pull/4371)). See the #cofest-biopython channel on [BOSC Slack](https://join.slack.com/t/obf-bosc/shared_invite/zt-n5ur1gsj-z2C~69_4lYTFPg5tbWA8Ew).

### What was done

- Progress on LaTeX to RST/Sphinx conversion of [Tutorial](https://github.com/biopython/biopython/tree/master/Doc) (tables, citations).
- Improvements to a script dealing with big FASTQ files: speed up reads extraction (6x faster).

### Future work

- Try to get the converted Tutorial to build without errors.

### Question to CoFest group

What file format would you prefer for the Tutorial (HTML, PDF, eBook...)?

## MultiK parallelization using **`Future`**

### Proposal

[MultiK](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-021-02445-5) is a R package built upon [Seurat](https://satijalab.org/seurat/) that objectively selects multiple insightful numbers of clusters ( _K_) in a single-cell RNA-seq dataset.

However the main function of the package is very expensive both in computing and in time since it is not parallelized.

The idea would be to attempt to parallelize it using the [Future](https://future.futureverse.org/) package (which is already used by Seurat) in order to speed up scRNA-Seq workflows making use of it.

### What was done

- The first main loop (out of two) was parallelized:
  - works when used locally & remotely on a small dataset,
  - 10x performance for the whole function.

### Future work

- MultiK crashes when processing the whole dataset remotely (“ `Error: Detected a non-exportable reference ('externalptr') used in the future expression`”): we plan to investigate further on that,
- Parallelize the second main loop of MultiK.

## Make installation of Bionano tools easier

### Proposal

[Bionano](https://bionano.com/) is a technology to create optical maps from HMW DNA. One major problem is the lack of tools options for analysis since there are only tools provided by _Bionano Genomics_ : Bionano Access (server and GUI) and Bionano Solve (analysis software).

The [installation of Bionano Solve](https://bionano.com/wp-content/uploads/2023/04/CG-30182_Bionano-Solve-Installation-Guide.pdf) is clumsy : it uses a docker image to install dependencies. My idea is to retrieve all the dependencies used from the docker image to create a bioconda recipe in order to easily install and maintain Bionano Solve software dependencies.

### What was done

- Installation of currently available Bionano docker image,
- Inspection of Bionano tools installation script.

### Future work

- Detailed list of dependencies, starting from Python / R packages and software present in the docker image,
- (Bio)Conda recipe documentation exploration.

## Applications of open source LLMs in bioinformatics

### Proposal

This group aims to explore the applications and promotion of open source large language models (LLMs) in the field of bioinformatics. LLMs have gained popularity, and the community seeks models that offer accessibility and transparency. Strategies for collaboration and community engagement, including the use of shared repositories and benchmarking frameworks, will be discussed. Ethical considerations such as data privacy, bias, and interpretability will also be explored.

**Sharing resources and ideas:**

[https://docs.google.com/document/d/1fxA3JCtPkScm7vXSFQqPJtgP6OEZgAwN7-o\_pKtoH5c/edit?usp=sharing](https://docs.google.com/document/d/1fxA3JCtPkScm7vXSFQqPJtgP6OEZgAwN7-o_pKtoH5c/edit?usp=sharing)

### What was done

- Shared documentation to collect ideas and useful links:
  - Tips for choosing/testing open source LLMs,
  - Some ideas for applications and benchmarking of the models.

### Future work

- Summarize the document and merge it into the paper being prepared by the LLM group from [BioHackathon Japan](https://2023.biohackathon.org/) that will be submitted to [BioHackrXiv](http://preview.biohackrxiv.org/) :
  - [BioHackJP 2023](https://biohackrxiv.org/discover?q=BioHackJP%202023).

## FAIR Biomedical Research Software (FAIR-BioRS)

### Proposal

Most would agree that making biomedical research software (code, scripts, desktop software, Jupyter Notebooks, etc.) reusable is essential to prevent duplicate effort, enable building on top of existing work, and ultimately increase the pace of discoveries and innovations for improving human health. The question then is, how do we make biomedical research software reusable? The Findable, Accessible, Interoperable, and Reusable principles for Research Software (or [FAIR4RS principles](https://doi.org/10.1038/s41597-022-01710-x)) published in 2022 provide high-level instructions to achieve that. It is the result of a large-scale effort and is backed by a large community of research software developers. However, just like the original FAIR principles, the FAIR4RS principles remain aspirational and do not provide clear actionable instructions. To address this, we have established the FAIR Biomedical Research Software (FAIR-BioRS) guidelines, that provide clear, actionable step-by-step instructions for making biomedical research software reusable in line with the FAIR4RS principles. Our idea here is to discuss the current version (v2.0.0) of the FAIR-BioRS guidelines, identify if/how they can be improved, brainstorm on how they can be maintained going forward, etc. so as a community we can start adhering consistently with the FAIR4RS principles to make our software reusable and also provide clear guidelines to do so especially for the next generation of biomedical software developers.

### What was done

- Worked with some attendees to explore how the [guidelines](https://github.com/FAIR-BioRS/Code) would apply to their project,
- Scope discussion, and at least one pull request merged,
- Notes from discussion available at [https://etherpad.osuosl.org/p/Cofest2023-fair-BioRS](https://etherpad.osuosl.org/p/Cofest2023-fair-BioRS),
- Discussion to wrap up on the paper and plan for future outreach/communication effort.

**That’s the second CoFest edition this project is worked on (already in 2022), and its outcome is now published in a peer-reviewed paper:**

_Making Biomedical Research Software FAIR: Actionable Step-by-step Guidelines with a User-support Tool_. Bhavesh Patel, Sanjay Soundarajan, Hervé Ménager and Zicheng Hu, _Scientific Data_ **10**:557 (2023). [doi:10.1038/s41597-023-02463-x](https://doi.org/10.1038/s41597-023-02463-x)

### Future work

- Outreach/communication effort.

### Question to CoFest group

- Would you use the guidelines to make your research software reusable? If not, why, how can they be improved?

[![](/wp-content/uploads/2023/09/CWL-Logo-HD-2-1024x654.png)](https://www.commonwl.org/)

## Next release of Common Workflow Language

### Proposal

108 proposed clarifications to the [_Common Workflow Language_](https://www.commonwl.org/) _v1.2 standards_ need summarizing before release v1.2.1.

### What was done

- All done!

**See:**

- [Introduction to the CWL Command Line Tool draft standard v1.2.1](https://deploy-preview-262--cwl-v1-2-dev.netlify.app/commandlinetool#Introduction_to_the_CWL_Command_Line_Tool_draft_standard_v1.2.1),
- [Changelog\_for\_v1.2.1](https://deploy-preview-262--cwl-v1-2-dev.netlify.app/workflow#Changelog_for_v1.2.1).

### Future work

- Get these changes reviewed & merged.

### Questions to CoFest group

- [Reviews](https://github.com/common-workflow-language/cwl-v1.2/pull/262/files) are very welcome! (Especially by those with CWL experience)

## SPARQL WR RO-Crate queries

### What was done

- Made [SPARQL queries](https://github.com/RenskeW/runcrate-analysis/tree/main/test-prov) to answer provenance questions from `ro-crate-manifest.json`.

### Future work

- Add more queries to the list.

### Question to CoFest group

- How to use SPARQL queries as unit tests?

## WfExS-backend changes to support **`envvars`** and get conformant to Workflow Run RO-Crate 0.2

### What was done

- Added support to describe environment variables needed by a workflow execution.
- Integrated used environment variables as inputs in Workflow Run RO-Crate, using FormalParameter. There is no standard way to signal which FormalParameters are a traditional workflow parameter and which are environment variables (besides the id).
- _(partially implemented)_ Output files and directories are not using an nih URI any more.
- _(work in progress)_ Better representation of CWL workflow dependencies, so the usage of an external ontology does not appear as a "hard" dependency itself.

# Our sponsors

We are grateful to all the sponsors who allowed us to host the BOSC CoFest 2023 in Lyon in excellent conditions and made it so successful:

[![](/wp-content/uploads/2023/09/IXXI_Logo.png)](https://www.ixxi.fr/)[Complex Systems Institute Rhône-Alpes](https://www.ixxi.fr/)[![](/wp-content/uploads/2023/06/ens_logo.png)](http://www.ens-lyon.fr/)[École normale supérieure de Lyon](http://www.ens-lyon.fr)[![](/wp-content/uploads/2023/06/ens_rdp_logo.jpeg)](http://www.ens-lyon.fr/RDP/)[Laboratoire Reproduction et développement des plantes](http://www.ens-lyon.fr/RDP/)[![](/wp-content/uploads/2023/09/IFB-HAUT-COULEUR-GRAND.png)](https://www.france-bioinformatique.fr/en/)[French Institute for Bioinformatics](https://www.france-bioinformatique.fr/en/)

We would also like to apologize to all our colleagues who would have liked to attend but had holiday date constraints this summer. Keep updated for next editions!

## Our suppliers

All the catering was purchased from local providers and carried by bike. They will probably not deliver abroad, but if you pass by Lyon and feel hungry, you can for sure trust them:

- Main caterer for lunches: [Cyril Nitard](https://www.cyril-nitard.com/),
- Baker: boulangerie [Ondo-Vernin](https://www.leprogres.fr/economie/2022/07/15/la-boulangerie-patisserie-ondo-vernin-une-affaire-de-famille),
- Cheese-seller: fromagerie [Les Trois Jean](https://www.fromagerielestroisjean.com/),
- Fruits and fruit juices: [Cerise et Potiron Monplaisir](https://www.cerise-et-potiron.fr/store/monplaisir/) (have a look [at some creations](https://www.instagram.com/sebgana/)).

We did our best to minimize waste, by using reusable containers for lunches and coffee breaks (including drink bottles, glasses, cups, plates, silverware…).

![](/wp-content/uploads/2023/09/CoFest_baker_delivery-576x1024.jpg)Coffee break

![](/wp-content/uploads/2023/09/CoFest_lunch_table-768x1024.jpg)Happy participants at lunch
