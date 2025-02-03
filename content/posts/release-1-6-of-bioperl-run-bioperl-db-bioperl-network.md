---
author: cjfields
category:
  - bioperl
  - code
  - development
  - documentation
date: "2009-02-26T05:18:32+00:00"
guid: http://news.open-bio.org/news/?p=241
tag:
  - bioperl
title: Release 1.6 of BioPerl-run, BioPerl-db, BioPerl-network
url: /2009/02/26/release-16-of-bioperl-run-bioperl-db-bioperl-network/

---
All,

I am proud to announce that the 1.6 release for BioPerl-run, BioPerl-
db, and BioPerl-network are now available by direct download and via
CPAN. These are designated as 1.006000, with a requirement for
BioPerl 1.6 and higher (1.006000).

FIXED:

1) Bio::Tools::Run::Primer3 now accepts primer3 or primer3\_core as
executable names
2) Bio::Tools::Run::Vista tests now pass if Vista.jar is installed.
3) bug fix in bioperl-network

What remains for the 1.6 release series:

\\* Documentation, Documentation, and Documentation. I haven't had much
time unfortunately to work on documentation, primarily for BUGS/
INSTALL/README etc within db/run/network (the latter has been mainly
updated by Brian O.) I will attempt to update these for the next
point release, tentatively scheduled for mid-April.

NOTE (so there is no confusion): the BioPerl-run archive is designated
as BioPerl-1.6.1.tar.gz. This is due to a small off-by-one bug in the
test suite that passed for me locally but fails if primer3 isn't
installed. This unfortunately required a reupload to PAUSE. However,
the minimal core version version required is still 1.006000.

Related to the above, I will sort out the versioning issues for the
next point release as we arrive closer to it. If needed we can bump
the point release up to 1.6.2 to bring everything in sync.

Here they are!

BioPerl-run:

http://bioperl.org/DIST/BioPerl-run-1.6.1.tar.bz2
http://bioperl.org/DIST/BioPerl-run-1.6.1.tar.gz
http://bioperl.org/DIST/BioPerl-run-1.6.1.zip

BioPerl-db:

http://bioperl.org/DIST/BioPerl-db-1.6.0.tar.bz2
http://bioperl.org/DIST/BioPerl-db-1.6.0.tar.gz
http://bioperl.org/DIST/BioPerl-db-1.6.0.zip

BioPerl-network:

http://bioperl.org/DIST/BioPerl-network-1.6.0.tar.bz2
http://bioperl.org/DIST/BioPerl-network-1.6.0.tar.gz
http://bioperl.org/DIST/BioPerl-network-1.6.0.zip

SIGNATURES:

http://bioperl.org/DIST/SIGNATURES.md5

Cheers!

chris
