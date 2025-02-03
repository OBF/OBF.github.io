---
author: heikki
category:
  - bioperl
date: "2003-07-08T20:27:41+00:00"
guid: http://news.open-bio.org/news/?p=106
summary: |-
  This is a bug fix release from the stable branch.

  The Bioperl release 1.2.2 is available at [http://www.bioperl.org/DIST/bioperl-1.2.2.tar.gz](http://www.bioperl.org/DIST/bioperl-1.2.2.tar.gz)
  and is propagating around CPAN now.

  Bioperl-run is a collection of modules that wrap bioinformatics
  applications to allow running them from bioperl. The release cycle of
  bioperl-run follows the core. The latest bioperl-run release is
  therefore at: [http://www.bioperl.org/DIST/bioperl-run-1.2.2.tar.gz](http://www.bioperl.org/DIST/bioperl-run-1.2.2.tar.gz)
title: Bioperl 1.2.2 released
url: /2003/07/08/bioperl-122-released/

---
This is a bug fix release from the stable branch.

The Bioperl release 1.2.2 is available at [http://www.bioperl.org/DIST/bioperl-1.2.2.tar.gz](http://www.bioperl.org/DIST/bioperl-1.2.2.tar.gz)
and is propagating around CPAN now.

Bioperl-run is a collection of modules that wrap bioinformatics
applications to allow running them from bioperl. The release cycle of
bioperl-run follows the core. The latest bioperl-run release is
therefore at: [http://www.bioperl.org/DIST/bioperl-run-1.2.2.tar.gz](http://www.bioperl.org/DIST/bioperl-run-1.2.2.tar.gz)

The main bug fixes in this release are:

bioperl

- OBDA Registry code is up to latest specs and fuly functional

- Sequence retrieval from NCBI works again after URL change
  (Bio::DB::GenBank)

- The BLAST output parsed now works on megablast and parses
  even the last hit

- Result writers now correctly report alignment start/end info
  for translated BLAST/FASTA searches
  (Bio::SearchIO::Writer::(HTML\|Text)ResultWriter)

- Improvements in closing and keeping open file handles

- Robustness of Bio::Graphics modules have been improved

- Other improved modules:
  - Bio::OntologyIO::dagflat

  - Bio::Annotation::OntologyTerm

  - Bio::TreeIO::newick

  - Bio::Tools::BPbl2seq

  - Bio::Tools::Genemark

  - Bio::SeqIO::genbank

bioperl-run

- SoapLab and PISE improvements

- New wrapper for Vista: [http://www-gsd.lbl.gov/vista/](http://www-gsd.lbl.gov/vista/)
  (Bio::Tools::Run::Vista)

- Other improved modules:
  - Bio::Tools::Run::Eponine

  - Bio::Tools::Run::FootPrinter

  - Bio::Tools::Run::Genewise

  - Bio::Tools::Run::Genscan

  - Bio::Tools::Run::Hmmpfam

  - Bio::Tools::Run::Mdust

  - Bio::Tools::Run::Signalp

  - Bio::Tools::Run::Phylo::Phylip::SeqBoot

  - Bio::Tools::Run::Phylo::Phylip::Neighbor

  - Bio::Tools::Run::Alignment::Blat

  - Bio::Tools::Run::Alignment::Lagan

More details are in distribution file 'Changes'.

Thank you for all who reported bugs and made this release possible.
