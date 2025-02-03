---
author: chebizarro
category:
  - biopython
  - blogroll
  - code
  - development
  - obf-projects
date: "2020-05-25T14:34:47+00:00"
guid: https://www.open-bio.org/?p=4768
tag:
  - biopython
title: Biopython 1.77 released
url: /2020/05/25/biopython-1-77-released/

---
Biopython 1.77 has been released and is available from our [website](https://biopython.org/wiki/Download) and [PyPI](https://pypi.python.org/pypi/biopython/1.77).

This is the first release since we dropped support for Python 2.7 and 3.5. Focusing on Python 3.6 or later will let us take advantage of new functionality and syntax, and simplify our code base and testing.

This release of Biopython supports Python 3.6, 3.7 and 3.8 It has also been tested on PyPy3.6.1 v7.1.1.

`pairwise2` now allows the input of parameters with keywords and returns the alignments as a list of `namedtuples`.

The codon tables have been updated to NCBI genetic code table version 4.5, which adds _Cephalodiscidae_ mitochondrial as table 33.

`Bio.Restriction` has been updated to the January 2020 release of REBASE.

A major contribution by Rob Miller to `Bio.PDB` provides new methods to handle protein structure transformations using dihedral angles (internal coordinates). The new framework supports lossless interconversion between internal and cartesian coordinates, which, among other uses, simplifies the analysis and manipulation of coordinates of protein structures.

As in recent releases, more of our code is now explicitly available under either our original " _Biopython License Agreement_", or the very similar but more commonly used " _3-Clause BSD License_". See the `LICENSE.rst` file for more details.

Additionally, a number of small bugs and typos have been fixed with further additions to the test suite. There has been further work to follow the Python PEP8, PEP257 and best practice standard coding style, and more of the code style has been reformatted with the `black` tool.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Alexander Decurnou (first contribution)
- Andrei Istrate (first contribution)
- Andrey Raspopov
- Austin Varela (first contribution)
- Chris Daley
- Chris Rands
- Deepak Khatri
- Hielke Walinga (first contribution)
- Kai Blin
- Karthikeyan Singaravelan (first contribution)
- Markus Piotrowski
- Michiel de Hoon
- Peter Cock
- Rob Miller
- Sergio Valqui
- Steve Bond
- Sujan Dulal (first contribution)
- Tianyi Shi (first contribution)

_Update_: And the following two whom we had initially wrongly listed under the previous release:

- Artemi Bendandi (first contribution)
- Konstantinos Zisis (first contribution)
