---
author: Disha Tandon
date: 2026-09-30

category:
 - community
 - event-fellowship
 - travel-fellowship

cover:
  image: /img/2026/2026-09-30-DishaTandon-nfdi4LS-IB2026-Individual.jpg
  alt: "Disha Tandon presenting at nfdi4ls-IB2026"

tag:
 - community
 - event-fellowship
 - travel-fellowship

title: "A Window into the World of Research Data Management"
url: /2026/09/30/2026-09-30-Disha-Tandon-nfdi4ls-IB/
---

**_The_** [**_Open Bioinformatics Foundation (OBF) Event Fellowship program_**](/travel-awards) **_aims to promote diverse participation at events promoting open-source bioinformatics software development and open science practices in the biological research community. Disha Tandon,_** _**an ARISE2 fellow at EMBL-EBI, UK**_, **_was awarded an OBF Event Fellowship to attend_** _**the**_ **_[NFDI4LS-Integrative Bioinformatics conference](https://meetings.ipk-gatersleben.de/nfdi4LS-IB2026)_**.

![nfdi4ls-IB2026-individual](/img/2026/2026-09-30-DishaTandon-nfdi4LS-IB2026-Individual.jpg)
*CC-BY-SA Mary-Ann Ebeling*

Recently I attended the Nationale Forchungsdaten Infrastuktur for Life Sciences (NFDI4LS) - Integrative Bioinformatics conference organised at the Leibniz-Institut für Pflanzengenetik und Kulturpflanzenforschung (IPK) in Gatersleben, Germany. Thanks to the Open Bioinformatics Foundation's Event Award, I got to take my work beyond my desk and share it with a diverse community active in research data management.

On the first day, filled with mixed thoughts, I stepped into the hall. Since the time I submitted my abstract, I knew that the topics covered in the conference could be out of my comfort zone, even if my work was relevant to the theme. My entry in microbiology was serendipity, a chance encounter that made it 'my field'. But my work on organizing biodiversity data into knowledge graphs was a deliberate action, a choice that brought me to present that work at this event.

The conference theme was structured around techniques of developing and managing research data and metadata in life sciences. I presented my work on managing biodiversity data. Have a look at the slides [here](https://doi.org/10.5281/zenodo.22288161). Taking plants as an example, in this work, we have shown a proof-of-concept of how multi-faceted data like traits, interactions and metabolites as well as corresponding metadata (location, bibliography, etc) can be integrated in a knowledge graph ([METRIN-KG](https://doi.org/10.1093/gigascience/giag051)) through a linked data format following a custom [ontology](https://w3id.org/emi). The latter comprises shared ontologies describing metadata, life sciences domain-specific vocabularies, and around 100 new entities and terms describing metabolite data. This work is part of the [Earth Metabolome Initiative](https://www.earthmetabolome.org/) (EMI), which aims to profile the metabolome of all known species on planet Earth. A massive undertaking, EMI brings together researchers from diverse backgrounds to bring this ambitious project to fruition.

## Expansive realm of research data management

To the readers of this blog, I guess it is no surprise that biology, even before the AI era, has been swimming in data, from the grassroots level of protocols scribbled in experimental biologists' lab notebooks, to manicured datasets prepared for journal submission. Only a fraction of this ever makes it into dedicated repositories. It is fitting then, that the talks at this conference were pointed at how to capture and organize such data, and how to manage the quality of both extraction workflows and the extracted data.

While this short write-up is not enough to comment on all talks, I want to highlight an insightful session on "Applied RDM, Curation, and Metadata Tooling." Stephanie Jurburg delivered a keynote on MiCoDa, a resource that captures microbiome data into standardized forms for large-scale analysis. She spoke about how we think of omics data in microbiology: it is not enough to preserve it, it has to be standardized for researchers to actually use. Even in the era of AI, the value of human curation came through clearly in the presentation.

![nfdi4ls-IB2026-gruppe](/img/2026/2026-09-30-DishaTandon-nfdi4LS-IB2026-Gruppe-JHimpe.jpg)
*IPK Leibniz Institute/J. Himpe*

Next was a talk by Eva Eleonora Ferradosa on the pain points researchers hit during metadata documentation. It shed light on why a pre-emptive approach to documentation is burdensome, and therefore perceived as unnecessary. Having spent part of my research career in a microbiology lab, this one hit home. Metadata recording was an essential task in my workflow, even though whether or how it would be reused downstream was an open question at the time. It only became clearer later, once I started piecing the data back together for my thesis.

The next talk by Kevin Schneider covered curating metadata as a version-controlled FAIR digital object, capturing metadata at the source of experiments rather than relying on downstream curation. My current research lies at the downstream end of this process, which made me realize how remarkable it would be if this data were captured at the start, as early as manuscript submission.

The last talk by Wolfgang Müller in the session introduced spreadsheets designed to capture metadata systematically, built on the OpenRefine framework. I found it especially useful in the context of supplementary data, an area long overlooked in legacy research data management. In my current work I run into supplementary files reported in every conceivable format: nested tables, non-interoperable structures, you name it. At the reporters' end, this might be their creativity singing at its best. At the curators' end, those beautiful songs are usually lost in the cacophony of the jungle full of supplementary files. The OpenRefine framework offered a way to manage that cacophony in a sane manner.

Beyond this session, the conference offered plenty more worth noting. Maria Meister proposed a quality management framework for research services. Sarah Oranna Fischer-Zielke talked about metadata standards for animal research. Ata Ul Haleem showed how to measure just how FAIR a repository really is. Aaruni Kaushik talked about MaRDI, a packaging system that's easy to implement and use, requiring less training than some of the bigger players in the field. Ayorinde Afolayan showed how the Type Strain Genome Server is used by several researchers for genome-based prokaryote taxonomy. Keywan Hassani-Pak's intriguing talk explored hypothesis generation from knowledge graphs with the aid of AI agents. The keynote by Paul Shaw introduced dedicated software for streamlining in-field data collection in plant sciences. All these talks offered a piece of research data management at various levels of sample and data collection, analysis and integration.

As part of the conference, the participants got a chance to visit some of IPK's facilities. I visited the PhenoSphere facility, where plants grow under strictly controlled environmental conditions (light, temperature, humidity, CO2 concentration, irrigation). It was an informative experience to know how the PhenoSphere facilitated study of a rhizotron system, where the roots are imaged via a monochrome camera and shoots through a high-resolution RGB camera. Some of the videos showing root growth under control versus treatment conditions were a delight to watch, as visually striking as they were informative. Visiting the experimental facilities outside my specialization was a refreshing experience.

## Food for thought

Throughout the conference, there were several talks aimed at reducing the costs and the human effort in constructing FAIR knowledge graphs. This led me to think about how much we should really rely on AI to do the hard work for us. Is it all about reducing the effort, and thereby the costs? If the goal is cutting effort and cost, then slop might be an obvious outcome of it. Historically, humans have organized work around keeping people employed, and thus efforts are tied to jobs. However, AI risks undoing that, automating away the very effort that gave people a place in the process.

And in this context, I must mention the most interesting keynote from Sabina Leonelli, where she talked about the mechanisms of the structure of scientific knowledge and its broader implications for society. Building on her work on environmental intelligence, she talked about how human agency shouldn't be removed, rather it should guide AI-assisted data management and analysis. While a lot has been said by others about AI-assistance in human agency, this keynote brought a refreshing take. A term that she mentioned is probably going to stay with me - 'Convenience AI'. What I initially made of this term was AI developed for reducing human efforts, where doing so may not offer major benefit, not just to humans, but also the machinery that keeps them going, including all entities on earth. Sabina Leonelli, however, compared Convenience AI to Environmental Intelligence in the context of intelligence embodiment and generalizability, relevance beyond evidence and human agency in decision-making. Until now, we all had a role in promoting convenience AI, but how should we collectively move towards environmental intelligence. Not a topic for this blog, but an endless food for thought!
