---
author: cjfields
category:
  - bioperl
date: "2016-09-25T15:10:29+00:00"
guid: https://news.open-bio.org/?p=1554
tag:
  - bioperl
  - obf-projects
  - release
title: BioPerl v1.7.0 released
url: /2016/09/25/bioperl-v1-7-0-released/

---
We are happy to announce the long-awaited release of BioPerl v1.7.0.  The release is now [available on CPAN](https://metacpan.org/release/BioPerl) and [Github](https://github.com/bioperl/bioperl-live/releases/tag/release-1-7-0).

During this release series, we will move some extraneous code to separate repositories and CPAN releases, primarily to reduce the number of dependencies required for BioPerl installation (in many cases for modules that are never used) and also reduce maintenance overhead.

This may only impact you if your code incorrectly list the immediate downstream dependencies that you utilize.  For example, we have now moved Bio::Coordinate code to a separate repo and will release it as a separate distribution on CPAN.  If your tools require Bio::Coordinate::Result and list this module as a dependency, you should be fine: a separate Bio::Coordinate release should pull in the latest BioPerl, until then it would pull in the last BioPerl release with that module.  However, if you list Bio::Root::Root or Bio::Perl as a dependency to pull in Bio::Coordinate::Result, your installation will not work correctly (as Bio::Root::Root is not the proper code dependency).  We can work with distributions affected to help with this transition and will be more consistently evaluating reverse dependencies on CPAN for upcoming releases as we split out code.  Please post [issues on Github](https://github.com/bioperl/bioperl-live/issues) if you see problems with your code and the latest release.

In addition to the above, modules relying on a remote web services that are no longer active or pose a security issue will be deprecated for use and (in some cases) immediately removed.  Normally these don't affect normal tests, but we have noticed some remote services out of our control causing problems with network-requiring or release testing.

In addition, the following changes have been made since the last release:

- NCBI HTTPS support \[Mark Johnson (aka mjohnson) and others\]
- We have migrated to Github Pages. This was actually planned, but the
  recent OBF server compromise forced our hand. Brian Osborne \[bosborne\] took this under his wing to move docs and has done a tremendous amount of work formatting the site and working out some of the idiosyncracies with the new Jekyll-based design. Mark Jensen, Paul Cantalupo and Franscison Ossandon also helped. Kudos!!
- Similarly, the official issue tracker is now Github Issues. This has been updated in the relevant documentation bits (we hope!)
- Previously deprecated modules have been removed
  - Bio::Tools::Infernal, Bio::Tools::ERPIN, Bio::Tools::RNAMotif
  - Bio::DB::SeqHound has been removed due to the service no longer being available
  - Bio::Tools::Analysis::Protein::Mitoprot has been removed for security reasons due to the server no longer having a valid cert
  - Bio::EUtilities, Bio::Biblio are now separate releases on CPAN
  - Bio::Coordinate, Bio::SearchIO::blastxml, Bio::SearchIO::Writer::BSMLResultWriter are now separate releases to be released independently on CPAN
- Docker instances of tagged releases are available! \[hlapp\]
- Bio::SearchIO::infernal
  - Issue #131: added CMSEARCH parsing support for Infernal 1.1 \[pcantalupo\]
  - Bio::Search::HSP::ModelHSP: Added a 'noncanonical\_string' method to retrieve the NC line from CMSEARCH reports \[pcantalupo\]
  - Bio::Search::Result::INFERNALResult - Added new module to represent features of Infernal reports \[pcantalupo\]
- SQLite support for Bio::DB::Taxonomy - \[cjfields\]
- WrapperBase quoted option values \[majensen\]
- Various documentation fixes and updates \[bosborne\]

And many many bug fixes.  Please see the Changes file with the distribution.

Thanks, and enjoy!

chris
