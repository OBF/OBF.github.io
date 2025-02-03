---
author: NaohisaGoto
category:
  - bioruby
  - code
  - development
  - obf
  - obf-projects
date: "2013-05-27T12:44:57+00:00"
guid: http://news.open-bio.org/news/?p=1023
summary: |-
  We are pleased to announce the release of BioRuby 1.4.3.0001. This new release fixes the following bugs.

  - "gem install bio" failed with Ruby 2.0 or later versions.
  - lib/bio/db/gff.rb script encoding issue
  - Bio::Blast::Default::Report parse error when subject sequence contains spaces.

  For more information, see [RELEASE\_NOTES.rdoc](https://github.com/bioruby/bioruby/blob/1.4.3.0001/RELEASE_NOTES.rdoc) and [ChangeLog](https://github.com/bioruby/bioruby/blob/1.4.3.0001/ChangeLog).
tag:
  - bioruby
title: BioRuby 1.4.3.0001 Released
url: /2013/05/27/bioruby-1-4-3-0001-released/

---
We are pleased to announce the release of BioRuby 1.4.3.0001. This new release fixes the following bugs.

- "gem install bio" failed with Ruby 2.0 or later versions.
- lib/bio/db/gff.rb script encoding issue
- Bio::Blast::Default::Report parse error when subject sequence contains spaces.

For more information, see [RELEASE\_NOTES.rdoc](https://github.com/bioruby/bioruby/blob/1.4.3.0001/RELEASE_NOTES.rdoc) and [ChangeLog](https://github.com/bioruby/bioruby/blob/1.4.3.0001/ChangeLog).

The archive is available at: [http://bioruby.org/archive/bioruby-1.4.3.0001.tar.gz](http://bioruby.org/archive/bioruby-1.4.3.0001.tar.gz)
Gem file is also available at: [http://bioruby.org/archive/gems/bio-1.4.3.0001.gem](http://bioruby.org/archive/gems/bio-1.4.3.0001.gem)

We also put RubyGems pacakge at RubyGems.org and RubyForge.

You can easily install by using RubyGems. First, check the version number by using search command:
% gem search –remote bio
and find “bio (1.4.3.0001)” in the list. Then,
% sudo gem install bio

Acknowledgments: Thanks to all persons reporting issues and/or submitting patches.
