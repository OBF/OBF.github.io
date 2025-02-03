---
author: NaohisaGoto
category:
  - bioruby
  - code
  - development
  - obf
  - obf-projects
date: "2012-08-21T16:47:56+00:00"
guid: http://news.open-bio.org/news/?p=971
tag:
  - bioruby
title: BioRuby 1.4.3 released
url: /2012/08/21/bioruby-1-4-3-released/

---
We are pleased to announce the release of [BioRuby](http://bioruby.org/) 1.4.3. This new release fixes bugs existed in 1.4.2 and improves portability on JRuby and Rubinius.

Here is a brief summary of changes.

- Bio::KEGG::KGML bug fixes and new class Bio::KEGG::KGML::Graphics for storing a graphics element.
- Many failures and errors running on JRuby and Rubinius are resolved.
- Strange behavior related with “circular require” is fixed.
- Fixed: Genomenet remote BLAST does not work.
- Fixed: Bio::NucleicAcid.to\_re(“s”) typo.
- Fixed: Bio::EMBL#os raises RuntimeError.
- Fixed: bin/bioruby: Failed to save object with error message "can’t convert Symbol into String" on Ruby 1.9.

In addition, many changes have been made, including incompatible changes. For more information, see [RELEASE\_NOTES.rdoc](https://github.com/bioruby/bioruby/blob/1.4.3/RELEASE_NOTES.rdoc) and [ChangeLog](https://github.com/bioruby/bioruby/blob/1.4.3/ChangeLog).

The archive is available at: [http://bioruby.org/archive/bioruby-1.4.3.tar.gz](http://bioruby.org/archive/bioruby-1.4.3.tar.gz)  

Gem file is also available at: [http://bioruby.org/archive/gems/bio-1.4.3.gem](http://bioruby.org/archive/gems/bio-1.4.3.gem)

We also put RubyGems pacakge at RubyGems.org and RubyForge. You can easily install by using RubyGems. First, check the version number by using search command:  

% gem search --remote bio  

and find “bio (1.4.3)” in the list. Then,  

% sudo gem install bio

Acknowledgments: Thanks to all persons reporting issues and/or submitting patches.

Hope you enjoy.
