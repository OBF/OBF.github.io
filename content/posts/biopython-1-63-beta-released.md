---
author: tiago
category:
  - biopython
  - code
  - community
  - development
  - obf
  - obf-projects
date: "2013-11-12T16:20:05+00:00"
guid: http://news.open-bio.org/news/?p=1063
tag:
  - biopython
  - code
  - community
  - development
  - obf-projects
  - open-source
title: Biopython 1.63 beta released
url: /2013/11/12/biopython-1-63-beta-released/

---
Source distributions and Windows installers for **Biopython 1.63 beta** are now available from the [downloads page](http://biopython.org/wiki/Download "Biopython<br /><br /><br /><br /> Downloads") on the [official Biopython website](http://biopython.org/ "Biopython website").

This is a beta release for testing purposes, the main reason for a beta version is the large amount of changes imposed by the removal of the 2to3 library previously required for the support of Python 3.X. **This was made possible by dropping Python 2.5 (and Jython 2.5).**

This release of Biopython supports Python 2.6 and 2.7, and also Python 3.3.

The Biopython Tutorial & Cookbook, and the docstring examples in the source code, now use the Python 3 style print function in place of the Python 2 style print statement. This language feature is available under Python 2.6 and 2.7 via:

```
    from __future__ import print_function
```

Similarly we now use the Python 3 style built-in next function in place of the Python 2 style iterators' .next() method. This language feature is also available under Python 2.6 and 2.7.

**Contributors**

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Chris Mitchell (first contribution)
- Christian Brueffer
- Eric Talevich
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
