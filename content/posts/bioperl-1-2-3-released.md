---
author: osborne
category:
  - bioperl
date: "2003-09-18T23:12:19+00:00"
guid: http://news.open-bio.org/news/?p=112
summary: |-
  Bioperl 1.2.3

  On behalf of the Bioperl developers, we are pleased to announce the release of Bioperl 1.2.3. This is the set of Core libraries which constitutes Bioperl and covers areas like Sequence file parsing, Sequence Feature representations, Database access to flatfile web-based sequence databases, Alignment parsing and manipulation, parsing of and data representation of output from a majority of standard bioinformatics tools, and many more features.

  This release constitutes several major bugfixes from the 1.2.2 release earlier this summer and provides some new minor functionality improvements. This release is intended to be compatible with code which has been programmed using the API in the 1.2.x series of releases.

  The release is available as always from [http://bioperl.org/DIST/](http://bioperl.org/DIST/).
title: Bioperl 1.2.3 Released
url: /2003/09/18/bioperl-123-released/

---
Bioperl 1.2.3

On behalf of the Bioperl developers, we are pleased to announce the release of Bioperl 1.2.3. This is the set of Core libraries which constitutes Bioperl and covers areas like Sequence file parsing, Sequence Feature representations, Database access to flatfile web-based sequence databases, Alignment parsing and manipulation, parsing of and data representation of output from a majority of standard bioinformatics tools, and many more features.

This release constitutes several major bugfixes from the 1.2.2 release earlier this summer and provides some new minor functionality improvements. This release is intended to be compatible with code which has been programmed using the API in the 1.2.x series of releases.

The release is available as always from [http://bioperl.org/DIST/](http://bioperl.org/DIST/).

Bioperl 1.2.3

On behalf of the Bioperl developers, I am pleased to announce the
release of Bioperl 1.2.3. This is the set of Core libraries which constitutes
Bioperl and covers areas like Sequence file parsing, Sequence Feature
representations, Database access to flatfile and webbased sequence
databases, Alignment parsing and manipulation, parsing of and data
representation of output from a majority of standard bioinformatics
tools, and many more features.

This release constitutes several major bugfixes from the 1.2.2 release
earlier this summer and provides some new minor functionality
improvements. This release is intended to be compatible with code
which has been programmed using the API in the 1.2.x series of releases.

The release is available as always from
[http://bioperl.org/DIST/](http://bioperl.org/DIST/) [http://bioperl.org/DIST/bioperl-1.2.3.tar.bz2](http://bioperl.org/DIST/bioperl-1.2.3.tar.bz2) [http://bioperl.org/DIST/bioperl-1.2.3.tar.gz](http://bioperl.org/DIST/bioperl-1.2.3.tar.gz) [http://bioperl.org/DIST/bioperl-1.2.3.zip](http://bioperl.org/DIST/bioperl-1.2.3.zip)

As well as from mirrors generously provided by Don Gilbert at Indiana
University
[http://iubio.bio.indiana.edu/](http://iubio.bio.indiana.edu/)

MD5 signatures for the release files
c64219b6540a722e781a53aea215ebc8 bioperl-1.2.3.tar.bz2
72b4a23f7372e820a7a7d9a72e7a0e76 bioperl-1.2.3.tar.gz
e3bef5ca6ec6692bc253b75046100b64 bioperl-1.2.3.zip

HTML-ized documentation for the release is available from the
documentation website [http://doc.bioperl.org/](http://doc.bioperl.org/) [http://doc.bioperl.org/releases/bioperl-1.2.3/](http://doc.bioperl.org/releases/bioperl-1.2.3/)

Related Projects
\-\-\--------------

The Generic Genome Browser which depends on bioperl will
likely release a new version which will utilize features in bioperl
1.2.3. This is coordinated by Lincoln Stein and Scott Cain. Code is available
from the project site at [www.gmod.org](http://www.gmod.org).

We plan to release a new version of bioperl-run in the coming week.
bioperl-run is a package of perl module wrappers around many
applications common to bioinformatics analyses. Shawn Hoon is responsible for
overseeing this release. Previous and future releases are available at
http://bioperl.org/DIST/ and in CPAN and as always from our CVS
repository [http://cvs.open-bio.org](http://cvs.open-bio.org).

A brand new package bioperl-microarray will be released this week as
well, version 0.1. This is a project headed by Allen Day and he will be
announcing a code release shortly. The code will be available from
CPAN, http://bioperl.org/DIST, and http://cvs.open-bio.org/.

Another recent project which has not been released yet, but should be
out this fall is bioperl-pedigree. This will include codes for parsing and
representing pedigree data and will interface with genotype parsing and
representations already part of the Bioperl Core. This package is
overseen by Jason Stajich. Code is available from our CVS repository
and will be available at http://bioperl.org/DIST.

Contributors
\-\-\----------

The hard work of many people has gone into this release, please see
[AUTHORS](http://bioperl.org/Core/Latest/AUTHORS.html) file included in the release for a complete list of individuals who have contributed to
the project.

We would especially like to thank those who have provided bug reports
and feedback about the modules to help us improve them. We would like to
welcome several new developers who have joined us recently to provide
code improvements and implementations of new areas for Bioperl.

Future plans
\-\-\----------
We intend to focus our energy on the next set of developer's releases in
the Fall of 2003 which will be numbered 1.3.x and will lead to the next
stable release 1.4 in 2004.

We encourage new and old developers to be part of the development cycle
as well as users to provide feedback and bug reports.

Bugs
\-\-\--
Bugs should be reported at our bug tracking site. Information about bugs in the Changes are also available from this site.
[http://bugzilla.bioperl.org](http://bugzilla.bioperl.org/)

A synopsis of changes from the Changes file

* * *

## 1.2.3 Stable release update

- Bug #1475 - Fix and add speedup to spliced\_seq for remote location
  handling.

- Bug #1477 - Sel --> Sec abbreviation fixed

- Fix bug #1487 where paring in-between locations when
  end < start caused the FTLocationFactory logic to fail.

- Fix bug #1489 which was not dealing with keywords as an
  arrayref properly (this is fixed on the main trunk because
  keywords returns a string and the array is accessible via
  get\_keywords).

- Bio::Tree::Tree memory leak (bug #1480) fixed
  Added a new initialization option -nodelete which
  won't try and cleanup the containing nodes if this
  is true.

- Bug with parsing labeled nodes with Bio::TreeIO::newick fixed
  this was only present on the branch for the 1.2.1 and 1.2.2
  series
  - Also merged main trunk changes to the branch which make
    newick -> nhx round tripping more effective (storing branch
    length and bootstrap values in same locate for NodeNHX and Node
    implementations.) Fixes to TreeIO parsing for labeled internal
    also required small changes to TreeIO::nhx. Improved
    tests for this module as well.
- Bio::SearchIO
  - Fixed bugs in BLAST parsing which couldn't parse NCBI
    gapped blast properly (was losing hit significance values due to
    the extra unexpeted column).

  - Parsing of blastcl3 (netblast from NCBI) now can handle case of
    integer overflow (# of letters in nt seq dbs is > MAX\_INT)
    although doesn't try to correct it - will get the negative
    number for you. Added a test for this as well.

  - Fixed HMMER parsing bug which prevented parsing when a hmmpfam
    report has no top-level family classification scores but does
    have
    scores and alignments for individual domains.

  - Parsing FASTA reports where ungapped percent ID is < 10 and the
    regular expression to match the line was missing the
    possibility of
    an extra space. This is rare, which is why we probably did not
    catch it before.

  - BLAST parsing picks up more of the statistics/parameter fields
    at the bottom of reports. Still not fully complete.

  - SearchIO::Writer::HTMLResultWriter and TextResultWriter
    were fixed to include many improvements and added flexiblity
    in outputting the files. Bug #1495 was also fixed in the
    process.
- Bio::DB::GFF
  - Update for GFF3 compatibility.

  - Added scripts for importing from UCSC and GenBank.

  - Added a 1.2003 version number.
- Bio::Graphics
  - Updated tutorial.

  - Added a 1.2003 version number.
- SeqIO::swiss Bug #1504 fixed with swiss writing which was not
  properly writing keywords out.

- Bio::SeqIO::genbank
  - Fixed bug/enhancement #1513 where dates of
    the form D-MMM-YYYY were not parsed. Even though this is
    invalid format we can handle it - and also cleanup the date
    string so it is properly formatted.

  - Bug/enhancement #1517 fixed so that SEGMENT line can be parsed
    and written with Genbank format. Similarly bug #1515 is fixed
    to
    parse in the ORIGIN text.
- Bio::SeqIO::fasta, a new method called preferred\_id\_type allows
  you to specify the ID type, one of (accession accession.version
  display primary). See Bio::SeqIO::preferred\_id\_type method
  documentation for more information.

- Unigene parsing updated to handle file format changes by NCBI

Jason Stajich on behalf of the Bioperl developers.
--
Jason Stajich
Duke University
jason at cgt.mc.duke.edu
