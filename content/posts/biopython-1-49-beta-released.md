---
author: peterc
category:
  - biopython
  - development
date: "2008-11-07T16:45:48+00:00"
guid: http://news.open-bio.org/news/?p=194
tag:
  - biopython
title: Biopython 1.49 beta released
url: /2008/11/07/biopython-149-beta-released/

---
We are pleased to announce a beta release of Biopython 1.49. There are been some significant changes since [Biopython 1.48](http://news.open-bio.org/news/2008/09/biopython-release-148/) was released two months ago, which is why we are initially releasing a beta for wider testing.

As [previously announced](http://news.open-bio.org/news/2008/09/biopython-numeric-and-numpy/), the big news is that Biopython now uses NumPy rather than its precursor Numeric (the original Numerical Python library).

As in the previous releases, Biopython 1.49 beta supports Python 2.3, 2.4 and 2.5 but should now also work fine on [Python 2.6](http://www.python.org/download/releases/2.6/). Please note that we intend to drop support for Python 2.3 in a couple of releases time (see [previous news article](http://news.open-bio.org/news/2008/11/biopython-and-python-26-and-python-23/)).

We also have some new functionality, starting with the basic sequence object (the Seq class) which now has more methods. This encourages a more object orientated coding style, and makes basic biological operations like transcription and translation more accessible and discoverable.

Our [BioSQL interface](http://www.biopython.org/wiki/BioSQL) can now optionally fetch the NCBI taxonomy on demand when loading sequences (via Bio.Entrez) allowing you to populate the taxon/taxon\_name tables gradually. Also, BioSQL should now work with the psycopg2 driver for PostgreSQL (as well as the older psycopg driver).

Finally, our old parsing infrastructure (Martel and Bio.Mindy) is now considered to be deprecated, meaning mxTextTools is no longer required to use Biopython. This should not affect any of the typically used parsers (e.g. [Bio.SeqIO](http://www.biopython.org/wiki/SeqIO) and [Bio.AlignIO](http://www.biopython.org/wiki/AlignIO)).

So, if you are feeling brave and know the risks, please try out Biopython 1.49 beta, and let us know on the [mailing lists](http://www.biopython.org/wiki/Mailing_lists) if it works, or more importantly if something doesn't.

We'd also like feedback on the updated [Biopython Tutorial and Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html) (also available in [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)).

Source distributions and Windows installers are available from the Biopython website: [biopython.org](http://biopython.org)

Thanks!

-Peter on behalf of the Biopython developers
