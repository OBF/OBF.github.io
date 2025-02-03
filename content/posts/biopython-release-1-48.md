---
author: peterc
category:
  - biopython
date: "2008-09-09T10:03:44+00:00"
guid: http://news.open-bio.org/news/?p=175
tag:
  - biopython
title: Biopython release 1.48
url: /2008/09/09/biopython-release-148/

---
We are pleased to announce the release of Biopython 1.48. Some new functionality has been added, a few bugs have been fixed, the documentation has been updated, plus several obsolete modules have been deprecated (or explicitly labelled as obsolete).

The following additional file formats are now supported in [Bio.SeqIO](http://biopython.org/wiki/SeqIO) and [Bio.AlignIO](http://biopython.org/wiki/AlignIO):

- reading and writing "tab" format (simple tab separated)
- writing "nexus" files
- reading "pir" files (NBRF/PIR)
- basic support for writing "genbank" files (GenBank plain text)

This release also fixes some problems reading Clustal alignments (introduced in Biopython 1.46 when consolidating Bio.AlignIO and Bio.Clustalw), and some updates to the Bio.Sequencing parsers.

The SeqRecord and Alignment objects have a new method to get the object as a string in a given file format (handled via Bio.SeqIO and Bio.AlignIO).

Bio.PubMed and the online code in Bio.GenBank are now considered obsolete, and we intend to deprecate them after the next release. For accessing PubMed and GenBank, please use Bio.Entrez instead. Martel and Bio.Mindy are now considered to be obsolete, and are likely to be deprecated and removed in a future release, at which point we will drop the optional dependency on mxTextTools. Bio.Fasta is also considered to be obsolete, please use Bio.SeqIO instead. We do intend to deprecate this module eventually, however, for several years this was the primary FASTA parsing module in Biopython and is likely to be in use in many existing scripts.

In addition a number of other modules have been deprecated, including: Bio.MetaTool, Bio.EUtils, Bio.Saf, Bio.NBRF, and Bio.IntelliGenetics - see the DEPRECATED file for full details.

Source distributions and Windows installers are available from the Biopython website: [biopython.org](http://biopython.org/)

My thanks to all bug reporters, code contributors and others who made this new release possible.

--Peter on behalf of the Biopython developers
