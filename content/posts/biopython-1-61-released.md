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
date: "2013-02-05T21:14:05+00:00"
guid: http://news.open-bio.org/news/?p=998
tag:
  - biopython
title: Biopython 1.61 released
url: /2013/02/05/biopython-1-61-released/

---
Source distributions and Windows installers for Biopython 1.61 are now available from the [downloads page](http://biopython.org/wiki/Download) on the [Biopython website](http://biopython.org/) and from the [Python Package Index (PyPI)](http://pypi.python.org/pypi/biopython).

The updated [Biopython Tutorial and Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html) is online ( [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)).

**Platforms/Deployment**

We currently support Python 2.5, 2.6 and 2.7 and also test under Python 3.1, 3.2 and 3.3 (including modules using NumPy), and [Jython](http://www.jython.org) 2.5 and [PyPy](http://pypy.org) 1.9 (Jython and PyPy do not cover NumPy or our C extensions). We are still encouraging early adopters to help test on these platforms, and have included a ‘beta’ installer for Python 3.2 (and Python 3.3 to follow soon) under 32-bit Windows.

Please note we are phasing out support for Python 2.5. We will continue support for at least one further release (Biopython 1.62). This could be extended given feedback from our users. Focusing on Python 2.6 and 2.7 only will make writing Python 3 compatible code easier.

**Features**

GenomeDiagram has three new sigils (shapes to illustrate features). OCTO shows an octagonal shape, like the existing BOX sigil but with the corners cut off. JAGGY shows a box with jagged edges at the start and end, intended for things like NNNNN regions in draft genomes. Finally BIGARROW is like the existing ARROW sigil but is drawn straddling the axis. This is useful for drawing vertically compact figures where you do not have overlapping genes.

New module Bio.Graphics.ColorSpiral can generate colors along a spiral path through HSV color space. This can be used to make arbitrary 'rainbow' scales, for example to color features or cross-links on a GenomeDiagram figure.

The Bio.SeqIO module now supports reading sequences from PDB files in two different ways. The "pdb-atom" format determines the sequence as it appears in the structure based on the atom coordinate section of the file (via Bio.PDB,
so NumPy is currently required for this). Alternatively, you can use the "pdb-seqres" format to read the complete protein sequence as it is listed in the PDB header, if available.

The Bio.SeqUtils module how has a seq1 function to turn a sequence using three letter amino acid codes into one using the more common one letter codes. This acts as the inverse of the existing seq3 function.

The multiple-sequence-alignment object used by Bio.AlignIO etc now supports an annotation dictionary. Additional support for per-column annotation is planned, with addition and splicing to work like that for the SeqRecord per-letter annotation.

The Bio.Motif module has been updated and reorganized. To allow for a clean deprecation of the old code, the new motif code is stored in a new module Bio.motifs, and a PendingDeprecationWarning was added to Bio.Motif.

**Experimental Code - SearchIO**

This release also includes [Bow's Google Summer of Code work](http://biopython.org/wiki/SearchIO) writing a unified parsing framework for NCBI BLAST (assorted formats including tabular and XML), HMMER, BLAT, and other sequence searching tools. This is currently available with the new `BiopythonExperimentalWarning` to indicate that this is still somewhat experimental. We're bundling it with the main release to get more public feedback, but with the big warning that the API is likely to change. In fact, even the current name of Bio.SearchIO may change since unless you are familiar with BioPerl its purpose isn't immediately clear.

**Contributors**

- Brandon Invergo
- Bryan Lunt (first contribution)
- Christian Brueffer (first contribution)
- David Cain
- Eric Talevich
- Grace Yeo (first contribution)
- Jeffrey Chang
- Jingping Li (first contribution)
- Kai Blin (first contribution)
- Leighton Pritchard
- Lenna Peterson
- Lucas Sinclair (first contribution)
- Michiel de Hoon
- Nick Semenkovich (first contribution)
- Peter Cock
- Robert Ernst (first contribution)
- Tiago Antao
- Wibowo 'Bow' Arindrarto
