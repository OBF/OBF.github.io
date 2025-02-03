---
author: davidw
category:
  - biopython
  - code
  - community
  - development
  - obf
  - obf-projects
date: "2009-08-17T11:52:03+00:00"
guid: http://news.open-bio.org/news/?p=385
tag:
  - biopython
  - fastq
title: Biopython 1.51 released
url: /2009/08/17/biopython-1-51-released/

---
We are pleased to announce the release of Biopython 1.51.This new stable release enhances [version 1.50](http://news.open-bio.org/news/2009/04/biopython-release-150/ "1.50 announcement") (released in April) by extending the functionality of existing modules, adding a set of application wrappers for popular alignment programs and fixing a number of minor bugs.

In particular, the SeqIO module can now write Genbank files that include features, and deal with FASTQ files created by Illumina 1.3+. Support for this format allows interconversion between FASTQ files using Solexa, Sanger and Ilumina variants using conventions agreed upon with the [BioPerl](http://www.bioperl.org/wiki/Main_Page "BioPerl main page") and [EMBOSS](http://emboss.sourceforge.net/ "EMBOSS page") projects.

Biopython 1.51 is the first stable release to include the Align.Applications module which allows users to define command line wrappers for popular alignment programs including [ClustalW](http://www.clustal.org/ "Clustal Hompage"), [Muscle](http://www.drive5.com/muscle/ "Muscle homepage") and [T-Coffee](//www.tcoffee.org/Projects_home_page/t_coffee_home_page.html "T-Coffe Hompage").

Bio.Fasta and the application tools ApplicationResult and generic\_run() have been marked as [deprecated](http://biopython.org/wiki/Deprecation_policy "Deprecation Policy") \- Bio.Fasta has been superseded by SeqIO's support for the Fasta format and we provide ducumentation for using the [subprocess](http://docs.python.org/library/subprocess.html "subprocess documentation") module from the Python Standard Library as a more flexible approach to calling applications.

As always the [Tutorial and Cookbook](http://www.biopython.org/DIST/docs/tutorial/Tutorial.html "Biopython Tutorial") has been updated to document all the changes.

Thank you to everyone who tested our 1.51 beta or submitted bugs since out last stable release and to all our contributors

Sources and Windows Installer are available from the [downloads page](http://biopython.org/wiki/Download "Biopython Downloads").
