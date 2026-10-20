---
author: "Moaaz Khokhar"
date: 2026-10-03 # format is YYYY-MM-DD
category:
 - community
 - event-fellowship
 - travel-fellowship
cover:
  image: /img/2026/2026-10-03-moaaz-presenting-deepalloweb-eccb-2026.jpeg
  alt: "Moaaz Presenting DeepAlloWeb at ECCB 2026"

tag:
 - community
 - event-fellowship
 - travel-fellowship

title: "Allostery, Protein Language Models, and Open Science: Presenting My Research at ECCB 2026"
url: /2026/10/03/2026-10-03-moaaz-khokhar-eccb-2026/
---

**_The_** [**_Open Bioinformatics Foundation (OBF) Event Fellowship program_**](/travel-awards) **_aims to promote diverse participation at events promoting open-source bioinformatics software development and open science practices in the biological research community. Moaaz Khokhar,_** _**a PhD Candidate at**_ _**Koç University**_, **_was awarded an OBF Event Fellowship to attend_** _**the**_ **_[European Conference on Computational Biology (ECCB 2026)](https://eccb2026.org/)_**.

![Moaaz Presenting DeepAlloWeb at ECCB 2026](/img/2026/2026-10-03-moaaz-presenting-deepalloweb-eccb-2026.jpeg)

I attended the 25th European Conference on Computational Biology in Geneva, held from 31 August to 4 September 2026. I work on predicting allosteric sites in proteins: regions where binding can influence activity elsewhere in the molecule. This makes the relationship between sequence, structure and function a practical problem in my research.

I presented a poster on [DeepAlloWeb](https://pubmed.ncbi.nlm.nih.gov/42155622/), which builds on [DeepAllo](https://pubmed.ncbi.nlm.nih.gov/40372465/) by making allosteric pocket prediction accessible through an interactive web server. The method combines a fine-tuned protein language model, ProtBERT-BFD, with structural pocket features extracted using FPocket. The underlying DeepAllo code is available as open-source software under the GPL-3.0 licence, allowing other researchers to inspect, reuse, and extend the method. Sharing the code alongside an accessible web interface supports the open-science values promoted by OBF and helps researchers build on our work. Presenting this work gave me an opportunity to introduce fellow researchers to a tool that could help them prioritise candidate allosteric pockets for further investigation. I also sought constructive feedback to guide the next version of DeepAlloWeb. Developing the tool has led me towards a broader question that shaped my interests at the conference: how much biological meaning can we assign to a model’s predictions and the residues it highlights?

The [ECCB protein programme](https://transition.iscb.org/cms_addon/conferences/eccb2026/schedule/Proteins) included Ivet Bahar's presentation on [Rhapsody-2](https://pubmed.ncbi.nlm.nih.gov/40314982/), a method for predicting whether amino acid substitutions are pathogenic. It combines evolutionary information with structural, energetic and dynamics descriptors. Its analysis of residues involved in allosteric communication is particularly relevant to the questions I work on. For my research, this gives a useful way to evaluate residue predictions: compare them with measured mutation effects while examining what the experiment actually measures. A mutation can change folding, stability, binding or regulation. Distinguishing those effects matters before treating agreement with a mutation dataset as evidence for an allosteric mechanism.

Samuele Firmani's [RIBEX](https://pubmed.ncbi.nlm.nih.gov/42635213/) presentation addressed RNA-binding prediction by combining protein language model representations with information from a protein interaction network. The study uses computational alanine scanning and ablation of network-derived features to investigate the predictions. It also shows that adapting ESM2-650M with LoRA produced larger improvements on its benchmarks than increasing the size of a frozen model. This connects closely to my interest in reliable explanations for protein models. In allosteric prediction, I want to test whether changing highly ranked residues affects a prediction more than changing suitable control residues. Such a test would examine the model's behaviour; experimental evidence would still be needed to establish biological causation. RIBEX also gives a concrete reason to compare task adaptation with frozen embeddings when choosing a protein representation.

Byung-Jun Yoon's presentation on [PROSOUNDS](https://academic.oup.com/bioinformatics/article/42/Supplement_2/btag436/8767294) examined uncertainty-weighted steering of protein language models. The method uses uncertainty estimates from a surrogate predictor when constructing directions that guide sequence optimization. It addresses the problem of relying on predicted properties when experimental labels are sparse or the target proteins differ from the training data. The connection to my work is the need to handle uncertain evidence explicitly. An unannotated pocket is not necessarily a confirmed negative example of allostery. I am interested in separating experimentally supported allosteric sites, orthosteric sites and uncharacterised pockets when constructing datasets. PROSOUNDS does not solve this annotation problem, but it illustrates why uncertain predictions need to be treated differently from reliable measurements.

Open science is closely connected to these technical questions. The [ELIXIR programme at ECCB](https://eccb2026.org/elixir-programme) included FAIR data, interoperable resources and research software. For a machine learning project, practical reproducibility involves recording the source structures, label evidence, preprocessing steps, model versions and evaluation splits. Those details determine whether another group can reproduce a result or understand why a method fails on a new protein. Developing [DeepAlloWeb](https://3dpath.ku.edu.tr/DeepAllo/) has made accessibility a concrete part of my work. A researcher should be able to inspect predicted pockets and residue-level outputs without first reconstructing the entire software environment. I want future work to make the assumptions behind those outputs equally accessible, including the limits of the training data and the meaning of the scores. The source code is available on [GitHub](https://github.com/MoaazK/deepallo).

As a Pakistani researcher based in Turkey, I value support that makes participation in an international research community more accessible. Sharing methods, documentation and practical examples also matters after the conference, particularly for students entering computational biology from a computer science background.

My priority is to develop opensource allosteric prediction methods that can be examined critically at both the model and biological levels. That means evaluating uncertain labels and testing the sensitivity of explanations.

I thank the Open Bioinformatics Foundation for awarding me the fellowship in support of my participation and research presentation at ECCB 2026.

*Moaaz Ur Rehman Azhar Khokhar*<br>
*PhD researcher at Koç University and KUIS AI Fellow*
