---
author: brad
category:
  - biopython
  - code
  - development
  - obf
  - obf-projects
date: "2011-04-02T12:17:44+00:00"
guid: http://news.open-bio.org/news/?p=811
tag:
  - biopython
  - development
  - release
title: Biopython 1.57 released
url: /2011/04/02/biopython-1-57-released/

---
The Biopython community is pleased to announce the release of Biopython 1.57. Source distributions and Windows installers are available from the [downloads page](http://www.biopython.org/wiki/Download) on the [Biopython website](http://www.biopython.org) and from the [Python Package Index.](http://pypi.python.org/pypi/biopython)

Bio.SeqIO now includes an index\_db() function which extends the existing
indexing functionality to allow indexing many files, and more importantly
this keeps the index on disk in a simple SQLite3 database rather than in
memory in a Python dictionary.

Bio.Blast.Applications now includes a wrapper for the BLAST+ blast\_formatter
tool from NCBI BLAST 2.2.24+ or later. This release of BLAST+ added the
ability to run the BLAST tools and save the output as ASN.1 format, and then
convert this to any other supported BLAST ouput format (plain text, tabular,
XML, or HTML) with the blast\_formatter tool. The wrappers were also updated
to include new arguments added in BLAST 2.2.25+ such as -db\_hard\_mask.

The SeqRecord object now has a reverse\_complement method (similar to that of
the Seq object). This is most useful to reversing per-letter-annotation (such
as quality scores from FASTQ) or features (such as annotation from GenBank).

Bio.SeqIO.write's QUAL output has been sped up, and Bio.SeqIO.convert now
uses an optimised routine for FASTQ to QUAL making this much faster.

Biopython can now be installed with pip. Thanks to David Koppstein and
James Casbon for reporting the problem.

Bio.SeqIO.write now uses lower case for the sequence for GenBank, EMBL and
IMGT output.

The Bio.PDB module received several fixes and improvements, including starting
to merge João's work from GSoC 2010; consequently Atom objects now know
their element type and IUPAC mass. (The new features that use these
attributes won't be included in Biopython until the next release, though, so
stay tuned.)

The nodetype hierachy in the Bio.SCOP.Cla.Record class is now a dictionary
(previously it was a list of key,value tuples) to better match the standard.

Many thanks to the Biopython developers and community for making this release
possible, especially the following contributors:

- Brad Chapman
- Eric Talevich
- Erick Matsen (first contribution)
- Hongbo Zhu
- Jeffrey Finkelstein (first contribution)
- Joanna & Dominik Kasprzak (first contribution)
- Joao Rodrigues
- Kristian Rother
- Leighton Pritchard
- Michiel de Hoon
- Peter Cock
- Peter Thorpe (first contribution)
- Phillip Garland
- Walter Gillett (first contribution)

Feedback is most welcome on the [mailing lists](http://biopython.org/wiki/Mailing_lists), or [redmine](http://redmine.open-bio.org/projects/biopython).
