---
author: peterc
category:
  - biopython
  - bosc
  - code
  - community
  - development
  - obf
  - obf-projects
date: "2013-08-28T22:14:43+00:00"
guid: http://news.open-bio.org/news/?p=1035
tag:
  - biopython
  - code
  - community
  - development
  - obf
  - obf-projects
  - open-source
  - release
title: Biopython 1.62 released
url: /2013/08/28/biopython-1-62-released/

---
Source distributions and Windows installers for **Biopython 1.62** are now available from the [downloads page](http://biopython.org/wiki/Download "Biopython Downloads") on the [official Biopython website](http://biopython.org/ "Biopython website") and ( _soon_) from the [Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython).

**Python support**

This is our first release of Biopython which _officially supports Python 3_. Specifically, this is supported under Python 3.3. Older versions of Python 3 may still work albeit with some issues, but are _not_ supported.

We still fully support Python 2.5, 2.6, and 2.7. Support under [Jython](http://www.jython.org/) is available for versions 2.5 and 2.7 and under [PyPy](http://pypy.org/) for versions 1.9 and 2.0. However, unlike CPython, Jython and PyPy support is partial: NumPy and our C extensions are not covered.

Please note that this release marks our last official for support Python 2.5. Beginning from Biopython 1.63, the minimum supported Python version will be 2.6.

**Highlights**

- The translation functions will give a warning on any partial codons (and this will probably become an error in a future release). If you know you are dealing with partial sequences, either pad with "N" to extend the sequence length to a multiple of three, or explicitly trim the sequence.
- The handling of joins and related complex features in Genbank/EMBL files has been changed with the introduction of a `CompoundLocation` object. Previously a `SeqFeature` for something like a multi-exon CDS would have a child `SeqFeature` (under the `sub_features` attribute) for each exon. The `sub_features` property will still be populated for now, but is deprecated and will in future be removed. Please consult the examples in the help (docstrings) and Tutorial.
- Thanks to the efforts of Ben Morris, the Phylo module now supports the file formats NeXML and CDAO. The Newick parser is also significantly faster, and can now optionally extract bootstrap values from the Newick comment field (like Molphy and Archaeopteryx do). Nate Sutton added a wrapper for FastTree to `Bio.Phylo.Applications`.
- New module `Bio.UniProt` adds parsers for the GAF, GPA and GPI formats from UniProt-GOA.
- The `BioSQL` module is now supported in Jython. MySQL and PostgreSQL databases can be used. The relevant JDBC driver should be available in the `CLASSPATH`.
- Feature labels on circular `GenomeDiagram` figures now support the `label_position` argument (start, middle or end) in addition to the current default placement, and in a change to prior releases these labels are outside the features which is now consistent with the linear diagrams.
- The code for parsing 3D structures in mmCIF files was updated to use the Python standard library's `shlex` module instead of C code using flex.
- The `Bio.Sequencing.Applications` module now includes a BWA command line wrapper.
- `Bio.motifs` supports JASPAR format files with multiple position-frequence matrices.

Additionally there have been other minor bug fixes and more unit tests.

**Contributors**

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Alexander Campbell (first contribution)
- Andrea Rizzi (first contribution)
- Anthony Mathelier (first contribution)
- Ben Morris (first contribution)
- Brad Chapman
- Christian Brueffer
- David Arenillas (first contribution)
- David Martin (first contribution)
- Eric Talevich
- Iddo Friedberg
- Jian-Long Huang (first contribution)
- Joao Rodrigues
- Kai Blin
- Lenna Peterson
- Michiel de Hoon
- Matsuyuki Shirota (first contribution)
- Nate Sutton (first contribution)
- Peter Cock
- Petra Kubincová (first contribution)
- Phillip Garland
- Saket Choudhary (first contribution)
- Tiago Antao
- Wibowo 'Bow' Arindrarto
- Xabier Bello (first contribution)
