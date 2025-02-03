---
author: tiago
category:
  - biopython
  - code
  - community
  - development
  - obf-projects
cover:
  alt: Biopython 2003 Logo
  image: /wp-content/uploads/2013/12/biopython.jpg
date: "2013-12-06T11:16:26+00:00"
guid: http://news.open-bio.org/news/?p=1076
tag:
  - biopython
  - code
  - community
  - development
  - obf-projects
  - open-source
title: Biopython 1.63 released
url: /2013/12/06/biopython-1-63-released/

---
Source distributions and Windows installers for **Biopython 1.63** are now available from the [downloads page](http://biopython.org/wiki/Download "Biopython Downloads") on the [official Biopython website](http://biopython.org/ "Biopython website") and ( _soon_) from the [Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython).

The current version removed the requirement of the 2to3 library. This was made possible by dropping Python 2.5 (and Jython 2.5).

This release of Biopython supports Python 2.6 and 2.7, and also Python 3.3.

The Biopython Tutorial & Cookbook, and the docstring examples in the source code, now use the Python 3 style print function in place of the Python 2 style print statement. This language feature is available under Python 2.6 and 2.7 via:

```
from __future__ import print_function
```

Similarly we now use the Python 3 style built-in next function in place of the Python 2 style iterators' .next() method. This language feature is also available under Python 2.6 and 2.7.

The restriction enzyme list in Bio.Restriction has been updated to the December 2013 release of REBASE.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Chris Mitchell (first contribution)
- Christian Brueffer
- Eric Talevich
- Gokcen Eraslan (first contribution)
- Josha Inglis (first contribution)
- Konstantin Tretyakov (first contribution)
- Lenna Peterson
- Martin Mokrejs
- Nigel Delaney (first contribution)
- Peter Cock
- Sergei Lebedev (first contribution)
- Tiago Antao
- Wayne Decatur (first contribution)
- Wibowo 'Bow' Arindrarto
