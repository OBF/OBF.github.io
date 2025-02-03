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
date: "2016-06-08T17:39:28+00:00"
guid: https://news.open-bio.org/?p=1513
tag:
  - biopython
  - development
  - open-source
  - release
  - releases
title: Biopython 1.67 released
url: /2016/06/08/biopython-1-67-released/

---
This was long over-due, but Biopython 1.67 was released earlier today. The most recent delay was due to migrating our website from MediaWiki to GitHub Pages earlier this year, following an OBF server failure.

Source distributions and Windows installers for Biopython 1.67 are now available from the [downloads page](http://biopython.org/wiki/Download) on the [official Biopython website](http://biopython.org/), and the release is also on the [Python Package Index (PyPI)](https://pypi.python.org/pypi/biopython/1.67).

This release of Biopython supports Python 2.6, 2.7, 3.3, 3.4 and 3.5, but support for Python 2.6 is considered to be deprecated. It has also been tested on PyPy 5.0, PyPy3 version 2.4, and Jython 2.7.

Comparison of SeqRecord objects until now has used the default Python object comparison (are they the same instance in memory?). This can be surprising, but comparing all of the attributes would be too complex. As of this release attempting to compare SeqRecord objects should raise an exception instead. If you want the old behaviour, use id(record1) == id(record2) instead.

New experimental module Bio.phenotype is for working with Phenotype Microarray plates in JSON and the machine vendor's CSV format (contributed by Marco Galardini).

Following the convention used elsewhere in Biopython, there is a new function Bio.KEGG.read(...) for parsing KEGG files expected to contain a single record only - the existing function Bio.KEGG.parse(...) is intended to be used to iterate over multi-record files.

When a gap character is defined, Bio.Seq will now translate gap codons (e.g. "---") into a single gap ("-") in the protein sequence. The gap character is inferred from the Seq object's alphabet, but it can also be passed as an argument to the translate method.

The new NCBI genetic code table 25, covering Candidate Division SR1 and Gracilibacteria, has been added to Bio.Data (and the translation functionality).

The Bio.Entrez interface will automatically use an HTTP POST rather than HTTP GET if the URL would exceed 1000 characters. This is based on NCBI guidelines and the fact that very long queries like complex searches can otherwise trigger an HTTP Error 414 Request URI too long.

Foreign keys are now used when creating BioSQL databases with SQLite3 (this was not possible until SQLite version 3.6.19). The BioSQL taxonomy code now updates the taxon table left/right keys when updating the taxonomy.

There have been some fixes to the MMCIF structure parser which now uses identifiers which better match results from the PDB structure parse.

The restriction enzyme list in Bio.Restriction has been updated to the May 2016 release of REBASE.

The mmCIF parser in Bio.PDB.MMCIFParser has been joined by a second version which only looks at the ATOM and HETATM lines and can be much faster.

The Bio.KEGG.REST will now return unicode text-based handles, except for images which remain as binary bytes-based handles, making it easier to use with the mostly text-based parsers in Biopython.

Note that the BioSQL test configuration information is now in a new file Tests/biosql.ini rather than directly in Tests/test\_BioSQL\_\*.py as before. You can make a copy of the provided example file Tests/biosql.ini.sample as Tests/biosql.ini and edit this if you wish to run the BioSQL tests.

Additionally, a number of small bugs have been fixed with further additions to the test suite, and there has been further work to follow the Python PEP8 standard coding style, and in converting our docstring documentation to use the reStructuredText markup style.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Aaron Rosenfeld (first contribution)
- Anders Pitman (first contribution)
- Barbara Mühlemann (first contribution)
- Ben Fulton
- Ben Woodcroft (first contribution)
- Brandon Invergo
- Brian Osborne (first contribution)
- Carlos Pena
- Chaitanya Gupta (first contribution)
- Chris Warth (first contribution)
- Christiam Camacho (first contribution)
- Connor T. Skennerton
- David Koppstein (first contribution)
- Eric Talevich
- Jacek Śmietański (first contribution)
- João D Ferreira (first contribution)
- João Rodrigues
- Joe Cora (first contribution)
- Kai Blin
- Leighton Pritchard
- Lenna Peterson
- Marco Galardini (first contribution)
- Markus Piotrowski
- Matt Ruffalo (first contribution)
- Matteo Sticco (first contribution)
- Nader Morshed (first contribution)
- Owen Solberg (first contribution)
- Peter Cock
- Steve Bond (first contribution)
- Terry Jones (first contribution)
- Vincent Davis
- Zheng Ruan

Again this list of contributors is longer than usual, which is good, but partly reflects the delay since our last release. My apologies.
