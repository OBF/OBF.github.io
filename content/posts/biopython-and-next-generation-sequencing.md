---
author: peterc
category:
  - biopython
  - code
  - development
  - obf
date: "2009-03-26T16:13:42+00:00"
guid: http://news.open-bio.org/news/?p=284
tag:
  - biopython
title: Biopython and next generation sequencing
url: /2009/03/26/biopython-next-gen-sequencing/

---
Those of you doing next generation sequencing may be pleased to know that the next release of [Biopython](http://www.biopython.org) is expected to include support for reading and writing [FASTQ](http://bioperl.org/wiki/FASTQ_sequence_format) and [QUAL](http://bioperl.org/wiki/Qual_sequence_format) files within our [Bio.SeqIO](http://biopython.org/wiki/SeqIO) interface. These formats are used for traditional Sanger capillary sequencing, and Roche 454 sequencing (Roche provide tools to convert from their binary SFF files) with PHRED quality scores. Solexa/Illumina sequencers produce a FASTQ variant where the quality scores are encoded differently, and this is also supported.

As part of this work, the [SeqRecord](http://biopython.org/wiki/SeqRecord) has a new attribute holding a dictionary of per-letter-annotation (e.g. PHRED quality scores, Solexa quality scores, or for proteins secondary structure predictions), and the SeqRecord object can be sliced to give a new SeqRecord covering just part of the sequence, with the per-letter-annotation cropped to match.

The code is in our [CVS tree](http://biopython.org/wiki/CVS), and [mirrored on github](http://github.com/biopython/biopython/tree/master), so those of you happy to install Biopython from source and help test it can grab the code now, and give it a go - feedback on the development [mailing list](http://biopython.org/wiki/Mailing_lists) please. Alternatively, sit back and await the forthcoming Biopython 1.50 (beta) release, which should allow more widespread testing...

_Update:_ This new functionality was included in [Biopython 1.50](http://news.open-bio.org/news/2009/04/biopython-release-150/ "Biopython 1.50"), including both Sanger standard FASTQ files and the original Solexa/Illumina FASTQ variant using Solexa scores. This did not cover the new FASTQ variant used on Solexa/Illumina 1.3+ but that is now supported in our development code, and will be included in Biopython 1.51. Peter, 2009/06/16
