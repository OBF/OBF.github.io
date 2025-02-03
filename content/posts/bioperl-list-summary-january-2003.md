---
author: aaron
category:
  - bioperl
date: "2003-03-04T19:51:52+00:00"
guid: http://news.open-bio.org/news/?p=74
summary: |-
  As I seem to be volunteering for more and more BioPerl documentation
  jobs recently, I thought I'd pool my resources and recycle some of my
  tuits to write a list summary. Expect these to be sporadic and
  incomplete; my goal is to highlight important questions, changes,
  fixes, and proposals, not recapitulate all list traffic.
title: BioPerl List Summary - January 2003
url: /2003/03/04/bioperl-list-summary-january-2003/

---
As I seem to be volunteering for more and more BioPerl documentation
jobs recently, I thought I'd pool my resources and recycle some of my
tuits to write a list summary. Expect these to be sporadic and
incomplete; my goal is to highlight important questions, changes,
fixes, and proposals, not recapitulate all list traffic.

- [Introduction](#introduction)
- [Questions](#questions)
- [Changes/Additions](#changes/additions)
- [Fixes](#fixes)
- [Proposals](#proposals)
- [Conclusion](#conclusion)

* * *

# Introduction

As I seem to be volunteering for more and more BioPerl documentation
jobs recently, I thought I'd pool my resources and recycle some of my
tuits to write a list summary. Expect these to be sporadic and
incomplete; my goal is to highlight important questions, changes,
fixes, and proposals, not recapitulate all list traffic. I'll try to
include appropriate links to specific messages, or at least to the
parent message. It'll probably take me awhile to get good at this, so
please bear with me (and do send any suggestions).

To play a bit of catch up, I'm now going to loosely summarize the
entire month of January (leaving a few topics untouched that are
better addressed in February). February's summary will be ready soon,
after which you'll see more easily digestable weekly (or perhaps
bi-weekly) summaries. I'll also be posting the HTML-ized summaries on
my O'Reilly weblog with active hyperlinks.

One item from December 31 of 2002 bears mentioning: Ewan Birney
released stable version 1.2, with significant new functionality, and
important updates to code that makes use of NCBI web services;
upgrading is highly recommended, although some of the January list
activity reflects small trials and tribulations with this release.

```
http://makeashorterlink.com/?S17521DA3
```

* * *

# Questions

- **Searching the mailing list archives**  

  This seemed like an appropriate topic to put at the top of my list.
  The Bioperl-l mailing list isn't exactly as high-traffic as
  perl5-porters or the linux kernel mailing list, but it is a mixture
  of both deeply technical development issues and novice user
  questions. While the BioPerl tutorial and documentation are the
  first places one should look for answers, the second place must be
  the archives of the mailing list. Brain Osborne pointed out that
  "the Search box is hidden below the Thanks link at www.bioperl.org".

  It wasn't mentioned, but the "htdig" link Hilmar Lapp pointed out
  (which is also below the search box) does not actually index the
  bioperl mailing list, but seems to search all other OBF-affiliated
  lists (biojava, biopython, etc) ...

  ```
  http://users.bioperl.org/htdig/
  ```

  Michal Kurowski pointed out that "the quickest way of accessing old
  postings seems to be a group archive from the mailman pages" and that
  "you can even download the whole thing and use it as a local mailbox",
  which happens to be very useful if you want to write list summaries.
  Mailman archives are at:

  ```
  http://bioperl.org/pipermail/bioperl-l/
  ```

- **Bioperl 1.2 builds under cygwin**  

  John Nash reports that he was able to build the 1.2 distribution
  under cygwin once MakeMaker issues were overcome (in his case by
  upgrading to perl 5.8.0). Other tips are provided:

  ```
  http://makeashorterlink.com/?S23631DA3
  http://makeashorterlink.com/?M27643DA3
  ```

- **Getting/untarring the 1.2 distribution**  

  Some people had trouble either FTPing the 1.2 distribution, or with
  successfully untarring the tarball. These problems seemed to have
  resolved by themselves, and may have been related to router issues at
  the server. For the record, bioperl-1.2 can be found at:

  ```
  http://www.bioperl.org/ftp/DIST/bioperl-1.2.tar.gz
  ```

- **man pages with bioperl-1.2**  

  People may have noticed that the "make" process for bioperl-1.2 does
  not generate nor install man pages. Ewan Birney explains, "In 1.2 we
  had to drop the manifyfication stage of the makefile because it was
  triggering a line-too-long error on some OSs due to shell
  constraints". If you wish to get them back, comment (or delete) out
  the MY::manifypods sub in Makefile.PL

  ```
  http://makeashorterlink.com/?F10761DA3
  ```

- **Converting ABI trace to Phred format**  

  When asked why an ABI trace file read via SeqIO::abi didn't generate a
  Bio::Seq::SeqWithQuality (a sequence with associated quality values),
  Aaron Mackey replied, "I'm not sure why abi.pm in the bioperl
  distribution doesn't set it's sequence factory to SeqWithQuality"; I'm
  still not sure why. See the fix at:

  ```
  http://makeashorterlink.com/?H2C954DA3
  ```

- **biocorba status**  

  When asked about the status of the biocorba project, Jason Stajich
  replied, "We have working bindings in java,perl,python and bridges to
  the respective Bio\* toolkits from these bindings for servers and
  clients based on a slightly modified BSANE IDL spec from OMG". He
  qualified that statement with "none of the original developers are
  using it in any of their work so development and final rounds of
  testing have not really happened"

  ```
  http://makeashorterlink.com/?G57A42DA3
  ```

- **DNA Smith-Waterman**  

  Yee Man has reimplemented the classic Smith-Waterman algorithm, with
  algorithmic improvements as suggested by Gotoh (affine gaps) and Myers
  & Miller (linear space), and wondered whether it would be a good
  addition to the BioPerl C-coded extension library (which currently
  contains a protein-only Smith-Waterman implementation by Ewan Birney,
  pSW.pm). Some discussion about classic (and novel) dynamic
  programming algorithms ensued, which eventually boiled down to a
  desire to have the generic (but extremely fast) Smith-Waterman code
  (written by Webb Miller) used by Bill Pearson's SSEARCH implementation
  made more widely available as a linkable C library (which BioPerl
  could then subsume). Interested parties should contact me.
  Relatedly, to answer one of our FAQ's yet again, if you currently want
  to do Smith-Waterman on DNA sequences, you should use BioPerl's
  bindings to the EMBOSS suite of sequence utilities.

  ```
  http://makeashorterlink.com/?Y20B21DA3
  http://makeashorterlink.com/?M12B23DA3
  ```

- **using AUTOLOAD for get/set accessors**  

  The BioPerl code is full of explicitly coded accessor methods; often
  we are asked why we don't use more code-efficient methods of
  autogenerating these identical functions (via AUTOLOAD or
  Class::MakeMethod). The discussion is long-ranging, but it boils down
  to wanting every accessor to have the same functionality with respect
  to undef values and return value behavior, as dictated by our accessor
  "boilerplate" (which we kindly ask everyone to use). Yes, we know we
  can achieve that via sophisticated Class::MakeMethod usage, but we
  have bigger fish to fry at the moment. There's another, subtler
  issue about interfaces and implementation method introspection, but
  I'll leave that to a later discussion.

  ```
  http://makeashorterlink.com/?Z22C32DA3
  ```

- **Bio:Seq no longer a RangeI (bug in Bio::Graphics::Panel)**  

  Much to the consternation of Lincoln Stein (and his legions of
  Bio::Graphics users), BioPerl 1.2 introduced a change to Bio::Seq in
  that it no longer complies with the Bio::RangeI interface; see Heikki
  Lehvaslaiho's "This has to be cruft!" message from November:

  ```
  http://makeashorterlink.com/?Q53C41DA3
  ```

  Unfortunately, Bio::Graphics::Panel relied on Bio::Seq having a
  "start" method, so lots of existing code broke. A number of fixes
  were recommended, including a) using a Bio::Seq::SeqFactory to
  generate Bio::LocatableSeq's (which do implement RangeI methods), b)
  patching your Bio::Graphics::Panel and c) upgrading BioPerl 1.2 to
  the live CVS development version. A BioPerl 1.2.1 is forthcoming for
  this, and other reasons.

  ```
  http://makeashorterlink.com/?R17C61DA3
  http://makeashorterlink.com/?S3AC21DA3
  ```

- **complement(join(e1, e2)) vs. join(complement(e1), `complement(e2))`**  

  Periodically, people ask "Is it possible to have bioperl output
  features in Genbank format of the form
  "complement(join(1..50,60..100))" rather than
  "join(complement(1..50),complement(60..100))?" This time it
  degenerated a little into a discussion about whether these two
  representations were semantically equivalent (short answer: yes). The
  answer to the original question is that BioPerl parses either
  representation into the same structure, which can only be "dumped" in
  one representation (presently, the latter).

  ```
  http://makeashorterlink.com/?H2CC16DA3
  ```

- **GenBank `bond()` FT operator**  

  Recent GenBank files have begun to exhibit a new feature location
  operator, "bond", to identify dicysteine bonds in proteins and mRNA
  splice sites in RefSeq sequences. BioPerl has no concept of this
  location operator (which is really more of a feature, and would
  be better represented as a /bond feature table entry), and so
  currently dies when parsing a record containing it. A brute force
  fix is provided, but a better answer is yet to appear:

  ```
  http://makeashorterlink.com/?L24D12DA3
  ```

* * *

# Changes/Additions

- **SearchIO now has megablast parser**  

  Jason Stajich writes, "The oft requested megablast parser has now been
  implemented in SearchIO". This should be available in the upcoming
  bioperl 1.2.1 bug-fix release, as well as CVS.

  ```
  http://makeashorterlink.com/?O29D62DA3
  ```

- **bl2seq parser needs to know report type to get strand right**  

  No matter how hard he tried, Dave Arenillas couldn't retrieve HSP
  strand information from a bl2seq (BLAST two sequences against each
  other) report. After "a little bit of detective work", Jason Stajich
  found that the Bio::Tools::BPbl2seq report object needs to be told
  the program type (e.g. "blastn") since it's not smart enough to guess
  it by context alone. The patch to BPbl2seq.pm is available via CVS.

  ```
  http://makeashorterlink.com/?M2ED52DA3
  ```

- **bioperl.rpm in biolinux.org distribution**  

  Marc Logghe reports that "A couple of friends of mine have started up
  www.biolinux.org \[ ... and\] are offering a number of rpm packages for
  free download like e.g. emboss, sim4, phylip, ncbiblast, ...". After
  some discussion about what a bugbear packaging BioPerl can be (most
  dependencies are not critical for the entire package, only certain
  subparts that may or may not be useful for a given person), Hunter
  Matthews chimed in that he'd likely be able to make a bioperl 1.2 rpm
  (he had previously made a 1.0 rpm); Hunter adds "7.3 would be the most
  likely target platform". Marc Logghe later reported that "the bioperl
  rpm's for RedHat and Suse are on line at [http://biolinux.org/bioperl.html"](http://biolinux.org/bioperl.html)

  ```
  http://makeashorterlink.com/?S16E22DA3
  ```

- **example scripts reorganization for installation as "production" code**  

  Spurred on by an earlier conversation regarding the perl scripts
  scattered between examples/ and scripts/, Brian Osborne has taken up
  the challenge to reorganize and reshape these so that those functional
  scripts with adequate POD and a .PLS suffix all live in scripts/ and
  get installed for "production" use. Scripts should remain in
  examples/ if they are simply "proof-of-concept" code, or just poorly
  documented. Everyone liked this, and from the CVS activity, it looks
  like the work is progressing.

  ```
  http://makeashorterlink.com/?R29E32DA3
  ```

- **Bio::Seq::SequenceTrace**  

  Chad Matsalla has added a Bio::Seq::SequenceTrace object, to "mimic
  the information available in a scf 'Sequence Chromatogram File"'. It
  slices and dices. In the process, Chad ended up rewriting his
  Bio::SeqIO::scf code, "because the old module was somewhat ...
  clunky".

  ```
  http://makeashorterlink.com/?R3AE25DA3
  ```

- **MLAGAN/LAGAN support**  

  Stephen Montgomery has supplied both MLAGAN and LAGAN wrappers and
  parsers (the Lagan Tookit is a set of alignment programs for
  comparative genomics).

  ```
  http://makeashorterlink.com/?N11F24DA3
  ```

* * *

# Fixes

- **SeqIO/scf.pm bug**  

  Tony Cox "finally got around to checking in a fix for the SeqIO/scf
  module when it has to deal with 8-bit encoded trace data". It's not
  yet clear where this fix stands with Chad Matsalla's rewrite of
  Bio/SeqIO/scf.pm

- **Bio::Tools::Run::WrapperBase.pm missing from 1.2**  

  Because of some code migration between bioperl subprojects,
  Bio/Tools/Run/WrapperBase.pm went missing in the 1.2 release, causing
  a wide variety of failures. The 1.2.1 release will address this, or
  you can retrieve the missing file and install it manually from here:

  ```
  http://makeashorterlink.com/?B20015EA3
  ```

- **bug fixes in Blast HSP tiling code**  

  After finding that for certain BLAST reports the "blast" and
  "psiblast" SearchIO parsers gave mildly differing values for
  "frac\_identical" and "frac\_conserved", Jason Stajich did some
  auditing of the HSP tiling code and found a few inconsistencies which
  have since been fixed. End result: frac\_identical and frac\_conserved
  should be better behaved and actually correct.

  ```
  http://makeashorterlink.com/?V26053EA3
  ```

* * *

# Proposals

- **Project ideas for the aspiring biohacker**  

  Periodically, we're asked "I'd like to get involved, do you have any
  project ideas a newbie could work on?". Jason Stajich shot out a few
  choice ideas including "blastz" SearchIO parsing, which was briefly
  discussed. Get involved!

  ```
  http://makeashorterlink.com/?D28022EA3
  ```

- **Bio::Perl namespace export groups**  

  The Bio::Perl module is a top-level, "novice" interface to a few small
  tidbits of BioPerl functionality. Many first-time users appreciate
  the simplicity of the Bio::Perl interface, and so we'd like to extend
  it's reach into other "meaty" areas of BioPerl functionality. Here we
  talk about how we might achieve this using custom export tags (a la
  CGI.pm and others). Another area where someone could make a dramatic
  impact without writing any new modules!

  ```
  http://makeashorterlink.com/?D4A025EA3
  ```

* * *

# Conclusion

Well, that's it for this installment. Stay tuned for February (a
much busier month!).
