---
author: dag
category:
  - biopython
  - general
  - obf-projects
date: "2003-07-28T02:33:36+00:00"
guid: http://news.open-bio.org/news/?p=109
tag:
  - biopython
title: BioPython 1.2.0 released
url: /2003/07/27/biopython-120-released/

---
Available now at [http://biopython.org/download/](http://biopython.org/download/)

Changes include:
added Andrew Dalke's EUtils library
added Michiel de Hoon's gene expression analysis package
updates to setup code, now smarter about dependencies
updates to test suite, now smarter about code that is imported
Michael Hoffman's fixes to DocSQL
syntax fixes in triemodule.c to compile on SGI, Python 2.1 compatible
updates in NCBIStandalone, short query error
Sebastian Bassi submitted code to calculate LCC complexity
Greg Kettler's NCBIStandalone fix for long query lengths
slew of miscellaneous fixes from George Paci
miscellaneous cleanups and updates from Andreas Kuntzagk
Peter Bienstman's fixes to Genbank code -- now parses whole database
Kayte Lindner's LocusLink package
miscellaneous speedups and code cleanup in ParserSupport by Brad Chapman
miscellaneous BLAST fixes and updates
Iddo added new code to parse BLAST table output format
Karl Diedrich's patch to read T\_Coffee files
Larry Heisler's fix for primer3 output
Bio.Medline now uses proper iterator objects
copen now handles SIGTERM correctly
small bugfixes and updates in Thomas Hamelryck's PDB package
bugfixes and updates to SeqIO.FASTA reader
updates to Registry system, conforms to 2003 hackathon OBDA spec
Yu Huang patch to support tblastn in wublast expression
