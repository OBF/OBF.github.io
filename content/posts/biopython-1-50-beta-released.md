---
author: peterc
category:
  - biopython
  - community
  - development
  - obf-projects
date: "2009-04-03T21:08:59+00:00"
guid: http://news.open-bio.org/news/?p=308
tag:
  - biopython
title: Biopython 1.50 beta released
url: /2009/04/03/biopython-150-beta-released/

---
We are pleased to announce a beta release of Biopython 1.50 for public testing. There have been some significant changes since [Biopython 1.49](http://news.open-bio.org/news/2008/11/biopython-release-149/) was released late last year.

[GenomeDiagram](http://bioinf.scri.ac.uk/lp/programs.php#genomediagram) by Leighton Pritchard has been integrated into Biopython as the Bio.Graphics.GenomeDiagram module.

A new module Bio.Motif has been added, which is intended to replace the existing Bio.AlignAce and Bio.MEME modules. Also have a look at Bio.ExPASy and the revised Prosite and Enzyme parsers.

As noted in a previous news posting, [Bio.SeqIO](http://biopython.org/wiki/SeqIO) can now read and write [FASTQ and QUAL files](http://news.open-bio.org/news/2009/03/biopython-next-gen-sequencing/) used in second generation sequencing work. In connection with this, our [SeqRecord](http://biopython.org/wiki/SeqRecord) object has a new dictionary attribute, letter\_annotations, for per-letter-annotation information like sequence quality scores or secondary structure predictions. Also, the SeqRecord object can now be sliced to give a new SeqRecord covering just part of the sequence.

As in the previous release, Biopython 1.50 beta supports Python 2.3, 2.4, 2.5 and 2.6. However, Biopython 1.50 is expected to be the final version to support Python 2.3 (see this [previous announcement](../2008/11/biopython-and-python-26-and-python-23/)). Also, Biopython 1.50 should be the last release to include our old deprecated parsing infrastructure (Martel and Bio.Mindy).

So, if you are feeling brave, please try out Biopython 1.50 beta, and let us know on the [mailing lists](http://www.biopython.org/wiki/Mailing_lists) if it works, or more importantly if something doesn’t. Comments on the new code are particularly welcome.

We’d also like feedback on the updated [Biopython Tutorial and Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html) (also available in [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)).

Source distributions and Windows installers are available from the Biopython website: [biopython.org](http://biopython.org/).

Thanks!

-Peter on behalf of the Biopython developers
