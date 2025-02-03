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
date: "2012-02-24T15:09:04+00:00"
guid: http://news.open-bio.org/news/?p=872
tag:
  - biopython
  - development
  - news
  - open-source
  - release
  - releases
title: Biopython 1.59 released
url: /2012/02/24/biopython-1-59-released/

---
Source distributions and Windows installers for **Biopython 1.59** are now available from the [downloads page](http://biopython.org/wiki/Download) on the [Biopython website](http://biopython.org/) and from the [Python Package Index (PyPI)](http://pypi.python.org/pypi/biopython).

### Platforms/Deployment

We currently support [Python](http://python.org) 2.5, 2.6 and 2.7 and also test under [Jython](http://jython.org) 2.5 (which does not cover NumPy). Please note that this release will not work on Python 2.4

Most functionality is also working under Python 3.1 and 3.2 (including modules using [NumPy](http://numpy.scipy.org/)), and under [PyPy](http://pypy.org/) (excluding our NumPy dependencies). We are now encouraging early adopters to help beta testing on these platforms.

The installation setup.py now supports 'install\_requires' when setuptools is installed. This avoids the manual dialog when installing Biopython via easy\_install or pip and numpy is not installed. It also allows user libraries that require Biopython to include it in their install\_requires and get automatic installation of dependencies.

### Features

New module `Bio.TogoWS` offers a wrapper for the [TogoWS REST API](http://togows.dbcls.jp/site/en/rest.html), a web service based in Japan offering access to KEGG, DDBJ, PDBj, CBRC plus access to some NCBI and EBI resources including PubMed, GenBank and UniProt. This is much easier to use than the NCBI Entrez API, but should be especially useful for Biopython users based in Asia.

The [NCBI Entrez Fetch](http://eutils.ncbi.nlm.nih.gov/corehtml/query/static/efetch_help.html) function `Bio.Entrez.efetch` has been updated to handle the NCBI's stricter handling of multiple ID arguments in EFetch 2.0 (released February 2012, see this [announcement](http://www.ncbi.nlm.nih.gov/mailman/pipermail/utilities-announce/2012-February/000086.html)), however the NCBI have also changed the `retmode` default argument so _you_ may need to make this explicit. e.g. add `retmode="text"` to your EFetch calls (see this [announcement](http://www.ncbi.nlm.nih.gov/mailman/pipermail/utilities-announce/2012-February/000085.html)).

The position objects used in `Bio.SeqFeature` now act almost like integers, making dealing with fuzzy locations in EMBL/GenBank files much easier. Also the `SeqFeature`'s strand and any database reference are now properties of the `FeatureLocation` object (a more logical placement), with proxy methods for backwards compatibility.

`Bio.Graphics.BasicChromosome` has been extended to allow simple sub-features to be drawn on chromosome segments, suitable to show the position of genes, SNPs or other loci.

`Bio.Graphics.GenomeDiagram` has been extended to allow [cross-links between tracks](http://news.open-bio.org/news/2012/03/cross-links-in-genomediagram/), and track specific start/end positions for showing regions. This can be used to imitate the output from the [Artemis Comparison Tool (ACT)](http://www.sanger.ac.uk/resources/software/act/). Also, a new attribute circle\_core makes it easier to have an empty space in the middle of a circular diagram (see tutorial).

Note `Bio.Graphics` requires the [ReportLab library](http://www.reportlab.com/software/opensource/).

`Bio.Align.Applications` now includes a wrapper for command line tool [Clustal Omega](http://www.clustal.org/omega/) for protein multiple sequence alignment.

`Bio.AlignIO` now supports sequential [PHYLIP](http://evolution.genetics.washington.edu/phylip.html) files (as well as interlaced PHYLIP files) as a separate format variant.

Additionally there have been other minor bug fixes and more unit tests, and updates to the documentation including the [Biopython Tutorial](http://biopython.org/DIST/docs/tutorial/Tutorial.html) ( [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)).

### Contributors

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Andreas Wilm (first contribution)
- Alessio Papini (first contribution)
- Brad Chapman
- Brandon Invergo
- Connor McCoy
- Eric Talevich
- João Rodrigues
- Konrad Förstner (first contribution)
- Michiel de Hoon
- Matej Repič (first contribution)
- Leighton Pritchard
- Peter Cock
