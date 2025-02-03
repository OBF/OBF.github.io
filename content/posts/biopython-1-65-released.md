---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - obf
  - obf-projects
cover:
  alt: Biopython 2003 Logo
  image: /wp-content/uploads/2013/12/biopython.jpg
date: "2014-12-17T21:06:29+00:00"
guid: http://news.open-bio.org/news/?p=1226
tag:
  - biopython
  - development
  - open-source
  - release
title: Biopython 1.65 released
url: /2014/12/17/biopython-1-65-released/

---
Dear Biopythoneers,

Source distributions and Windows installers for Biopython 1.65 are now available from the [downloads page](http://biopython.org/wiki/Download) on the [official Biopython website](http://biopython.org/) and from the [Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython).

This release of Biopython supports Python 2.6, 2.7, 3.3 and 3.4. It is also tested on PyPy 2.0 to 2.4, PyPy3 version 2,4, and Jython 2.7b2.

The most visible change is that the Biopython _**sequence objects now use string comparison**_, rather than Python's object comparison. This has been planned for a long time with warning messages in place (under Python 2, the warnings were sadly missing under Python 3).

The Bio.KEGG and Bio.Graphics modules have been expanded with support for the online KEGG REST API, and parsing, representing and drawing KGML pathways.

The _Pterobranchia_ Mitochondrial genetic code has been added to Bio.Data (and the translation functionality), which is the new [NCBI genetic code](http://www.ncbi.nlm.nih.gov/Taxonomy/Utils/wprintgc.cgi) table 24.

The Bio.SeqIO parser for the ABI capillary file format now exposes all the raw data in the SeqRecord's annotation as a dictionary. This allows further in-depth analysis by advanced users.

Bio.SearchIO QueryResult objects now allow Hit retrieval using its alternative IDs (any IDs listed after the first one, for example as used with the NCBI BLAST NR database).

Bio.SeqUtils.MeltingTemp has been rewritten with new functionality.

The new experimental module Bio.CodonAlign has been renamed Bio.codonalign (and similar lower case PEP8 style module names have been used for the sub-modules within this).

Bio.SeqIO.index\_db(...) and Bio.SearchIO.index\_db(...) now store any relative filenames relative to the index file, rather than (as before) relative to the current directory at the time the index was built. This makes the indexes less fragile, so that they can be used from other working directories. _NOTE:_ This change is backward compatible (old index files work as before), however relative paths in new indexes will not work on older versions of Biopython!

Behind the scenes, we have done a lot of work applying [PEP8 coding styles](https://www.python.org/dev/peps/pep-0008/) to Biopython, and improving the formatting of the source code documentation ( [PEP257 docstrings](https://www.python.org/dev/peps/pep-0257/)).

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Alan Du (first contribution)
- Carlos Pena (first contribution)
- Colin Lappala (first contribution)
- Christian Brueffer
- David Bulger (first contribution)
- Eric Talevich
- Evan Parker (first contribution)
- Hongbo Zhu
- Kai Blin
- Kevin Wu (first contribution)
- Leighton Pritchard
- Leszek Pryszcz (first contribution)
- Markus Piotrowski
- Matt Shirley (first contribution)
- Mike Cariaso (first contribution)
- Peter Cock
- Seth Sims (first contribution)
- Tiago Antao
- Travis Wrightsman (first contribution)
- Tyghe Vallard (first contribution)
- Vincent Davis
- Wibowo 'Bow' Arindrarto
- Zheng Ruan

This is a longer list of contributors and changes than usual, but it was also a longer gap since our last release.
