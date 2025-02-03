---
author: peterc
category:
  - biopython
  - code
  - development
  - obf
  - obf-projects
date: "2012-06-25T18:17:08+00:00"
guid: http://news.open-bio.org/news/?p=940
tag:
  - biopython
title: Biopython 1.60 released
url: /2012/06/25/biopython-1-60-released/

---
Source distributions and Windows installers for **Biopython 1.60** are now available from the [downloads page](http://biopython.org/wiki/Download) on the [Biopython website](http://biopython.org/) and from the [Python Package Index (PyPI)](http://pypi.python.org/pypi/biopython).

### Platforms/Deployment

We currently support Python 2.5, 2.6 and 2.7 and also test under [Jython](http://www.jython.org/) 2.5 and [PyPy](http://pypy.org/) 1.9 (which does not cover NumPy or our C extensions). Please note that Python 2.4 or earlier is not supported.

Most functionality is also working under Python 3.1 and 3.2 (including modules using NumPy). We are now encouraging early adopters to help beta testing on these platforms, and have included a 'beta' installer for Python 3.2 under 32-bit Windows.

### Features

New module `Bio.bgzf` supports reading and writing BGZF files (Blocked GNU Zip Format), a variant of GZIP with efficient random access, most commonly used as part of the [BAM file format](http://samtools.sourceforge.net/) and in [tabix](http://samtools.sourceforge.net/tabix.shtml). This uses Python's `zlib` library internally, and provides a simple interface like Python's gzip library. Using this the `Bio.SeqIO` indexing functions now support BGZF compressed sequence files. See this blog post for [more](http://custom-essay-service-help.co.uk/) background on [BGZF and SeqIO](http://blastedbio.blogspot.com/2011/11/bgzf-blocked-bigger-better-gzip.html).

The GenBank/EMBL parser will now give a warning on unrecognized feature locations and continue parsing (leaving the feature's location as None). Previously it would abort with an exception, which was often unhelpful.

The `Bio.PDB.MMCIFParser` is now compiled by default (but is still not available under Jython, PyPy or Python 3).

The SFF parser in `Bio.SeqIO` now decodes Roche 454 'universal accession number' 14 character read names, which encode the timestamp of the run, the region the read came from, and the location of the well.

In the Phylo module, the "draw" function for plotting tree objects has become much more flexible, with improved support for [matplotlib](http://matplotlib.sourceforge.net/) conventions and new parameters for specifying branch and taxon labels. Writing in the [PhyloXML](http://www.phyloxml.org/) format has been updated to more closely match the output of other programs. A wrapper for the program [RAxML](http://sco.h-its.org/exelixis/software.html) has been added under `Bio.Phylo.Applications`, alongside the existing wrapper for PhyML.

Additionally there have been other minor bug fixes and more unit tests.

### Contributors

Many thanks to the Biopython developers and community for making this release
possible, especially the following contributors:

- Brandon Invergo
- Eric Talevich
- Jeff Hussmann (first contribution)
- John Comeau (first contribution)
- Kamil Slowikowski (first contribution)
- Kevin Jacobs
- Lenna Peterson (first contribution)
- Matt Fenwick (first contribution)
- Peter Cock
- Paul T. Bathen
- Wibowo Arindrarto
