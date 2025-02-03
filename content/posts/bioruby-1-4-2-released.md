---
author: NaohisaGoto
category:
  - bioruby
  - code
  - development
  - obf
  - obf-projects
date: "2011-08-26T09:49:42+00:00"
guid: http://news.open-bio.org/news/?p=848
summary: |-
  We are pleased to announce the release of [BioRuby](http://bioruby.org/ "BioRuby") 1.4.2. This new release fixes bugs existed in 1.4.1 and adds new features and improvement of performance.

  Here is a brief summary of changes.
tag:
  - bioruby
  - development
  - news
  - open-source
  - release
  - releases
title: BioRuby 1.4.2 released
url: /2011/08/26/bioruby-1-4-2-released/

---
We are pleased to announce the release of [BioRuby](http://bioruby.org/ "BioRuby") 1.4.2. This new release fixes bugs existed in 1.4.1 and adds new features and improvement of performance.

Here is a brief summary of changes.

**Speed-up of Bio::RestrictionEnzyme::Analysis.cut:** The new code is 50 to 80 fold faster than the previous code when cutting 1Mbp sequence running on Ruby 1.9.2p180. The code is written by Tomoaki NISHIYAMA and Naohisa Goto.

**New classes Bio::DDBJ::REST, REST interface for DDBJ Web API for Biology (WABI) web service** in additon to SOAP. Currently, only selected APIs are implemented.

**Bio::Blast with remote DDBJ server uses REST instead of SOAP** because Soap4r (SOAP library for Ruby) does not work well with Ruby 1.9. We can now use remote DDBJ BLAST server with Ruby 1.9.

**The Tutorial.rd is updated** by Pjotr Prins and Michael O'Keefe.

**Many unit tests are added** for Bio::GenBank, Bio::GenPept, Bio::NBRF, Bio::PDB and so on. Most of them are developed by Kazuhiro Hayashi during the Google Summer of Code 2010.
**New methods:** Bio::Fastq#to\_s, Bio::NCBI::REST::EFetch.nucleotide, Bio::NCBI::REST::EFetch.protein.

**Bug fixes:**

- Bio::Blast: Failure of remote BLAST execution is fixed, due to the changes in GenomeNet and DDBJ.
- Bio::Blast: When executing remote BLAST with "genomenet" server, options "-b" and "-v" are now correctly used to limit the number of hits to be reported.
- Bio::SPTR (Bio::UniProt): Due to the UniProtKB format changes, ID, DE, and WEB RESOURCE of CC lines were not correctly parsed.
- Bio::Reference#pubmed\_url: Updated to follow recent NCBI changes.
- Bio::Newick#reparse failure.
- Bio::MEDLINE#reference: doi field should be filled.
- Bio::Reference#endnote fails when url is not set.
- Bio::FastaFormat#query passes nil to the given factory object.
- BioRuby Shell: efetch(), getent(), and demo() fail.

In addition, many changes have been made, including incompatible changes. For more information, see [RELEASE\_NOTES.rdoc](https://github.com/bioruby/bioruby/blob/1.4.2/RELEASE_NOTES.rdoc) and [ChangeLog](https://github.com/bioruby/bioruby/blob/1.4.2/ChangeLog).

The archive is available at: [http://bioruby.org/archive/bioruby-1.4.2.tar.gz](http://bioruby.org/archive/bioruby-1.4.2.tar.gz)

Gem file is also available at:  [http://bioruby.org/archive/gems/bio-1.4.2.gem](http://bioruby.org/archive/gems/bio-1.4.2.gem)

We also put RubyGems pacakge at RubyForge and RubyGems.org. You can easily install by using RubyGems. First, check the version number by using search command:
% gem search --remote bio
and find “bio (1.4.2)” in the list. Then,
% sudo gem install bio

Acknowledgments: Thanks to all persons reporting issues and/or submitting patches. In addition, thanks to [NDBC](http://biosciencedbc.jp/?lng=en) / [DBCLS](http://dbcls.rois.ac.jp/en/) [BioHackathon2011](http://2011.biohackathon.org/) participants and organizers who try BioRuby during the BioHackathon2011.

Hope you enjoy.
