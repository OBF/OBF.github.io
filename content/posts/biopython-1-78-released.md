---
author: chebizarro
category:
  - biopython
  - blogroll
  - code
  - development
  - obf-projects
date: "2020-09-04T12:11:00+00:00"
guid: https://www.open-bio.org/?p=5057
tag:
  - biopython
title: Biopython 1.78 released
url: /2020/09/04/biopython-1-78-released/

---
Biopython 1.78 has been released and is available from our [website](https://biopython.org/wiki/Download) and [PyPI](https://pypi.python.org/pypi/biopython/1.78).

The main change is that `Bio.Alphabet` is no longer used. In some cases you will now have to specify expected letters, molecule type (DNA, RNA, protein), or gap character explicitly. Please consult the updated [Tutorial](http://biopython.org/DIST/docs/tutorial/Tutorial.html) and [API documentation](https://biopython.org/docs/1.78/api/) for guidance. This simplification has sped up many `Seq` object methods. See [https://biopython.org/wiki/Alphabet](https://biopython.org/wiki/Alphabet) for more information.

`Bio.SeqIO.parse()` is faster with "fastq" format due to small improvements in the `Bio.SeqIO.QualityIO` module.

The `SeqFeature` object's `.extract()` method can now be used for  
trans-spliced locations via an optional dictionary of references.

As in recent releases, more of our code is now explicitly available under either our original " _Biopython License Agreement_", or the very similar but more commonly used " _3-Clause BSD License_". See the `LICENSE.rst` file for more details.

Additionally, a number of small bugs and typos have been fixed with additions to the test suite. There has been further work to follow the Python PEP8, PEP257 and best practice standard coding style, and all of the tests have been reformatted with the `black` tool to match the main code base.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Adam Sjøgren (first contribution)
- Carlos Pena
- Chris Daley
- Chris Rands
- Christian Brueffer
- Damien Goutte-Gattat
- João Rodrigues
- João Vitor F Cavalcante (first contribution)
- Marie Crane
- Michiel de Hoon
- Peter Cock
- Sergio Valqui
- Yogesh Kulkarni (first contribution)
- Zheng Ruan
