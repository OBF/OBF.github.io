---
author: peterc
category:
  - biopython
  - development
date: "2008-11-02T11:54:59+00:00"
guid: http://news.open-bio.org/news/?p=184
tag:
  - biopython
title: Biopython and Python 2.6 (and Python 2.3)
url: /2008/11/02/biopython-and-python-26-and-python-23/

---
Many of you will be aware that [Python 2.6](http://www.python.org/download/releases/2.6/) was released a month ago (October 1st, 2008). This supports a lot of new syntax and functionality, but also deprecates some old modules (e.g. the sets module).

While [Biopython 1.48](http://news.open-bio.org/news/2008/09/biopython-release-148/) does mostly work with Python 2.6, we've been testing with Python 2.6 and have fixed a number of deprecations or breakages in [our CVS repository](http://www.biopython.org/wiki/CVS). If using Biopython with Python 2.6 is important to you, please help out by testing the CVS code (which needs [NumPy and not Numeric](http://news.open-bio.org/news/2008/09/biopython-numeric-and-numpy/)) and letting us know on the [mailing list](http://www.biopython.org/wiki/Mailing_lists) or [bugzilla](http://bugzilla.open-bio.org/) if we've missed anything.

The next release of Biopython _should_ support Python 2.3 to 2.6 inclusive :)

However, the bad news is that we are considering dropping support for Python 2.3 after only a couple more releases - please get in touch via the [mailing list](http://www.biopython.org/wiki/Mailing_lists) ASAP if this will cause you problems.
