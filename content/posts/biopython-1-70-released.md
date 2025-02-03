---
author: peterc
category:
  - biopython
  - code
  - community
  - development
  - obf
  - obf-projects
cover:
  alt: biopython_2017_banner_white_bg
  image: /wp-content/uploads/2017/07/biopython_2017_banner_white_bg.png
date: "2017-07-11T10:45:49+00:00"
guid: https://news.open-bio.org/?p=1683
tag:
  - biopython
  - code
  - community
  - development
  - obf
  - obf-projects
  - open-source
  - release
  - releases
title: Biopython 1.70 released
url: /2017/07/11/biopython-1-70-released/

---
Dear Biopythoneers,

Source distributions of Biopython 1.70 are now available from the [downloads page](http://biopython.org/wiki/Download) on the official [Biopython website](http://biopython.org/), and the release is also [on the Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython/1.70). Windows installers and/or wheels should be available later. ( _Update: Compiled wheel packages now available for Linux, Mac OS X and Windows_).

This release of Biopython supports Python 2.7, 3.4, 3.5 and 3.6 (we have now dropped support for Python 3.3). It has also been tested on PyPy v5.7, PyPy3.5 v5.8 beta, and Jython 2.7 (although we are deprecating support for Jython).

_**New Logo:**_

Biopython now has a new [logo](http://biopython.org/wiki/Logo), contributed by Patrick Kunzmann. Drawing on our original logo (with two yellow snakes) and the current Python logo, this shows a yellow and blue snake forming a double helix.

![](https://news.open-bio.org/wp-content/uploads/2017/07/biopython_logo_l-300x200.png)![[Biopython Logo]](https://news.open-bio.org/wp-content/uploads/2013/12/biopython-300x84.jpg) _**Setup changes:**_

We now explicitly recommend installation using pip, rather than the classic "python setup.py install" approach. In a related change, we now depend on the Python package setuptools (rather than the older package distutils in the Python standard library) and have made the dependency on NumPy explicit and automatic (except on Jython).

_**License changes:**_

As of Biopython 1.69, we have started to dual-license Biopython under both our original liberal “Biopython License Agreement”, and the very similar but more commonly used “3-Clause BSD License”. A growing number of the Python files are explicitly available under either license, but most of the code remains under the “Biopython License Agreement” only. See the [LICENSE](https://github.com/biopython/biopython/blob/master/LICENSE.rst) file for more details.

_**Code changes:**_  `Bio.AlignIO` now supports Mauve's eXtended Multi-FastA (XMFA) file format under the format name "mauve" (contributed by Eric Rasche).

`Bio.ExPASy` was updated to fix fetching PROSITE and PRODOC records, and return text-mode handles for use under Python 3.

Two new arguments for reading and writing blast-xml files have been added to the Bio.SearchIO functions (read/parse and write, respectively). They are `use_raw_hit_ids` and `use_raw_query_ids`. Check out the relevant SearchIO.BlastIO documentation for a complete description of what these arguments do.

`Bio.motifs` was updated to support changes in MEME v4.11.4 output.

The `Bio.Seq` sequence objects now have a `.count_overlap()` method to supplement the Python string like non-overlap based `.count()` method.

The `Bio.SeqFeature` location objects can now be compared for equality.

In `Bio.Phylo.TreeConstruction`, the `DistanceMatrix` class (previously `_DistanceMatrix`) has a new method `.format_phylip()` to write Phylip-compatible distance matrix files (contributed by Jordan Willis).

Additionally, a number of small bugs have been fixed with further additions to the test suite, and there has been further work to follow the Python PEP8, PEP257 and best practice standard coding style.

_**Acknowledgements:**_

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Aaron Kitzmiller (first contribution)
- Adil Iqbal (first contribution)
- Allis Tauri
- Andrew Guy
- Ariel Aptekmann (first contribution)
- Ben Fulton
- Bertrand Caron (first contribution)
- Chris Rands
- Connor T. Skennerton
- Eric Rasche
- Eric Talevich
- Francesco Gastaldello
- François Coste (first contribution)
- Frederic Sapet (first contribution)
- Jimmy O'Donnell (first contribution)
- Jared Andrews (first contribution)
- John Kern (first contribution)
- Jordan Willis (first contribution)
- João Rodrigues
- Kai Blin
- Markus Piotrowski
- Mateusz Korycinski (first contribution)
- Maximilian Greil
- Michiel de Hoon
- morrme (first contribution)
- Noam Kremen (first contribution)
- Patrick Kunzmann
- Peter Cock
- Rasmus Fonseca (first contribution)
- Rodrigo Dorantes-Gilardi (first contribution)
- Sacha Laurent (first contribution)
- Sourav Singh
- Ted Cybulski (first contribution)
- Tiago Antao
- Wibowo 'Bow' Arindrarto
- Zheng Ruan

Thank you all.

P.S. You can follow [@Biopython on Twitter](https://twitter.com/Biopython) _**Checksums**_:

```
$ md5sum biopython-1.70.*
feff7a3e2777e43f9b13039b344e06ff  biopython-1.70.tar.gz
6307ab27c257fe69b9dae4bfc3052f49  biopython-1.70.zip
```

```
$ shasum -a 256 biopython-1.70.*
4a7c5298f03d1a45523f32bae1fffcff323ea9dce007fb1241af092f5ab2e45b  biopython-1.70.tar.gz
34312ce899f6c3fc9dea77ca997f9a8c228043d05284a0653577594aeb119d4f  biopython-1.70.zip
```
