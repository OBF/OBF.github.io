---
author: peterc
category:
  - biopython
  - code
  - community
  - development
  - obf-projects
date: "2009-06-23T15:42:16+00:00"
guid: http://news.open-bio.org/news/?p=373
tag:
  - biopython
  - fastq
title: Biopython 1.51 beta released
url: /2009/06/23/biopython-151-beta-released/

---
A _beta_ release for Biopython 1.51 is now available for download and testing.

In the two months since [Biopython 1.50](http://news.open-bio.org/news/2009/04/biopython-release-150/) was released, we have introduced support for writing features in GenBank files using [Bio.SeqIO](http://biopython.org/wiki/SeqIO), extended [SeqIO's support for the FASTQ format](http://news.open-bio.org/news/2009/03/biopython-next-gen-sequencing/) to include files created by Illumina 1.3+, and added a new set of application wrappers for alignment programs, and made numerous tweaks and bug fixes.

All the new features have been tested by the dev team but it's possible there are cases that we haven't been able to foresee and test, especially for the GenBank feature writer (as there as just so many possible odd fuzzy feature locations).

Note that as previously announced, Biopython no longer supports [Python 2.3](http://news.open-bio.org/news/2009/05/dropping-python23-support/), and our deprecated parsing infrastructure (Martel and Bio.Mindy) has been removed.

Source distributions and Windows installers are available from the [downloads](http://biopython.org/wiki/Download) page on the [Biopython website (biopython.org)](http://biopython.org).

We are interested in getting feedback on the beta release as a whole, but especially on the new features and the [Biopython Tutorial and Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html) ( [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)).

So, gather your courage, download the release, try it out and let us know what works and what doesn't through the [mailing lists](http://www.biopython.org/wiki/Mailing_lists) (or [bugzilla](http://bugzilla.open-bio.org/)).
