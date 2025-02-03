---
author: davidw
category:
  - biopython
  - code
  - development
  - obf-projects
date: "2009-09-22T16:26:00+00:00"
guid: http://news.open-bio.org/news/?p=410
tag:
  - biopython
title: Biopython 1.52 released
url: /2009/09/22/biopython-release-152/

---
We are pleased to announce the availability of Biopython 1.52, a new stable release of the [Biopython](http://biopython.org) library.

It may only have been one month since [the last release](http://news.open-bio.org/news/2009/08/biopython-1-51-released/ "Biopython 1.51"), but in that time we've added enough useful features to warrant a new release. In particular, Biopython 1.52 includes more substantial support for population genetics, and adds new functions that will be useful for people working with next generation sequencing.

Tiago Antao's work on the Population Genetics module brings a command line wrapper for GenePop which allows the estimation of [F-statistics](http://en.wikipedia.org/wiki/F-statistics), null allele frequencies and migration rates as well as tests for isolation by distance (IBD) and deviation from Hardy-Weinberg equilibrium.

Bio.SeqIO and Bio.AlignIO both now have a [new **convert()** function](http://news.open-bio.org/news/2009/09/biopython-convert-function/) that allows for simple (and potentially optimized) conversion between file formats. Bio.SeqIO also gets a [new **index()** function](http://news.open-bio.org/news/2009/09/biopython-seqio-index/ "Indexing sequence files with Biopython") which allows random access to sequences in a file without reading every record in that file into memory.

The new release also adds command line wrappers for the [EMBOSS versions](http://emboss.sourceforge.net/embassy/#PHYLIP "Emboss Embassy packages") of the [PHYLIP phylogeny programs](http://evolution.genetics.washington.edu/phylip.html "Joe Felsenstein's Phylip page") and the [Novoalign assembler from NovaCraft](http://www.novocraft.com/products.html#novoalign) \- plus squashes a few minor bugs reported since 1.51 was released.

Biopython 1.52 will be the last release to use the CVS server as the main repository for code in development. From now on the [official development branch will be on github](http://github.com/biopython/biopython "Biopython on github"), would-be developers can see our wiki page on [git usage](http://www.biopython.org/wiki/GitUsage "Biopython wiki article on git usage") to see the benefits on this system.

Sources and Windows Installers are available from the [downloads page](http://www.biopython.org/wiki/Download "Download Biopython").

Thanks to the Biopython development team and to everyone who has reported bugs since our last release.
