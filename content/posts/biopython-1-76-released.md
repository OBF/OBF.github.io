---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - obf-projects
cover:
  alt: biopython
  image: /wp-content/uploads/2019/02/biopython.png
date: "2019-12-20T15:02:10+00:00"
guid: https://www.open-bio.org/?p=4432
tag:
  - biopython
title: Biopython 1.76 released
url: /2019/12/20/biopython-1-76-released/

---
Biopython 1.76 has been released and is available from our [website](https://biopython.org/wiki/Download) and [PyPI](https://pypi.python.org/pypi/biopython/1.76).

Coming relatively soon after our last release, the timing is linked to the official end of life for Python 2, and a [focus hereafter on Python 3](https://python3statement.org/). We intend this to be our final release supporting Python 2.7 and 3.5. Focusing on Python 3.6 or later will let us take advantage of new functionality and syntax, and simplify our code base and testing.

This release of Biopython supports Python 2.7, 3.5, 3.6, 3.7 and 3.8. It has also been tested on PyPy2.7.13 v7.1.1 and PyPy3.6.1 v7.1.1-beta0.

As in recent releases, more of our code is now explicitly available under either our original " _Biopython License Agreement_", or the very similar but more commonly used " _3-Clause BSD License_". See the `LICENSE.rst` file for more details.

In addition to the mainstream `x86_64` aka `AMD64` CPU architecture, we now also test every contribution on the `ARM64`, `ppc64le`, and `s390x` CPUs under Linux thanks to Travis CI. Further post-release testing done by Debian and other packagers and distributors of Biopython also covers these CPUs.

The `Bio.motifs.PositionSpecificScoringMatrix.search()` method has been re-written: it now applies `.calculate()` to chunks of the sequence to maintain a low memory footprint for long sequences.

Additionally, a number of small bugs and typos have been fixed with further additions to the test suite. There has been further work to follow the Python PEP8, PEP257 and best practice standard coding style, and more of the code style has been reformatted with the `black` tool.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Chris Daley (first contribution)
- Chris Rands
- Christian Brueffer
- Ilya Flyamer (first contribution)
- Jakub Lipinski (first contribution)
- Michael R. Crusoe (first contribution)
- Michiel de Hoon
- Peter Cock
- Sergio Valqui
