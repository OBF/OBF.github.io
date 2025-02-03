---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - obf
  - obf-projects
cover:
  alt: Biopython 2003 Logo
  image: /wp-content/uploads/2013/12/biopython.jpg
date: "2015-10-21T19:55:16+00:00"
guid: http://news.open-bio.org/news/?p=1401
tag:
  - biopython
  - code
  - development
  - obf
  - obf-projects
  - release
title: Biopython 1.66 released
url: /2015/10/21/biopython-1-66-released/

---
Source distributions and Windows installers for Biopython 1.66 are now available from the [downloads page](http://biopython.org/wiki/Download) on the [official Biopython website](http://biopython.org/) and from the [Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython/1.66).

This release of Biopython supports Python 2.6, 2.7, 3.3, 3.4 and 3.5, although support for Python 2.6 is now deprecated. It has also been tested on PyPy 2.4 to 2.6, PyPy3 version 2.4, and Jython 2.7.

Further work on the `Bio.KEGG` and `Bio.Graphics` modules now allows drawing KGML pathways with transparency.

The `Bio.SeqIO "abi"` parser now decodes almost all the documented fields used by the ABIF instruments - including the individual color channels.

`Bio.PDB` now has a `QCPSuperimposer` module using the Quaternion Characteristic Polynomial algorithm for superimposing structures. This is a fast alternative to the existing `SVDSuperimposer` code using singular value decomposition.

Bio.Entrez now implements the NCBI Entrez Citation Matching function (ECitMatch), which retrieves PubMed IDs (PMIDs) that correspond to a set of input citation strings. `Bio.Entrez.parse(...)` now supports NCBI XML files using XSD schemas, which will be downloaded and cached like NCBI DTD files.

A subtle bug in how multi-part GenBank/EMBL locations on the reverse strand were parsed into CompoundLocations was fixed: `complement(join(...))` as used by NCBI worked, but `join(complement(...),complement(...),...)` as used by EMBL/ENSEMBL gave the CompoundLocation parts in the wrong order. A related bug when taking the reverse complement of a SeqRecord containing features with CompoundLocations was also fixed.

Additionally, a number of small bugs have been fixed with further additions to the test suite, and there has been further work on conforming to the Python PEP8 standard coding style.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Alan Medlar (first contribution)
- Anthony Mathelier (first contribution)
- Antony Lee (first contribution)
- Anuj Sharma (first contribution)
- Ben Fulton (first contribution)
- Bertrand Néron (first contribution)
- Brandon Invergo
- Carlos Pena
- Christian Brueffer
- Connor T. Skennerton (first contribution)
- David Arenillas (first contribution)
- David Nicholson (first contribution)
- Emmanuel Noutahi (first contribution)
- Eric Rasche (first contribution)
- Fabio Madeira (first contribution)
- Franco Caramia (first contribution)
- Gert Hulselmans (first contribution)
- Gleb Kuznetsov (first contribution)
- João Rodrigues
- John Bradley (first contribution)
- Kai Blin
- Kian Ho (first contribution)
- Kozo Nishida (first contribution)
- Kuan-Yi Li (first contribution)
- Leighton Pritchard
- Lucas Sinclair
- Michiel de Hoon
- Peter Cock
- Saket Choudhary
- Sunhwan Jo (first contribution)
- Tarcisio Fedrizzi (first contribution)
- Tiago Antao
- Vincent Davis

This is a longer list than usual, which is good, but in part this reflects the fact that this release is long overdue. Sorry, that was my fault.
