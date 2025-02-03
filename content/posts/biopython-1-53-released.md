---
author: peterc
category:
  - biopython
  - code
  - development
  - obda-/-biosql
  - obf-projects
date: "2009-12-15T16:57:53+00:00"
guid: http://news.open-bio.org/news/?p=555
tag:
  - biopython
title: Biopython 1.53 released
url: /2009/12/15/biopython-release-153/

---
We are pleased to announce the availability of Biopython 1.53, a new stable release of the Biopython library, three months after the release of [Biopython 1.52](http://news.open-bio.org/news/2009/09/biopython-release-152/). This is our first release since [migrating from CVS to git](http://news.open-bio.org/news/2009/09/biopython-cvs-to-git-migration/) for source code control.

There have been some additions to our core objects - the [Seq](http://biopython.org/wiki/Seq) (and related UnknownSeq) objects gained upper and lower methods (like the string methods of the same name but alphabet aware) plus a new ungap method. The SeqFeature object now has an extract method to get the region of sequence it describes (useful for getting CDS nucleotide sequences from GenBank files). Also [SeqRecord](http://biopython.org/wiki/SeqRecord) objects now support addition, giving a new SeqRecord with the combined sequence, all the SeqFeatures, and any common annotation.

SQLite support (built into Python 2.5+) was added to our [BioSQL interface](http://biopython.org/wiki/BioSQL) (Brad Chapman). This is still a little experimental as we are using a draft BioSQL SQLite schema, but this should be merged into the next [BioSQL](http://www.biosql.org) release.

Biopython now includes wrappers for the new NCBI BLAST C++ tools, which will be replacing the old NCBI "legacy" BLAST tools written in C. The plain text BLAST parser has been updated to cope as well. Nevertheless, we (and the NCBI) still recommend using the XML output for parsing.

Bio.Entrez includes the [new (Jan 2010) DTD files](http://www.nlm.nih.gov/bsd/licensee/announce/2009.html#d09_17) from the NCBI for parsing MedLine/PubMed data.

The NCBI codon tables have been updated from version 3.4 to 3.9, which adds a few extra start codons, and a few new tables (Tables 16, 21, 22 and 23).

The restriction enzyme list in Bio.Restriction has been updated to the Nov 2009 release of [REBASE](http://rebase.neb.com/rebase/rebase.html).

The Bio.PDB parser and output code has been updated to understand the element column in ATOM and HETATM lines (based on patches contributed by Hongbo Zhu and Frederik Gwinner), and Bio.PDB.PDBList has been updated for recent changes to the PDB FTP site (Paul T. Bathen).

Finally, support for running Biopython under [Jython](http://www.jython.org) (using the Java Virtual Machine) has been much improved (with input from Kyle Ellrott). Note that Jython does not support C code, and currently Jython does not parse DTD files ( [Jython Issue 1447](http://bugs.jython.org/issue1447); needed for the Bio.Entrez XML parser). However, most of the Biopython modules seem fine from testing with Jython 2.5.0 and 2.5.1.

Sources and Windows Installers are available from our [downloads](http://www.biopython.org/wiki/Download) page.

Thanks to the Biopython development team and to everyone who has reported bugs or contributed patches since our last release.

(At least) 12 people contributed to this release, including 3 first timers:

- Bartek Wilczynski
- Brad Chapman
- Chris Lasher
- Cymon Cox
- Frank Kauff
- Frederik Gwinner (first contribution)
- Hongbo Zhu (first contribution)
- Kyle Ellrott
- Leighton Pritchard
- Michiel de Hoon
- Paul Bathen (first contribution)
- Peter Cock
