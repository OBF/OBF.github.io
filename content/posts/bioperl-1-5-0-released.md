---
author: stajich
category:
  - bioperl
date: "2005-01-29T16:33:38+00:00"
guid: http://news.open-bio.org/news/?p=127
summary: |-
  Bioperl 1.5.0 Developer's release is available for download.
  ===============================================

  - [http://bioperl.org/DIST/bioperl-1.5.0.tar.bz2](http://bioperl.org/DIST/bioperl-1.5.0.tar.bz2) 425ac55ecbb4339b7b532ba6d429bb40

  - [http://bioperl.org/DIST/bioperl-1.5.0.tar.gz](http://bioperl.org/DIST/bioperl-1.5.0.tar.gz) 172472f0675de9a583432e21c9b1b5fc

  - [http://bioperl.org/DIST/bioperl-1.5.0.zip](http://bioperl.org/DIST/bioperl-1.5.0.zip) 3febcd2445a7393c65981a6f9f13a9ed


  We'll update the website to reflect this new release.

  The odd-numbered releases are called developer releases and are not
  deposited on CPAN. Please note that the API in 1.5.0 may change before
  the 1.6.0 release. which will be consider a stable API. We may do
  another developer release before 1.6.0 goes out.

  Lots of people have contributed to this release, I apologize for not
  naming them all. I'll try to cover some: thanks to Aaron Mackey for
  getting this release started, Brian Osborne for extensive documentation
  improvements, Nathan Haigh for volunteering to make a PPM of the
  release and Barry Moore and Nathan answering many of the windows
  related questions, Allen Day & Scott Cain & Steffen Grossmann for the
  work on FeatureIO, GFF3, and SeqFeature::Annotated, Chris Mungall for
  the work with Unflattener to merge GenBank annotations into GFF3
  objects.

  Please see the AUTHORS file for a complete list of contributors.

  Jason Stajich on behalf of the Bioperl developers.

  [http://portal.open-bio.org/pipermail/bioperl-l/2005-January/018031.html](http://portal.open-bio.org/pipermail/bioperl-l/2005-January/018031.html)
title: Bioperl 1.5.0 released
url: /2005/01/29/bioperl-150-released/

---
Bioperl 1.5.0 Developer's release is available for download.
===============================================

- [http://bioperl.org/DIST/bioperl-1.5.0.tar.bz2](http://bioperl.org/DIST/bioperl-1.5.0.tar.bz2) 425ac55ecbb4339b7b532ba6d429bb40

- [http://bioperl.org/DIST/bioperl-1.5.0.tar.gz](http://bioperl.org/DIST/bioperl-1.5.0.tar.gz) 172472f0675de9a583432e21c9b1b5fc

- [http://bioperl.org/DIST/bioperl-1.5.0.zip](http://bioperl.org/DIST/bioperl-1.5.0.zip) 3febcd2445a7393c65981a6f9f13a9ed

We'll update the website to reflect this new release.

The odd-numbered releases are called developer releases and are not
deposited on CPAN. Please note that the API in 1.5.0 may change before
the 1.6.0 release. which will be consider a stable API. We may do
another developer release before 1.6.0 goes out.

Lots of people have contributed to this release, I apologize for not
naming them all. I'll try to cover some: thanks to Aaron Mackey for
getting this release started, Brian Osborne for extensive documentation
improvements, Nathan Haigh for volunteering to make a PPM of the
release and Barry Moore and Nathan answering many of the windows
related questions, Allen Day & Scott Cain & Steffen Grossmann for the
work on FeatureIO, GFF3, and SeqFeature::Annotated, Chris Mungall for
the work with Unflattener to merge GenBank annotations into GFF3
objects.

Please see the AUTHORS file for a complete list of contributors.

Jason Stajich on behalf of the Bioperl developers.

[http://portal.open-bio.org/pipermail/bioperl-l/2005-January/018031.html](http://portal.open-bio.org/pipermail/bioperl-l/2005-January/018031.html)

Here is the info from the Changes file.
1.5 Developer release

- Bio::Align::DNAStatistics and Bio::Align::ProteinStatistics provide Jukes-Cantor and Kimura pairwise distance methods, respectively.

- Bio::AlignIO support for "po" format of POA, and "maf"; Bio::AlignIO::largemultifasta is a new alternative to Bio::AlignIO::fasta for temporary file-based manipulation of particularly large multiple sequence alignments.

- Bio::Assembly::Singlet allows orphan, unassembled sequences to be treated similarly as an assembled contig.

- Bio::CodonUsage provides new rare\_codon() and probable\_codons() methods for identifying particular codons that encode a given amino acid.

- Bio::Coordinate::Utils provides new from\_align() method to build a Bio::Coordinate pair directly from a Bio::Align::AlignI-conforming object.

- Bio::DB::Biblio::eutils is a class for querying NCBI's Eutils. Send a Pubmed, Pubmed Central, Entrez, or other query to NCBI's web service using standard Pubmed query syntax, and retrieve results as XML.

- Bio::DB::GFF has various sundry bug fixes.

- Bio::FeatureIO is a new SeqIO-style subsystem for writing/reading genomic features to/from files. I/O classes exist for BED, GTF (aka GFF v2.5), and GFF v3. Bio::FeatureIO classes only read/write Bio::SeqFeature::Annotated objects. Notably, the GFF v3 class requires features to be typed into the Sequence Ontology.

- Bio::Graph namespace contains new modules for manipulation and analysis of protein interaction graphs.

- Bio::Graphics has many bug fixes and shiny new glyphs.

- Bio::Index::Hmmer and Bio::Index::Qual provide multiple-file
  indexing for HMMER reports and FASTA qual files, respectively.

- Bio::Map::Clone, Bio::Map::Contig, and Bio::Map::FPCMarker are
  new objects that can be placed within a Bio::Map::MapI-compliant
  genetic/physical map; Bio::Map::Physical provides a new physical
  map type; Bio::MapIO::fpc provides finger-printed clone mapping
  import.

- Bio::Matrix::PSM provide new support for postion-specific
  (scoring) matrices (e.g. profiles, or "possums").

- Bio::Ontology::Ontology and Bio::Ontology::Term objects can now
  be instantiated without explicitly using Bio::OntologyIO. This
  is possible through changes to Bio::Ontology::OntologyStore to
  download ontology files from the web as necessary. Locations of
  ontology files are hard-coded into
  Bio::Ontology::DocumentRegistry.

- Bio::PopGen includes many new methods and data types for
  population genetics analyses.

- New constructor to Bio::Range, unions(). Given a list of
  ranges, returns another list of "flattened" ranges --
  overlapping ranges are merged into a single range with the
  mininum and maximum coordinates of the entire overlapping group.

- Bio::Root::IO now supports -url, in addition to -file and -fh. The new -url argument allows one to specify the network address of a file for input. -url currently only works for GET requests, and thus is read-only.

- Bio::SearchIO::hmmer now returns individual Hit objects for each domain alignment (thus containing only one HSP); previously separate alignments would be merged into one hit if the domaini nvolved in the alignments was the same, but this only worked when the repeated domain occured without interruption by any other domain, leading to a confusing mixture of Hit and HSP objects.

- Bio::Search::Result::ResultI-compliant report objects now implement the "get\_statistics" method to access Bio::Search::StatisticsI objects that encapsulate any statistical parameters associated with the search (e.g. Karlin's lambda for BLAST/FASTA).

- Bio::Seq::LargeLocatableSeq combines the functionality already found in Bio::Seq::LargeSeq and Bio::LocatableSeq.

- Bio::SeqFeature::Annotated is a replacement for Bio::SeqFeature::Generic. It breaks compliance with the Bio::SeqFeatureI interface because the author was sick of dealing with untyped annotation tags. All Bio::SeqFeature::Annotated annotations are Bio::AnnotationI compliant, and accessible through Bio::Annotation::Collection.

- Bio::SeqFeature::Primer implements a Tm() method for primer melting point predictions.

- Bio::SeqIO now supports AGAVE, BSML (via SAX), CHAOS-XML, InterProScan-XML, TIGR-XML, and NCBI TinySeq formats.

- Bio::Taxonomy::Node now implements the methods necessary for Bio::Species interoperability.

- Bio::Tools::CodonTable has new reverse\_translate\_all() and make\_iupac\_string() methods.

- Bio::Tools::dpAlign now provides sequence profile alignments.

- Bio::Tools::GFF now parses GFF version 2.5 (a.k.a. GTF).

- Bio::Tools::Fgenesh, Bio::Tools::tRNAscanSE are new report parsers.

- Bio::Tools::SiRNA includes two new rulesets (Saigo and Tuschl) for designing small inhibitory RNA.

- Bio::Tree::DistanceFactory provides NJ and UPGMA tree-building methods based on a distance matrix.

- Bio::Tree::Statistics provides an assess\_bootstrap() method to calculate bootstrap support values on a guide tree topology, based on provided bootstrap tree topologies.

- Bio::TreeIO now supports the Pagel (PAG) tree format.
