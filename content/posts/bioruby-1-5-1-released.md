---
author: NaohisaGoto
category:
  - bioruby
  - code
  - development
  - obf
  - obf-projects
date: "2016-09-07T15:04:32+00:00"
guid: https://news.open-bio.org/?p=1547
summary: |-
  We are pleased to announce the release of BioRuby 1.5.1.

  In this new release, NCBI Entrez web client classes, Bio::NCBI::REST and Bio::PubMed, are changed to use HTTPS instead of HTTP, to prepare [NCBI website transitioning to HTTPS](https://www.ncbi.nlm.nih.gov/news/06-10-2016-ncbi-https/).
tag:
  - bioruby
title: BioRuby 1.5.1 released
url: /2016/09/07/bioruby-1-5-1-released/

---
We are pleased to announce the release of BioRuby 1.5.1.

In this new release, NCBI Entrez web client classes, Bio::NCBI::REST and Bio::PubMed, are changed to use HTTPS instead of HTTP, to prepare [NCBI website transitioning to HTTPS](https://www.ncbi.nlm.nih.gov/news/06-10-2016-ncbi-https/).

For more information, see [RELEASE\_NOTES.rdoc](https://github.com/bioruby/bioruby/blob/1.5.1/RELEASE_NOTES.rdoc "RELEASE_NOTES.rdoc") and [ChangeLog](https://github.com/bioruby/bioruby/blob/1.5.1/ChangeLog "ChangeLog").

The archive is available for download from the following links.

- Tar.gz file: [http://bioruby.org/archive/bioruby-1.5.1.tar.gz](http://bioruby.org/archive/bioruby-1.5.1.tar.gz)
- Gem file: [https://rubygems.org/gems/bio](https://rubygems.org/gems/bio "https://rubygems.org/gems/bio") or [http://bioruby.org/archive/gems/bio-1.5.1.gem](http://bioruby.org/archive/gems/bio-1.5.1.gem)

You can easily install by using RubyGems. First, check the
version number by using search command:

`% gem search --remote bio`

and find “bio (1.5.1)” in the list. Then,

`% sudo gem install bio`

Note that BioRuby 1.5.X will be the final release version that supports Ruby 1.8.

Because this release is a minor version up, only few changes picked from the [git head](https://github.com/bioruby/bioruby) are included.

Acknowledgments: Thanks to Dr. Mark Johnson about information of the NCBI website change.
