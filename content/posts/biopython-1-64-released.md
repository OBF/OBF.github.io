---
author: tiago
category:
  - biopython
  - code
  - community
  - development
  - obf-projects
date: "2014-05-29T13:55:23+00:00"
guid: http://news.open-bio.org/news/?p=1179
tag:
  - biopython
  - code
  - community
  - development
  - obf-projects
  - open-source
title: Biopython 1.64 released
url: /2014/05/29/biopython-1-64-released/

---
Source distributions and Windows installers for **Biopython 1.64** are now available from the [downloads page](http://biopython.org/wiki/Download "Biopython Downloads") on the [official Biopython website](http://biopython.org/ "Biopython website") and from the [Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython).

This release of Biopython supports Python 2.6 and 2.7, 3.3 and also the new 3.4 version. It is also tested on PyPy 2.0 to 2.3, and Jython 2.7b2.

The new experimental module Bio.CodonAlign facilitates building codon alignment and further analysis upon it. This work is from the Google Summer of Code (GSoC) project by Zheng Ruan.

Bio.Phylo now has tree construction and consensus modules, from on the GSoC work by Yanbo Ye.

Bio.Entrez will now automatically download and cache new NCBI DTD files for XML parsing under the user's home directory (using _~/.biopython_ on Unix like systems, and _$APPDATA/biopython_ on Windows).

Bio.Sequencing.Applications now includes a wrapper for the samtools command line tool.

Bio.PopGen.SimCoal now also supports fastsimcoal.

SearchIO hmmer3-text, hmmer3-tab, and hmmer3-domtab now support output from hmmer3.1b1.

BioSQL can now use the mysql-connector package (available for Python 2, 3 and PyPy) as an alternative to MySQLdb (Python 2 only) to connect to a MySQL database.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Chunlei Wu (first contribution)
- Edward Liaw (first contribution)
- Eric Talevich
- Leighton Pritchard
- Manlio Calvi (first contribution)
- Markus Piotrowski (first contribution)
- Melissa Gymrek (first contribution)
- Michiel de Hoon
- Nigel Delaney (first contribution)
- Peter Cock
- Saket Choudhary
- Tiago Antao
- Vincent Davis (first contribution)
- Wibowo 'Bow' Arindrarto
- Yanbo Ye (first contribution)
- Zheng Ruan (first contribution)
