---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - obf-projects
cover:
  alt: biopython_2017_banner_white_bg
  image: /wp-content/uploads/2017/07/biopython_2017_banner_white_bg.png
date: "2018-04-04T15:32:14+00:00"
guid: https://news.open-bio.org/?p=1922
tag:
  - biopython
  - code
  - development
  - obf-projects
  - open-source
  - release
  - releases
title: Biopython 1.71 released
url: /2018/04/04/biopython-1-71-released/

---
Dear Biopythoneers,

Source distributions of Biopython 1.71 are now available from the [downloads page](http://biopython.org/wiki/Download) on the official [Biopython website](http://biopython.org/), and the release is also [on the Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython/1.71) including pre-compiled Wheel Packages for Linux, Mac OS X and Windows.

This release of Biopython supports Python 2.7, 3.4, 3.5 and 3.6 (we have now dropped support for Python 3.3). It has also been tested on PyPy2.7 v5.10.0 and PyPy3.5 v5.10.1.

Python 3 is the primary development platform for Biopython. We will drop support for Python 2.7 no later than 2020, in line with the end-of-life or sunset date for Python 2.7 itself.

_**Setup changes:**_

We now explicitly recommend installation using "pip install biopython", rather than the classic "python setup.py install" approach. In a related change, we depend on the Python package setuptools (rather than the older package distutils in the Python standard library) and have made the dependency on NumPy explicit and automatic.

_**License changes:**_

As of Biopython 1.69, we have started to dual-license Biopython under both our original liberal “Biopython License Agreement”, and the very similar but more commonly used “3-Clause BSD License”. A growing number of the Python files are explicitly available under either license, but most of the code remains under the “Biopython License Agreement” only. See the [LICENSE](https://github.com/biopython/biopython/blob/master/LICENSE.rst) file for more details.

_**Code changes:**_

Encoding issues have been fixed in several parsers when reading data files with non-ASCII characters, like accented letters in people's names. This would raise `UnicodeDecodeError: 'ascii' codec can't decode byte ...` under some system locale settings.

Bio.KEGG can now parse Gene files.

The multiple-sequence-alignment object used by Bio.AlignIO etc now supports a per-column annotation dictionary, useful for richly annotated alignments in the Stockholm/PFAM format.

The SeqRecord object now has a translate method, following the approach used for its existing reverse\_complement method etc.

The output of function `format_alignment` in `Bio.pairwise2` for displaying a pairwise sequence alignment as text now indicates gaps and mis-matches.

Bio.SeqIO now supports reading and writing two-line-per-record FASTA files under the format name "fasta-2line", useful if you wish to work without line-wrapped sequences.

Bio.PDB now contains a writer for the mmCIF file format, which has been the standard PDB archive format since 2014. This allows structural objects to be written out and facilitates conversion between the PDB and mmCIF file formats.

Bio.Emboss.Applications has been updated to fix a wrong parameter in fuzznuc wrapper and include a new wrapper for fuzzpro.

The restriction enzyme list in Bio.Restriction has been updated to the November 2017 release of REBASE.

New codon tables 27-31 from NCBI (NCBI genetic code table version 4.2) were added to Bio.Data.CodonTable. Note that tables 27, 28 and 31 contain no dedicated stop codons; the stop codons in these codes have a context dependent encoding as either STOP or as amino acid.

IO functions such as `SeqIO.parse` now accept any objects which can be passed to the builtin `open` function. Specifically, this allows using `pathlib.Path` objects under Python 3.6 and newer, as per [PEP 519](https://www.python.org/dev/peps/pep-0519).

Bio.SearchIO can now parse InterProScan XML files.

For Python 3 compatibility, comparison operators for the entities within a Bio.PDB Structure object were implemented. These allow the comparison of models, chains, residues, and atoms with the common operators (==, !=, >, ...) Comparisons are based on IDs and take the parents of the entity up to the model level into account. For consistent behaviour of all entities the operators for atoms were modified to also consider the parent IDs. NOTE: this represents a change in behaviour in respect to v1.70 for Atom comparisons. In order to mimic the behaviour of previous versions, comparison will have to be done for Atom IDs and alternative locations specifically.

Additionally, a number of small bugs have been fixed with further additions to the test suite, and there has been further work to follow the Python [PEP8](https://www.python.org/dev/peps/pep-0008), [PEP257](https://www.python.org/dev/peps/pep-0257) and best practice standard coding style.

_**Acknowledgements:**_

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Adhemar Zerlotini
- Ariel Aptekmann
- Chris Rands
- Christian Brueffer
- Erik Cederstrand (first contribution)
- Fei Qi (first contribution)
- Francesco Gastaldello
- James Jeffryes (first contribution)
- Jerven Bolleman (first contribution)
- Joe Greener (first contribution)
- Joerg Schaarschmidt (first contribution)
- João Rodrigues
- Jeroen Van Goey
- Jun Aruga (first contribution)
- Kai Blin
- Kozo Nishida
- Lewis A. Marshall (first contribution)
- Markus Piotrowski
- Michiel de Hoon
- Nicolas Fontrodona (first contribution)
- Peter Cock
- Philip Bergstrom (first contribution)
- rht (first contribution)
- Saket Choudhary
- Shuichiro MAKIGAKI (first contribution)
- Shyam Saladi (first contribution)
- Siong Kong
- Spencer Bliven
- Stefans Mezulis
- Steve Bond
- Yasar L. Ahmed (first contribution)
- Zachary Sailer (first contribution)
- Zaid Ur-Rehman (first contribution)

Thank you all.

P.S. You can follow [@Biopython on Twitter](https://twitter.com/Biopython) _**Checksums**_:

```
$ md5sum biopython-1.71*
b2cd1215bacfb7cb9ee73b6b67695da0  biopython-1.71-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
a85b46133003383e428b05895e5d3613  biopython-1.71-cp27-cp27m-manylinux1_i686.whl
89e368cbcb6517915ee371f27f459b90  biopython-1.71-cp27-cp27m-manylinux1_x86_64.whl
395e12573e9a56130489aafe3617e254  biopython-1.71-cp27-cp27mu-manylinux1_i686.whl
f80e811aeebf9241e03a6ef3d4c9d9c6  biopython-1.71-cp27-cp27mu-manylinux1_x86_64.whl
b98d04351a94eb94a95e57c4ded460c2  biopython-1.71-cp27-cp27m-win32.whl
4997d76f075f4840d82f7d596917ba92  biopython-1.71-cp27-cp27m-win_amd64.whl
47b6e58c03599b4e8a5534efa9171d0c  biopython-1.71-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
53df08929d39abda3c0b668d7d06456c  biopython-1.71-cp34-cp34m-manylinux1_i686.whl
d308f83c49dc38395928348628d24238  biopython-1.71-cp34-cp34m-manylinux1_x86_64.whl
a2f05c067222c31091ad97c6c394e54d  biopython-1.71-cp34-cp34m-win32.whl
b5f26e1288f5124a2a02ffeab7139650  biopython-1.71-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
0f5e731a17b3d5798347a21b88224583  biopython-1.71-cp35-cp35m-manylinux1_i686.whl
4f1fa297348d4797acab537b44480aaa  biopython-1.71-cp35-cp35m-manylinux1_x86_64.whl
cf859db69d1c182f133cd34774ff15ca  biopython-1.71-cp35-cp35m-win32.whl
9eb34690189f4c156157e0991852bb56  biopython-1.71-cp35-cp35m-win_amd64.whl
80cf17e84f22a4ea61e7394a521500f9  biopython-1.71-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
09fbad06133a8b2b9c3d20faa0d6a156  biopython-1.71-cp36-cp36m-manylinux1_i686.whl
d7e15723aac481d945289d179a52a9f9  biopython-1.71-cp36-cp36m-manylinux1_x86_64.whl
80c03614cb3b4c486793e6e31c62403d  biopython-1.71-cp36-cp36m-win32.whl
dc7149f7297176bf0c8ca80fa176ecb0  biopython-1.71-cp36-cp36m-win_amd64.whl
966ac542f39809c37852410a95f641fb  biopython-1.71.tar.gz
4c63ec2a2908adf8d3338f8e8b180514  biopython-1.71.zip
```

```
$ shasum -a 256 biopython-1.71*
f919aa78031c00e44350742331f5a1eed7b447bde7812abe2ca0f6a5165900bb  biopython-1.71-cp27-cp27m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
7449d7df74a298c190fbc9ad60591577acb2e45d5ff788faa8672df460f3dc4d  biopython-1.71-cp27-cp27m-manylinux1_i686.whl
3fdf4c9502404dd62905fd70bce57806cb775e636eede5de13f1abe8f0915158  biopython-1.71-cp27-cp27m-manylinux1_x86_64.whl
4960e0ec35de8b02cd0b6a720db623abf30931a5677046ec06c0097b6a565541  biopython-1.71-cp27-cp27mu-manylinux1_i686.whl
4e4c6fe00e1d49e016634602e8554380ec437b505d8f20132da408a37da560ce  biopython-1.71-cp27-cp27mu-manylinux1_x86_64.whl
65f00db00b2f91ba90e5bb61c7dd14d2beacb9f2d3e60c9d4330376b693d8975  biopython-1.71-cp27-cp27m-win32.whl
6318172b107ad72abf45a03de6a189a3e7cfc2e682d402520c14bbbe8295e335  biopython-1.71-cp27-cp27m-win_amd64.whl
5b7284947a4b657d7955d0af8c48594be62a4d8dd51b84223fded371e81911d6  biopython-1.71-cp34-cp34m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
20fbbbc0f1c2f11972ea598191ba2cd8cb7ecb38595fa89031b9c3974ebcbdff  biopython-1.71-cp34-cp34m-manylinux1_i686.whl
9fabcb8cd0a87c5e2514bc959f5504ea5dc58219bc2ff91e6c689279322319c6  biopython-1.71-cp34-cp34m-manylinux1_x86_64.whl
038ecb2376cbfd2b42e79f64fe96ffb4921fecacad6f5157b684168933320455  biopython-1.71-cp34-cp34m-win32.whl
b7782271639fb92ea7fde4ad1caeeed3ca4ba6795de81bde391a4ea21e3870fb  biopython-1.71-cp35-cp35m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
14067b4ae2596979fd82a1e61fafbf2f8acd81f547b09220d8f4d7642a2b3759  biopython-1.71-cp35-cp35m-manylinux1_i686.whl
1c6190b552c5b9e2b2b7456ecc5258f344b1afee63c1d656b610a5c1a4b52b3f  biopython-1.71-cp35-cp35m-manylinux1_x86_64.whl
23580bf169d044cc749819465520f33579c62ce06816f87f814e4a78fdd48877  biopython-1.71-cp35-cp35m-win32.whl
f2603eeb09a7eef41eb81d874901c02e848ad80776f9e80d91b15206e7c4441d  biopython-1.71-cp35-cp35m-win_amd64.whl
9f800d7db93685a73fe244d16ab76dec91e51ddcde20a3f9e8dffa3d05170d96  biopython-1.71-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
4b7f6552b4d9162ca90bc0515a93815a7d81b8b0435932ab0aaf2affc53b40f6  biopython-1.71-cp36-cp36m-manylinux1_i686.whl
6ac8e5c2f6ffa1190a491ccc5f00e004d05107abf9879ebdff202088be31d02a  biopython-1.71-cp36-cp36m-manylinux1_x86_64.whl
693e9f2955393438613a431fe9b308d3d39a30923fe1efd32e0000c83feda6e3  biopython-1.71-cp36-cp36m-win32.whl
dccb66a68968c4c76a7ec92d82e44abf8721a2f65c9afb7acdc3deb2457b7b4e  biopython-1.71-cp36-cp36m-win_amd64.whl
4f1770a29a5b18fcaca759bbc888083cdde2b301f073439ff640570d4a93e033  biopython-1.71.tar.gz
08e2123c043cbfc4faf483fd59857b7df95662ac706ad9c3c9ef34d7a41b1d2d  biopython-1.71.zip
```
