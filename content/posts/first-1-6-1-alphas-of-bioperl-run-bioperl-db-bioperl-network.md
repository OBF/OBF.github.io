---
author: cjfields
category:
  - bioperl
  - code
  - development
  - obf
  - obf-projects
date: "2009-10-01T16:40:51+00:00"
guid: http://news.open-bio.org/news/?p=453
tag:
  - bioperl
title: First 1.6.1 alphas of BioPerl-Run, BioPerl-DB, BioPerl-Network
url: /2009/10/01/first-alphas-of-bioperl-run-bioperl-db-bioperl-network/

---
Running a bit late on this, so just a quick note that the first alphas for BioPerl-Run, BioPerl-DB, and BioPerl-Network have been uploaded to CPAN:

- [BioPerl-Run](http://search.cpan.org/~cjfields/BioPerl-Run-1.6.1_001/)
- [BioPerl-DB](http://search.cpan.org/~cjfields/BioPerl-DB-1.6.0_001/)
- [BioPerl-Network](http://search.cpan.org/~cjfields/BioPerl-Network-1.6.0_001/)

They can also be downloaded from the BioPerl website:

[http://bioperl.org/DIST/RC/](http://bioperl.org/DIST/RC/)

This is the first run where we've switched to a regular Module::Build installation, so expect some initial bumps! There are a few initial problems that I plan on addressing soon, the main one being none of the modules are assigned version numbers (this may be a consequence of not pulling the version from a specific module). The other, more serious one, is that the Build.PL script checks for DBI but isn't checking for any compatible DBD::\* adaptors for BioPerl-DB (so it fails tests if DBI is installed). We have code in core to check for DBI drivers, so I may adapt that for BioPerl-DB.

Enjoy!

chris
