---
author: stajich
category:
  - bioperl
  - development
date: "2008-12-09T19:49:57+00:00"
guid: http://news.open-bio.org/news/?p=216
tag:
  - bioperl
  - development
  - releases
title: BioPerl 1.6 preparations
url: /2008/12/09/bioperl-16-preparations/

---
[BioPerl](http://bioperl.org/) is preparing for version 1.6 release in the coming months. As part of this some restructuring and simplification of the packaging is occurring.

- [Bio-Graphics has been split off](http://lists.open-bio.org/pipermail/bioperl-l/2008-December/028597.html) into its own package back on [Sourceforge](http://gmod.cvs.sourceforge.net/viewvc/gmod/Bio-Graphics) to allow for a separate release schedule. It will be uploaded to CPAN as a separate package. In the future other small groups of modules will also be split off from the Core.  Eventually the Core will constitute components that will be the main parsers and data objects while less-common use cases or tightly related modules (like bioperl-network) will be released to CPAN on their own.
- [Tests have been split off](http://lists.open-bio.org/pipermail/bioperl-l/2008-December/028590.html) into smaller chunks.
- [Anyone who has contributed to the code](http://lists.open-bio.org/pipermail/bioperl-l/2008-December/028655.html) and feels their name should be included in the authors' list needs to either add it or email the mailing list or Chris Fields.
- S [endu has moved](http://lists.open-bio.org/pipermail/bioperl-l/2008-December/028649.html) ModuleBuildBioperl and BioperlTest into Bio::Root
- Bugs are being triaged at [bugzilla](http://bugzilla.open-bio.org) so if you have any opinions you can vote on the bugs in the queue.
