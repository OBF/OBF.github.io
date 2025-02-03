---
author: NaohisaGoto
category:
  - bioruby
  - code
  - development
  - obf
  - obf-projects
date: "2010-10-22T06:36:50+00:00"
guid: http://news.open-bio.org/news/?p=746
summary: |-
  We are pleased to announce the release of [BioRuby](http://bioruby.org/ "BioRuby") 1.4.1. This new release fixes bugs existed in 1.4.0 and new features are added.

  Here is a brief summary of changes.

  **
title: BioRuby 1.4.1 released
url: /2010/10/22/bioruby-1-4-1-released/

---
We are pleased to announce the release of [BioRuby](http://bioruby.org/ "BioRuby") 1.4.1. This new release fixes bugs existed in 1.4.0 and new features are added.

Here is a brief summary of changes.

**PAML Codeml support is significantly improved:** PAML Codeml result parser is completely rewritten and is significantly improved. The code is developed by Pjotr Prins.

**KEGG PATHWAY and KEGG MODULE parsers are added:** The code is developed by Kozo Nishida and Toshiaki Katayama.

**Bio::KEGG::GENES and Bio::KEGG::GENOME and bug fixes and new methods:** Some of them are due to the file format changes.

**Test codes are added and improved:** Test codes are added and improved. Tney are developed by Kazuhiro Hayashi, Kozo Nishida, John Prince, and Naohisa Goto.

**Bug fixes in Bio::Tree:** somemethods did not work correctly.

**Platform-dependent bug when calling external programs:** Detection of platform is improved not to call fork(2) on platforms that do not support it (e.g. JRuby).

In addition, many changes have been made, including incompatible changes. For more information, see [RELEASE\_NOTES.rdoc](http://github.com/bioruby/bioruby/blob/1.4.1/RELEASE_NOTES.rdoc) and [ChangeLog](http://github.com/bioruby/bioruby/blob/1.4.1/ChangeLog).

The archive is available at: [http://bioruby.org/archive/bioruby-1.4.1.tar.gz](http://bioruby.org/archive/bioruby-1.4.1.tar.gz)

Gem file is also available at:  [http://bioruby.org/archive/gems/bio-1.4.1.gem](http://bioruby.org/archive/gems/bio-1.4.1.gem)

We also put RubyGems pacakge at RubyForge and Gemcutter. You can easily install by using RubyGems. First, check the version number by using search command:
% gem search –remote bio
and find “bio (1.4.1)” in the list. Then,
% sudo gem install bio

Finally, we are sorry that many new features are waiting to be merged to BioRuby, including  HMMER3 support. These will be included in the next major release version.

Hope you enjoy.
