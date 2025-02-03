---
author: heikki
category:
  - bioperl
date: "2003-12-23T13:36:11+00:00"
guid: http://news.open-bio.org/news/?p=118
summary: |-
  The stable Bioperl release 1.4 is available for immediate use at:
  [http://bioperl.org/DIST](http://bioperl.org/DIST).

  We are releasing simultaneously three modules:

  - bioperl-core - core bioperl modules (
    [gz](http://bioperl.org/DIST/current_core_stable.tar.gz) [b2z](http://bioperl.org/DIST/current_core_stable.tar.bz2))

  - bioperl-ext - C compiled extensions (
    [gz](http://bioperl.org/DIST/current_ext_stable.tar.gz) [b2z](http://bioperl.org/DIST/current_ext_stable.tar.bz2))

  - bioperl-run - wrappers for external programs (
    [gz](http://bioperl.org/DIST/current_run_stable.tar.gz) [b2z](http://bioperl.org/DIST/current_run_stable.tar.bz2))


  They will also appear shortly at
  [the IUBIO mirror](http://iubio.bio.indiana.edu/soft/molbio/perl/bioperl/) (later today)
  and in
  [CPAN](http://search.cpan.org/dist/bioperl/).

  Remember, all the external modules needed by bioperl-core can be
  installed from CPAN under name
  [Bundle-BioPerl](http://search.cpan.org/dist/Bundle-BioPerl/).
title: Bioperl Release  1.4
url: /2003/12/23/bioperl-release-14/

---
The stable Bioperl release 1.4 is available for immediate use at:
[http://bioperl.org/DIST](http://bioperl.org/DIST).

We are releasing simultaneously three modules:

- bioperl-core - core bioperl modules (
  [gz](http://bioperl.org/DIST/current_core_stable.tar.gz) [b2z](http://bioperl.org/DIST/current_core_stable.tar.bz2))

- bioperl-ext - C compiled extensions (
  [gz](http://bioperl.org/DIST/current_ext_stable.tar.gz) [b2z](http://bioperl.org/DIST/current_ext_stable.tar.bz2))

- bioperl-run - wrappers for external programs (
  [gz](http://bioperl.org/DIST/current_run_stable.tar.gz) [b2z](http://bioperl.org/DIST/current_run_stable.tar.bz2))

They will also appear shortly at
[the IUBIO mirror](http://iubio.bio.indiana.edu/soft/molbio/perl/bioperl/) (later today)
and in
[CPAN](http://search.cpan.org/dist/bioperl/).

Remember, all the external modules needed by bioperl-core can be
installed from CPAN under name
[Bundle-BioPerl](http://search.cpan.org/dist/Bundle-BioPerl/).

### Changes

Over 3000 file changes have gone into this release since the 1.2
development tree was branched off from the main. These are the main feature enhancements:

- installable scripts

- global module version from Bio::Root:Version

- Bio::Graphics - major improvements; added SVG support

- Bio::Popgen - population genetics

- Bio::Restriction - new restrion analysis modulues

- Bio::Tools::Analysis - web based DNA and Protein analysis
  framework and several implementaions

- Bio::Seq::Meta - per residue annotable sequences

- Bio::Matrix- including Bio::Matrix::PSM - Position Scoring Matrix

- Bio::Ontology - major contributions

- Bio:Tree

- Bio::Tools::SiRNA, Bio::SeqFeature::SiRNA - small inhibitory RNA

- Bio::SeqFeature::Tools - seqFeature mapping tools,
  e.g. Bio::SeqFeature::Tools::Unflattener.pm

- Bio::Tools::dpAlign - pure perl dynamic programming sequence alignment (needs Bioperl-ext)

- new Bio::SearchIO formats

- new Bio::SeqIO formats: tab, kegg, tigr, game; important fixes for
  old modulues

- Bio::AlignIO: maf

- improved Bio::Tools::Genewise

- Bio::SeqIO now can recognize sequence formats automatically from stream

- new parsers in Bio::Tools:
  Blat, Geneid, Lagan, Mdust, Promoterwise, PrositeScan,

- several new HOWTOs: SimpleWebAnalysis, Trees, Feature Annotation,
  OBDA Access, Flat Databases

- hundreds of new and improved files

For detailed documentation, see individual module documentation in the
distribution or in [http://doc.bioperl.org/](http://doc.bioperl.org/). The tutorials are
available at [http://bioperl.org/HOWTOs/](http://bioperl.org/HOWTOs/).

This release is a result of hard work by the bioperl core team, nearly
hundred developers and countless suggestions and bug reports at the
bioperl mailing list (bioperl-l@bioperl.org) or the the bioperl bug
tracking system ( [http://bugzilla.bioperl.org/](http://bugzilla.bioperl.org/)).

Wishing you all Peaceful Christmas,

-Heikki and the bioperl core developers
