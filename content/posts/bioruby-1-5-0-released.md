---
author: NaohisaGoto
category:
  - bioruby
  - code
  - development
  - obf
  - obf-projects
date: "2015-07-02T14:03:08+00:00"
guid: http://news.open-bio.org/news/?p=1328
tag:
  - bioruby
title: BioRuby 1.5.0 released
url: /2015/07/02/bioruby-1-5-0-released/

---
We are pleased to announce the release of BioRuby 1.5.0. This new release includes support of recent Ruby versions (Ruby 2.0.0, 2.1 and 2.2),  improvement of codes, and bug fixes.

Here is a brief summary of changes.

- Ruby 2.0.0, 2.1, 2.2 support.
- Some features are removed because of remote service discontinuance or difficulty of code maintenance.
- Refactoring of code.
- Bio::SPTR is renamed as Bio::UniProtKB.
- Bug fixes.

In addition, many changes have been made, including incompatible changes. For more information, see [RELEASE\_NOTES.rdoc](https://github.com/bioruby/bioruby/blob/1.5.0/RELEASE_NOTES.rdoc "RELEASE_NOTES.rdoc") and [ChangeLog](https://github.com/bioruby/bioruby/blob/1.5.0/ChangeLog "ChangeLog").

The archive is available for download from the following links.

- Tar.gz file: [http://bioruby.org/archive/bioruby-1.5.0.tar.gz](http://bioruby.org/archive/bioruby-1.5.0.tar.gz "http://bioruby.org/archive/bioruby-1.5.0.tar.gz")
- Gem file: [https://rubygems.org/gems/bio](https://rubygems.org/gems/bio "https://rubygems.org/gems/bio") or [http://bioruby.org/archive/gems/bio-1.5.0.gem](http://bioruby.org/archive/gems/bio-1.5.0.gem "http://bioruby.org/archive/gems/bio-1.5.0.gem")

You can easily install by using RubyGems. First, check the
version number by using search command:

`% gem search --remote bio`

and find “bio (1.5.0)” in the list. Then,

`% sudo gem install bio`

Note that BioRuby 1.5.X will be the final release version that supports Ruby 1.8.

Acknowledgments: Thanks to all persons reporting issues and/or
submitting patches.

Hope you enjoy.
