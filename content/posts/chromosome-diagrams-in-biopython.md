---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - documentation
  - howto
  - obf
  - obf-projects
date: "2011-10-28T15:44:10+00:00"
guid: http://news.open-bio.org/news/?p=855
tag:
  - biopython
title: Chromosome Diagrams in Biopython
url: /2011/10/28/chromosome-diagrams-in-biopython/

---
One of the new things coming in Biopython 1.59 is improved chromosome diagrams, something you may have seen [via Twitter](http://twitter.com/#!/pjacock/status/121676973054496768). I've just been updating the Biopython Tutorial (current version [here](http://biopython.org/DIST/docs/tutorial/Tutorial.html), [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)) to include an example drawing this:

![tRNA genes in Arabidopsis thaliana](https://github.com/biopython/biopython/raw/1574d8112914ea147f4e62c6b980543db1abdc7d/Doc/images/tRNA_chrom.png)

Here's a [PDF version](https://github.com/biopython/biopython/raw/1574d8112914ea147f4e62c6b980543db1abdc7d/Doc/images/tRNA_chrom.pdf) too. This example just parses the _Arabidopsis thaliana_ GenBank files to get the chromosome lengths and the tRNA gene placements. There are so many tRNA on the forward strand of Chr I that their labels are forced to overlap. Here the figure just uses a different color for each chromosome, but you can color each feature individually.

This kind of diagram is often used for showing the placement of SNPs or other loci of interest (e.g. disease or breeding markers).

P.S. Biopython produces these and other graphics using [ReportLab](http://www.reportlab.com/software/opensource/), an open source Python library capable of outputting PDF, SVG, PNG, etc. Very handy.
