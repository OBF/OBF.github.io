---
author: cjfields
category:
  - bioperl
  - community
  - development
  - documentation
  - general
  - obf
  - obf-projects
date: "2009-09-29T17:55:27+00:00"
guid: http://news.open-bio.org/news/?p=448
tag:
  - bioperl
  - fastq
title: BioPerl 1.6.1 released
url: /2009/09/29/bioperl-1-6-1-released/

---
We are pleased to announce the immediate availability of BioPerl 1.6.1, the latest release of BioPerl's core code. You can grab it here:

Via CPAN:

[http://search.cpan.org/~cjfields/BioPerl-1.6.1/](http://search.cpan.org/~cjfields/BioPerl-1.6.1/)

Via the BioPerl website:

[http://bioperl.org/DIST/BioPerl-1.6.1.tar.bz2](http://bioperl.org/DIST/BioPerl-1.6.1.tar.bz2) [http://bioperl.org/DIST/BioPerl-1.6.1.tar.gz](http://bioperl.org/DIST/BioPerl-1.6.1.tar.gz) [http://bioperl.org/DIST/BioPerl-1.6.1.zip](http://bioperl.org/DIST/BioPerl-1.6.1.zip)

The PPM for Windows should also finally be available this week, ActivePerl problems permitting (we will post more information when it becomes available).

Tons of bug fixes and changes have been incorporated into this release. For a more complete change list please see the 'Changes' file included with the distribution.

A few highlights:

- FASTQ parsing and interconversion of the three FASTQ variants (Sanger, Illumina, Solexa) now works (a concerted OBF effort!)
- Significant refactoring of Bio::Restriction methods
- Complete refactoring of Bio::Search-related tiling code, including HOWTO documentation
- GBrowse-related fixes:
- \- _berkeleydb database now autoindexes wig files and locks correctly_
- \- _add Pg, SQLite, and faster BerkeleyDB implementations_
- Infernal 1.0 output is now parsed
- New SearchIO-based parser for gmap -f9 output
- BLAST XML parsing essentially complete
- Installation via CPANPLUS should now work
- For those using Strawberry Perl on Windows, the latest build is expected to pass all tests.
- 'raw' sequence format now parsed by line or optionally as a single sequence
- SCF parsing/writing now round-trips
- Demo code for using RPS-BLAST and Bio::Tools::Run::RemoteBlast
- Bio::Tools::SeqPattern now has a backtranslate() method
- Bio::Tree::Statistics now has methods to calculate Fitch-based score, internal trait values, statratio(), sum of leaf distances
- Scripts
- _\- update to bp\_seqfeature\_load for SQLite_
- _\- hivq.pl - commmand-line interface to Bio::DB::HIV_
- _\- fastam9\_to\_table - fix for MPI output_
- _\- gccalc - total stats_
- _\- einfo - simple script to find up-to-date NCBI databases, list field and link values for a specific database_

We will shortly release updates for BioPerl-db, BioPerl-run, and BioPerl-network. Enjoy!

chris
