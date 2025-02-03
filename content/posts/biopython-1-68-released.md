---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - obf
  - obf-projects
cover:
  alt: Biopython 2003 Logo
  image: /wp-content/uploads/2013/12/biopython.jpg
date: "2016-08-26T16:23:42+00:00"
guid: https://news.open-bio.org/?p=1540
tag:
  - biopython
title: Biopython 1.68 released
url: /2016/08/26/biopython-1-68-released/

---
Dear Biopythoneers,

Source distributions and Windows installers for Biopython 1.68 are now available from the [downloads page](http://biopython.org/wiki/Download) on the official [Biopython website](http://biopython.org/), and the release is also [on the Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython/1.68).

This release of Biopython supports Python 2.6, 2.7, 3.3, 3.4 and 3.5, but **this will be our final release to run on Python 2.6.** It has also been tested on PyPy 5.0, PyPy3 version 2.4, and Jython 2.7.

Bio.PDB has been extended to parse the RSSB's new binary Macromolecular Transmission Format (MMTF, see [http://mmtf.rcsb.org](http://mmtf.rcsb.org)), in addition to the mmCIF and PDB file formats (contributed by Anthony Bradley). This requires an optional external dependency on the [mmtf-python library](https://github.com/rcsb/mmtf-python).

Module Bio.pairwise2 has been re-written (contributed by Markus Piotrowski). It is now faster, addresses some problems with local alignments, and also now allows gap insertions after deletions, and vice versa, inspired by the [preprint from Flouri et al](http://dx.doi.org/10.1101/031500).

The two sample graphical tools SeqGui (Sequence Graphical User Interface) and xbbtools were rewritten (SeqGui) or updated (xbbtools) using the tkinter library (contributed by Markus Piotrowski). SeqGui allows simple nucleotide transcription, back-transcription and translation into amino acids using Bio.Seq internally, offering of the NCBI genetic codes supported in Biopython. xbbtools is able to open Fasta formatted files, does simple nucleotide operations and translations in any reading frame using one of the NCBI genetic codes. In addition, it supports standalone Blast installations to do local Blast searches.

New [NCBI genetic code table](https://www.ncbi.nlm.nih.gov/Taxonomy/Utils/wprintgc.cgi) 26 (Pachysolen tannophilus Nuclear Code) has been added to Bio.Data (and the translation functionality), and table 11 is now also available under the alias Archaeal.

In line with [NCBI website HTTPS changes](https://www.ncbi.nlm.nih.gov/news/06-10-2016-ncbi-https/), Biopython now uses HTTPS rather than HTTP to connect to the NCBI Entrez and QBLAST API.

Additionally, a number of small bugs have been fixed with further additions to the test suite, and there has been further work to follow the Python PEP8 and best practice standard coding style.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Anthony Bradley (first contribution)
- Ben Fulton
- Carlos Pena
- Connor T. Skennerton
- Iddo Friedberg
- Kai Blin
- Kristian Davidsen (first contribution)
- Markus Piotrowski
- Olivier Morelle (first contribution)
- Peter Cock
- Tiago Antao
- Travis Wrightsman
- Uwe Schmitt (first contribution)
- Xiaoyu Zhuo (first contribution)

Thank you all.

P.S. You can follow [@Biopython on Twitter](https://twitter.com/Biopython)

Checksums:

```
$ md5sum biopython-1.68.*
078e915185485a5327937029b7577ddc biopython-1.68.tar.gz
362e964543a424a2f7585ea4008ea834 biopython-1.68.win32-py2.6.exe
772d07d9a6490d674688d00ede2bdfe9 biopython-1.68.win32-py2.7.exe
fda2d1c8d4a7862f6af85122c86fcd0f biopython-1.68.win32-py2.7.msi
8de95a90704f15f4c22d5359dbc54b75 biopython-1.68.win32-py3.3.exe
92f40105761520daeeb9128254a8bc94 biopython-1.68.win32-py3.3.msi
b1cd3f6b4ad1096347d5019c68128dac biopython-1.68.win32-py3.4.exe
9403b9b0d01c22b49edb34e2164c31de biopython-1.68.win32-py3.4.msi
72202792fc387376c07e28997ece181f biopython-1.68.win32-py3.5.exe
ff0cfc6c835ddf890b69ba872fb46b39 biopython-1.68.win32-py3.5.msi
adb3e8ce60b02b3b46330bbca68f9732 biopython-1.68.zip
```

```
$ shasum -a 256 biopython-1.68.*
d1dc09d1ddc8e90833f507cf09f80fa9ee1537d319058d1c44fe9c09be3d0c1f  biopython-1.68.tar.gz
09449d7204c65e6010545092f2bc1dc662a0b5f6a873e52a08e19392f935fdb7  biopython-1.68.win32-py2.6.exe
a7c2fe52ce8dcf503a492e4ee006dd8bc62faa77078d04c92abdbf7713bf2166  biopython-1.68.win32-py2.7.exe
f92dfefc9a4ee61dda838a61d73a38b55552a1771ce411505009a48702aefd41  biopython-1.68.win32-py2.7.msi
bce6a4cece7b75650d6a478f4ed9d7d1a5351df42a1820866a0cbd74c254565d  biopython-1.68.win32-py3.3.exe
85bd5d499400e594f77d297966f56c139499711513b9cd24b87fece5a0463fbe  biopython-1.68.win32-py3.3.msi
05c1f59933ef35ecb838649f6fabacb823f2a48c2498ed57ac59a6b3629b5369  biopython-1.68.win32-py3.4.exe
10928347029bc6b0b76567d5f6026a8a002bd3502a7ceeaded7d566938db4bef  biopython-1.68.win32-py3.4.msi
5d08e4de11f920ec5207e10d264fceb837e2000843a56fd684e0ee2dfb948fe5  biopython-1.68.win32-py3.5.exe
299888c32b36f32542775952e7b863bd9c3d362f61a69b7d8a136a63aeabec36  biopython-1.68.win32-py3.5.msi
986a0fa6919d2b51959259011dd0674b115383237e109c5a55c37cb18eef999b  biopython-1.68.zip
```

 _Updated_ 29 August 2016 to include the Python 3.5 installer checksums.
