---
author: cjfields
category:
  - bioperl
  - code
  - community
  - development
  - obf
  - obf-projects
date: "2010-01-19T03:58:58+00:00"
guid: http://news.open-bio.org/news/?p=603
title: BioPerl at GMOD Meeting 2010
url: /2010/01/18/bioperl-at-gmod-meeting-2010/

---
BioPerl developers and users attended the [BioPerl satellite meeting](http://www.bioperl.org/wiki/GMOD_2010_Meeting) on January 13th, just prior to the [GMOD Meeting](http://gmod.org/wiki/January_2010_GMOD_Meeting).  Several items were covered on the agenda:

- In order to start addressing whole genome data with more lightweight objects, we are planning on setting up a lightweight Bio::SeqI object that has a flexible DB backend (i.e. Bio::DB::SeqFeature::Store or similar).  We are also contemplating adding lazy parsing for some parsers, possibly using the Bio::PullParserI methods (or similar) that Sendu Bala created.
- After a final  1.6 branch point release, we may 'freeze' BioPerl in a maintenance mode, primarily so that we can reorganize core into several more easily installed subdistributions on a branch.  New modules will essentially be additional separate repos that will depend on BioPerl core.  This reorganization has been discussed for a few years now, and as we edge closer to starting this (probably this spring) we'll announce more details.
- Some initial thoughts on how to handle circular genomes more efficiently.  We essentially do this already, but it isn't full-proof.
- Need some significant time dedicated towards GFF3-based coding (reimplement FeatureIO but allow some flexibility).  Rob Buels had started the initial run at splitting out FeatureIO, so next step is a true reimplementation.
- We don't plan on including Moose support for the immediate future, feeling that it would be better to reimplement some of the classes from scratch using Moose and similar as a BioPerl 2.0, or possibly await the impending Rakudo Perl 6 alpha and start afresh using that instead of Moose.

Anything we missed?  Anything you would like to address?  Please add comments and we'll discuss them on list.
