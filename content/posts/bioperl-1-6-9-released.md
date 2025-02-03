---
author: cjfields
category:
  - bioperl
  - development
  - general
  - obf
  - obf-projects
date: "2011-04-14T20:03:27+00:00"
guid: http://news.open-bio.org/news/?p=822
title: BioPerl 1.6.9 released
url: /2011/04/14/bioperl-1-6-9-released/

---
[BioPerl 1.6.9](http://search.cpan.org/~cjfields/BioPerl-1.6.900/) is now available in CPAN.  In this release:

- Refactored Bio::Species/Bio::Tree
- New SeqIO modules (gbxml, msout, mbsout)
- Updates for perl 5.12
- Bio::Assembly support for SAM/BAM, Newbler, ace output
- Bio::DB::SeqFeature updates
- PAML updated to work with v. 4.4d
- lots of various bug fixes, around 50

Just to note, this is the first release after we reworked the Build.PL system, so we will probably hit a few speed bumps along the way.  This is in effort to simplify the process for further work this summer on modularizing BioPerl, but it also makes new releases much easier to make.  In particular, this has only been tested on Ubuntu Linux and Mac OS X (no Windows testing has occurred yet).    Please post if there are any problems.

Enjoy!
