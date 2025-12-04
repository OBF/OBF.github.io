---
author: JoaoRodrigues
category:
  - biopython
  - obf-projects
cover:
  alt: biopython
  image: /wp-content/uploads/2019/02/biopython.png
date: "2021-06-03T23:03:10+00:00"
guid: https://www.open-bio.org/?p=5603
tag:
  - biopython
title: Biopython 1.79 released!
url: /2021/06/03/biopython-1-79-released/

---
Biopython 1.79 has been released and is available from our [website](https://biopython.org/wiki/Download) and [PyPI](https://pypi.python.org/pypi/biopython/1.79).

This is the final release supporting Python version 3.6. It also supports Python versions 3.7, 3.8, and 3.9, as well as PyPy 3.6.1 v7.1.1.

The major changes in this version are listed below:

\- The `Seq` and `MutableSeq` classes in `Bio.Seq` now inherit from the same base class, ensuring their mutual consistency. In addition, both classes now store sequence data as `bytes` and `bytearray` objects, respectively.

\- Empty or unknown sequences can now be created directly by passing `None` to the `Seq` class, instead of using `UnknownSeq`. This latter class is now deprecated and will be removed in a future version of Biopython.

\- A new module `Bio.PDB.SASA` implements the Shrake-Rupley algorithm to calculate solvent accessible areas natively, without requiring third-party tools such as _DSSP_ or _NACCESS_.

\- Other minor improvements to the `Bio.PDB` module include a new `center_of_mass()` method to calculate the center of mass or center of gravity of any Entity subclass (e.g. Structure, Chain, or Residue).

\- Changes in the KEGG `KGML_Pathway` module now produce output files compliant with KGML v0.7.2. In addition, `Bio.UniProt.GOA` now parses GPI files version 1.2.

As in recent releases, more of our code is now explicitly available under either our original “ _Biopython License Agreement_“, or the very similar but more commonly used “ _3-Clause BSD License_“. See the `LICENSE.rst` file for more details.

Additionally, a number of small bugs and typos have been fixed with further additions to the test suite. There has been further work to follow the Python PEP8, PEP257 and best practice standard coding style, and more of the code style has been reformatted with the `black` tool.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

\- Damien Goutte-Gattat
\- Gert Hulselmans
\- João Rodrigues
\- Markus Piotrowski
\- Sergio Valqui
\- Suyash Gupta
\- Vini Salazar (first contribution)
\- Leighton Pritchard
