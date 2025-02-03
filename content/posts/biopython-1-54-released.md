---
author: andreas
category:
  - biopython
  - code
  - community
  - development
  - general
  - google-summer-of-code
  - obf
  - obf-projects
date: "2010-05-20T19:04:27+00:00"
guid: http://news.open-bio.org/news/?p=653
tag:
  - biopython
  - release
title: Biopython 1.54 released
url: /2010/05/20/biopython-release-154/

---
The Biopython team is proud to announce Biopython 1.54, a new stable release of the Biopython library. Biopython 1.54 comes five months after our last release and brings new features, tweaks to some established functions and the usual collection of bug fixes.

This is the first stable release to feature the new [Bio.Phylo](http://www.biopython.org/wiki/Phylo "Bio.Phylo documentation on the wiki") module which can be used to read, write and take data from phylogenetic trees in Newick, Nexus and [PhyloXML](http://www.phyloxml.org/ "PhyloXML decription") formats. The module is the result of Eric Talevich's Google Summer of Code project which was supported by [The National Evolutionary Synthesis Center (NESCent)](http://www.nescent.org/index.php).

Biopython now supports the reading, writing and indexing of Standard Flowgram Format (SFF) files produced in 454 sequencing. Jose Blanca (the brains behind the widely used [sff\_extract](http://bioinf.comav.upv.es/sff_extract/ "sff_extract homepage") tool) provided code to handle SFF files and Peter Cock has integrated that code with `Bio.SeqIO`. Adding SFF support to `SeqIO` makes it possible to convert these files to the FASTQ, FASTA and QUAL formats (as trimmed or untrimmed reads).

As well as adding features the new release tweaks and extends some of the core modules:

- Both `Bio.SeqIO` and `Bio.AlignIO` will accept filenames as well as handles, [as detailed here](http://news.open-bio.org/news/2010/04/biopython-seqio-and-alignio-easier/).
- The multiple sequence alignment object that underlies Bio.AlignIO has been improved.
- `Bio.SeqIO` can read and write EMBL nucleotide files.
- The dictionary-like objects returned by `Bio.SeqIO.index()` have a new method " `get_raw`" that gets unparsed data from a file as a string, [as detailed here](http://news.open-bio.org/news/2010/04/partial-seq-files-biopython/).
- `Bio.Entrez` includes some more DTD files, in particular `eLink_090910.dtd`, used by our NCBI Entrez Utilities XML parser.

Binaries and source files for Biopython 1.54 are available from the [downloads page](http://www.biopython.org/wiki/Download). The [documentation](http://www.biopython.org/wiki/Documentation "Biopython Documentation") has been updated to include the changes made since our last release.

A big thanks to every one who tested our beta release or submitted bugs since [Biopython 1.53](http://news.open-bio.org/news/2009/12/biopython-release-153/). And an especially big thanks to everyone who contributed to this release, including five first time contributors:

- Anne Pajon (first contribution)
- Brad Chapman
- Christian Zmasek
- Diana Jaunzeikare (first contribution)
- Eric Talevich
- Jose Blanca (first contribution)
- Kevin Jacobs (first contribution)
- Leighton Pritchard
- Michiel de Hoon
- Peter Cock
- Thomas Holder (first contribution)
