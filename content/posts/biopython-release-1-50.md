---
author: peterc
category:
  - biopython
  - community
  - development
  - obf
  - obf-projects
date: "2009-04-20T18:58:05+00:00"
guid: http://news.open-bio.org/news/?p=320
tag:
  - biopython
title: Biopython release 1.50
url: /2009/04/20/biopython-release-150/

---
We are pleased to announce Biopython release 1.50, featuring some significant additions since [Biopython 1.49](http://news.open-bio.org/news/2008/09/biopython-release-148/) was released late last year.

[GenomeDiagram](http://bioinf.scri.ac.uk/lp/programs.php#genomediagram) by Leighton Pritchard has been integrated into Biopython as the Bio.Graphics.GenomeDiagram module.

A new module Bio.Motif has been added, which is intended to replace the existing Bio.AlignAce and Bio.MEME modules. Also have a look at Bio.SwissProt and Bio.ExPASy and their revised parsers.

As noted in a previous news posting, [Bio.SeqIO](http://biopython.org/wiki/SeqIO) can now read and write [FASTQ and QUAL files](http://news.open-bio.org/news/2009/03/biopython-next-gen-sequencing/) used in second generation sequencing work. In connection with this, our [SeqRecord](http://biopython.org/wiki/SeqRecord) object has a new dictionary attribute, letter\_annotations, for per-letter-annotation information like sequence quality scores or secondary structure predictions. Also, the SeqRecord object can now be sliced to give a new SeqRecord covering just part of the sequence.

Biopython 1.50 supports Python 2.3, 2.4, 2.5 and 2.6. However, this is expected to be the final version to support Python 2.3 (see this [previous announcement](http://news.open-bio.org/news/2009/04/2008/11/biopython-and-python-26-and-python-23/)). Also, Biopython 1.50 should be the last release to include our old deprecated parsing infrastructure (Martel and Bio.Mindy).

We’ve also updated the [Biopython Tutorial and Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html "Biopython Tutorial and Cookbook (HTML)") (also available in [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf "Biopython Tutorial and Cookbook (PDF)")), and not just by adding [our logo](http://biopython.org/wiki/Logo "About the Biopython logo") to the cover ;)

Thank you to everyone who tested the [Biopython 1.50 beta release](http://news.open-bio.org/news/2009/04/biopython-150-beta-released/), and to all our contributors.

Source distributions and Windows installers are available from the [downloads](http://biopython.org/wiki/Download) page on the [Biopython website (biopython.org)](http://biopython.org/).

-Peter, on behalf of the Biopython developers
