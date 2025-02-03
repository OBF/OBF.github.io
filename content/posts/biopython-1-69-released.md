---
author: peterc
category:
  - biopython
  - code
  - development
  - obf
  - obf-projects
cover:
  alt: Biopython 2003 Logo
  image: /wp-content/uploads/2013/12/biopython.jpg
date: "2017-04-07T11:03:24+00:00"
guid: https://news.open-bio.org/?p=1602
summary: |-
  Dear Biopythoneers,

  Source distributions and Windows installers for Biopython 1.69 are now available from the [downloads page](http://biopython.org/wiki/Download) on the official [Biopython website](http://biopython.org/), and the release is also [on the Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython/1.69).
tag:
  - biopython
  - development
  - obf
  - obf-projects
  - open-source
  - release
  - releases
title: Biopython 1.69 released
url: /2017/04/07/biopython-1-69-released/

---
Dear Biopythoneers,

Source distributions and Windows installers for Biopython 1.69 are now available from the [downloads page](http://biopython.org/wiki/Download) on the official [Biopython website](http://biopython.org/), and the release is also [on the Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython/1.69).

This release of Biopython supports Python 2.7, 3.3, 3.4, 3.5 and 3.6 (we have now dropped support for Python 2.6). It has also been tested on PyPy v5.7, PyPy3.5 v5.7 beta, and Jython 2.7.

We have started to dual-license Biopython under both our original liberal "Biopython License Agreement", and the very similar but more commonly used "3-Clause BSD License". In this release a small number of the Python files are explicitly available under either license, but most of the code remains under the "Biopython License Agreement" only. See the [LICENSE](https://github.com/biopython/biopython/blob/master/LICENSE.rst) file for more details.

We now expect and take advantage of NumPy under PyPy, and compile most of the Biopython C code modules as well.

[Bio.AlignIO](http://biopython.org/wiki/AlignIO) now supports the UCSC Multiple Alignment Format (MAF) under the format name "maf", using new module Bio.AlignIO.MafIO which also offers indexed access to these potentially large files using SQLite3 (contributed by Andrew Sczesnak, with additional refinements from Adam Novak).

Bio.SearchIO.AbiIO has been extended to support parsing FSA files. The underlying format (ABIF) remains the same as AB1 files and so the string 'abif' is the expected format argument in the main SeqIO functions. AbiIO determines whether the file is AB1 or FSA based on the presence of specific tags.

The Uniprot parser is now able to parse "submittedName" elements in XML files.

The NEXUS parser handling of internal node comments has been improved, which should help if working with tools like the BEAST TreeAnnotator. Slashes are now also allowed in identifiers.

New parser for ExPASy Cellosaurus, a cell line database, cell line catalogue, and cell line ontology (contributed by Steve Marshall).

For consistency the Bio.Seq module now offers a complement function (already available as a method on the Seq and MutableSeq objects).

The SeqFeature object's qualifiers is now an explicitly ordered dictionary (note that as of Python 3.6 the Python dict is ordered by default anyway). This helps reproduce GenBank/EMBL files on input/output.

The Bio.SeqIO UniProt-XML parser was updated to cope with features with unknown locations which can be found in mass spec data.

The Bio.SeqIO GenBank, EMBL, and IMGT parsers now record the molecule type from the LOCUS/ID line explicitly in the record.annotations dictionary. The Bio.SeqIO EMBL parser was updated to cope with more variants seen in patent data files, and the related IMGT parser was updated to cope with IPD-IMGT/HLA database files after release v3.16.0 when their ID line changed. The GenBank output now uses colon space to match current NCBI DBLINK lines.

The Bio.Affy package supports Affymetrix version 4 of the CEL file format, in addition to version 3.

The restriction enzyme list in Bio.Restriction has been updated to the February 2017 release of REBASE.

Bio.PDB.PDBList now can download PDBx/mmCif (new default), PDB (old default), PDBML/XML and mmtf format protein structures. This is inline with the RCSB recommendation to use PDBx/mmCif and deprecate the PDB file format. Biopython already has support for parsing mmCif files.

Additionally, a number of small bugs have been fixed with further additions to the test suite, and there has been further work to follow the Python PEP8, PEP257 and best practice standard coding style.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Aaron Rosenfeld
- Adam Kurkiewicz (first contribution)
- Adam Novak (first contribution)
- Adrian Altenhoff (first contribution)
- Allis Tauri (first contribution)
- Andrew Dalke
- Andrew Guy (first contribution)
- Andrew Sczesnak (first contribution)
- Ben Fulton
- Bernhard Thiel (first contribution)
- Bertrand Néron
- Blaise Li (first contribution)
- Brandon Carter (first contribution)
- Brandon Invergo
- Carlos Pena
- Carlos Ríos
- Chris Warth
- Emmanuel Noutahi
- Foen Peng (first contribution)
- Francesco Gastaldello (first contribution)
- Francisco Pina-Martins (first contribution)
- Hector Martinez (first contribution)
- Jacek Śmietański
- Jack Twilley (first contribution)
- Jeroen Van Goey (first contribution)
- Joshua Meyers (first contribution)
- Kurt Graff (first contribution)
- Lenna Peterson
- Leonhard Heizinger (first contribution)
- Marcin Magnus (first contribution)
- Markus Piotrowski
- Maximilian Greil (first contribution)
- Michał J. Gajda (first contribution)
- Michiel de Hoon
- Milind Luthra (first contribution)
- Oscar G. Garcia (first contribution)
- Owen Solberg
- Peter Cock
- Richard Neher (first contribution)
- Sebastian Bassi
- Sourav Singh (first contribution)
- Spencer Bliven (first contribution)
- Stefans Mezulis
- Steve Bond
- Steve Marshall (first contribution)
- Uri Laserson
- Veronika Berman (first contribution)
- Vincent Davis
- Wibowo 'Bow' Arindrarto

Thank you all.

![[Biopython Logo]](https://news.open-bio.org/wp-content/uploads/2013/12/biopython-300x84.jpg)

P.S. You can follow [@Biopython on Twitter](https://twitter.com/Biopython)

Checksums:

```
$ md5sum biopython-1.69.*
18ad299569eea79febf4641cce840db0  biopython-1.69.tar.gz
1acfa83d7340d82e248261f8344038be  biopython-1.69.win32-py2.7.exe
ff38a7286b455156619c8c2c4cb45a0e  biopython-1.69.win32-py2.7.msi
e03809050cd862226299ba4285b25615  biopython-1.69.win32-py3.3.exe
f8605d2e76e60353c776f69991067e07  biopython-1.69.win32-py3.3.msi
6bc7d291b7482f194f66a91d3eb89cb6  biopython-1.69.win32-py3.4.exe
0bc8e39ca0c3127b531f1998c91c7233  biopython-1.69.win32-py3.4.msi
0944a254c079869c481c13ac3bfa6c53  biopython-1.69.win32-py3.5.exe
567ba8c2b5e069cbcda5b13b558e4b1e  biopython-1.69.win32-py3.5.msi
48549d7083f1dcd37f73acfdbb30c100  biopython-1.69.win32-py3.6.exe
d3e02e227b6db736bc15f3ce4a08c149  biopython-1.69.win32-py3.6.msi
a134c5b8e35d6515ca4f9e663000bcb3  biopython-1.69.zip
```

```
$ shasum -a 256 biopython-1.69.*
169ffa90c3d3ec5678c7a5c99501c0cfeb54c40ca51a619ce6cee5026d3403eb  biopython-1.69.tar.gz
6520ac092f52fd35b48d12c5f264d78c4cd20ede841a4755b73376184c1f9c83  biopython-1.69.win32-py2.7.exe
505aa27537f358129d096c1cb5b761108c6200a11483d25ad83188b11089b45c  biopython-1.69.win32-py2.7.msi
11a5a04da0d8830789d53fed7d631f5a8a6d3926869241d212265b7b9889b987  biopython-1.69.win32-py3.3.exe
7e3e764236e29f01fe3b346878801ee9f1166269e4ac557d88201e2f1cd85949  biopython-1.69.win32-py3.3.msi
c9ee5594e5f865fbf4871be8661e4be559dcb599c64e7fa4922e55b771aab249  biopython-1.69.win32-py3.4.exe
8426e2b548e594d63bfa7584f39513ee906d2de32037c900af9b6625318e051c  biopython-1.69.win32-py3.4.msi
3025f12b7f8cf81b25823223dc17830d4e0eeda8095e59177069d44fa2be9d32  biopython-1.69.win32-py3.5.exe
853eb6b75ca84ba703e0c8873d673b49f1580b5b1b9372105fbf9735153ad0dd  biopython-1.69.win32-py3.5.msi
7f11960168e335c1581de2e4a90bef905c92e08d42c67482f25a522db5d7b702  biopython-1.69.win32-py3.6.exe
4cac457773f251c511ede520f3e8701d8f00e22524103e03d0d1f69a040f95bf  biopython-1.69.win32-py3.6.msi
e71ae4c5ba996cbe01002d55d877bf5eafa053c116012d7ace489dfc41959e05  biopython-1.69.zip
```
