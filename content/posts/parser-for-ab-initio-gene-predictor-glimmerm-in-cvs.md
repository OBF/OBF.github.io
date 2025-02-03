---
author: dag
category:
  - bioperl
date: "2003-05-23T23:55:21+00:00"
guid: http://news.open-bio.org/news/?p=92
title: parser for ab initio gene predictor GlimmerM  in  CVS
url: /2003/05/23/parser-for-ab-initio-gene-predictor-glimmerm-in-cvs/

---
Jason writes:

I've added a parser for the ab initio gene predictor GlimmerM in
Bio::Tools::Glimmer. Tests are added to t/Genpred.t now.

It follows the Bio::Tools::AnalysisParser interface which support the
next\_prediction call and returns a Bio::Tools::Prediction::Gene object in
the same way as Genscan.

I also have some scripts for building the training set file so you can run
Glimmer on other species. There is also a similar script for building
custom splice sites file for Genewise which I'll commit soon. Basically
it takes as input a GFF file which has exons annotated (typically from
Sim4/Exonerate alignments of cDNA to DNA) and a reference to the genomic
DNA db (typically just a flatfile which we index with Bio::DB::Flat).

Not sure where to put these - scripts/gene\_prediction ?
