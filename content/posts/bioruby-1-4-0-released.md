---
author: NaohisaGoto
category:
  - bioruby
  - code
  - development
  - obf
  - obf-projects
date: "2009-12-29T10:22:25+00:00"
guid: http://news.open-bio.org/news/?p=588
tag:
  - bioruby
  - fastq
title: BioRuby 1.4.0 released
url: /2009/12/29/bioruby-1-4-0-released/

---
We are pleased to announce the release of BioRuby 1.4.0. This new release contains many new features, in addition to bug fixes and improvements.

**PhyloXML support:** Support for reading and writing PhyloXML file format is added, developed by Diana Jaunzeikare, mentored by Christian M Zmasek and co-mentors, supported by Google Summer of Code 2009 in
collaboration with the National Evolutionary Synthesis Center (NESCent).

**FASTQ file format support:** Support for reading and writing FASTQ file format is added. All of the three FASTQ format variants are supported. The code is written by Naohisa Goto, with the help of discussions in the
open-bio-l mailing list. The prototype of Bio::Fastq class was first developed during the BioHackathon 2009 held in Okinawa.

**DNA chromatogram support:** Support for reading DNA chromatogram files are added. SCF and ABIF file formats are supported. The code is developed by Anthony Underwood.

**MEME (motif-based sequence analysis tools) support:** Support for running MAST (Motif Alignment & Search Tool, part of the MEME Suite, motif-based sequence analysis tools) and parsing its results are added,  developed by Adam Kraut.

**Improvement of KEGG parser classes:** Some new methods are added to parse new fields added to some KEGG file formats. Unit tests for KEGG parsers are also added and improved. These are contributed by Kozo Nishida.

**Many sample scripts are added:** Many sample scripts showing demonstrations of usages of classes are added. They were originally primitive test codes written in the "if \_\_FILE\_\_ == $0" convention.

**Unit tests can test installed BioRuby:** Mechanism to load library and to find test data in the unit tests are changed, and target library path and test data path can be changed with environment variables.

**Incompatible change: Bio::NCBI::REST needs email address:** NCBI announced that all Entrez Utilities (E-utilities)  requests must contain email and tool parameters, and requests without them will return error after June 2010. In BioRuby, to set default email address and tool name, following methods are added.

- Bio::NCBI.default\_email=(email)
- Bio::NCBI.default\_tool=(tool\_name)

Note that no default email address is preset in BioRuby. Library users must set their own email address or implement to get user's email address in some way (from input form, configuration file, etc).

In addition, many changes have been made, including incompatible changes. For more information, see [RELEASE\_NOTES.rdoc](http://github.com/bioruby/bioruby/blob/1.4.0/RELEASE_NOTES.rdoc) and [ChangeLog](http://github.com/bioruby/bioruby/blob/1.4.0/ChangeLog).

The archive is available at: [http://bioruby.org/archive/bioruby-1.4.0.tar.gz](http://bioruby.org/archive/bioruby-1.4.0.tar.gz)

Gem file is also available at:  [http://bioruby.org/archive/gems/bio-1.4.0.gem](http://bioruby.org/archive/gems/bio-1.4.0.gem)

We also put RubyGems pacakge at RubyForge and Gemcutter. You can easily install by using RubyGems.
First, check the version number by using search command:
% gem search --remote bio
and find "bio (1.4.0)" in the list. Then,
% sudo gem install bio

Hope you enjoy.
