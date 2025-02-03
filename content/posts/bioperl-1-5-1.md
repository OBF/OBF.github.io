---
author: stajich
category:
  - bioperl
date: "2005-10-14T01:14:28+00:00"
guid: http://news.open-bio.org/news/?p=136
summary: |-
  I am pleased to announce the 1.5.1 developer release of Bioperl.

  Essential links here
  Core
  [http://bioperl.org/DIST/bioperl-1.5.1.tar.gz](http://bioperl.org/DIST/bioperl-1.5.1.tar.gz) [http://bioperl.org/DIST/bioperl-1.5.1.zip](http://bioperl.org/DIST/bioperl-1.5.1.zip) [http://bioperl.org/DIST/bioperl-1.5.1.tar.bz2](http://bioperl.org/DIST/bioperl-1.5.1.tar.bz2)

  Run
  [http://bioperl.org/DIST/bioperl-run-1.5.1.tar.gz](http://bioperl.org/DIST/bioperl-run-1.5.1.tar.gz) [http://bioperl.org/DIST/bioperl-run-1.5.1.zip](http://bioperl.org/DIST/bioperl-run-1.5.1.zip) [http://bioperl.org/DIST/bioperl-run-1.5.1.tar.bz2](http://bioperl.org/DIST/bioperl-run-1.5.1.tar.bz2)

  Ext
  [http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.gz](http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.gz) [http://bioperl.org/DIST/bioperl-ext-1.5.1.zip](http://bioperl.org/DIST/bioperl-ext-1.5.1.zip) [http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.bz2](http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.bz2)

  MD5 sum
  [http://bioperl.org/DIST/SIGNATURES.md5](http://bioperl.org/DIST/SIGNATURES.md5)

  Please see [my mailing list post](http://portal.open-bio.org/pipermail/bioperl-l/2005-October/019932.html) for more information.
title: Bioperl 1.5.1
url: /2005/10/13/bioperl-151/

---
I am pleased to announce the 1.5.1 developer release of Bioperl.

Essential links here
Core
[http://bioperl.org/DIST/bioperl-1.5.1.tar.gz](http://bioperl.org/DIST/bioperl-1.5.1.tar.gz) [http://bioperl.org/DIST/bioperl-1.5.1.zip](http://bioperl.org/DIST/bioperl-1.5.1.zip) [http://bioperl.org/DIST/bioperl-1.5.1.tar.bz2](http://bioperl.org/DIST/bioperl-1.5.1.tar.bz2)

Run
[http://bioperl.org/DIST/bioperl-run-1.5.1.tar.gz](http://bioperl.org/DIST/bioperl-run-1.5.1.tar.gz) [http://bioperl.org/DIST/bioperl-run-1.5.1.zip](http://bioperl.org/DIST/bioperl-run-1.5.1.zip) [http://bioperl.org/DIST/bioperl-run-1.5.1.tar.bz2](http://bioperl.org/DIST/bioperl-run-1.5.1.tar.bz2)

Ext
[http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.gz](http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.gz) [http://bioperl.org/DIST/bioperl-ext-1.5.1.zip](http://bioperl.org/DIST/bioperl-ext-1.5.1.zip) [http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.bz2](http://bioperl.org/DIST/bioperl-ext-1.5.1.tar.bz2)

MD5 sum
[http://bioperl.org/DIST/SIGNATURES.md5](http://bioperl.org/DIST/SIGNATURES.md5)

Please see [my mailing list post](http://portal.open-bio.org/pipermail/bioperl-l/2005-October/019932.html) for more information.

I have appended the Change log from Bioperl core compents below
1.5.1 Developer release

o Major problem with how Annotations were written out with
Bio::Seq is fixed by reverting to old behavior for
Bio::Annotation objects.

o Bio::SeqIO

\- genbank.pm
\\* bug #1871; REFLOOP' parsing loop, I changed the pattern to
expect at l east 9 spaces at the beginning of a line to
indicate line wrapping.

\\* Treat multi-line SOURCE sections correctly, this defect broke
both common\_name() and classification()

\\* parse swissprot fields in genpept file

\\* parse WGS genbank records

\- embl.pm
\\* Changed regexp for ID line. The capturing parentheses are
the same, the difference is an optional repeated-not-semi-
colon expression following the captured S+. This means the
regexp works when the division looks like /PRO;/ or when the
division looks like /ANG ;/ - the latter is from EMBL
repbase

\\* fix ID line parsing: the molecule string can have spaces in
it. Like: "genomic DNA"

\- swiss.pm: bugs #1727, #1734

\- entrezgene.pm
\\* Added parser for entrezgene ASN1 (text format) files.
Uses Bio::ASN1::EntrezGene as a low level parser (get it from CPAN)

o Bio::AlignIO

\- maf.pm coordinate problem fixed

o Bio::Taxonomy and Bio::DB::Taxonomy

\- Parse NCBI XML now so that nearly all the taxonomy up-and-down
can be done via Web without downloading all the sequence.
o Bio::Tools::Run::RemoteBlast supports more options and complies
to changes to the NCBI interface. It is reccomended that you
retrieve the data in XML instead of plain-text BLAST report to
insure proper parsing and retrieval of all information as NCBI
fully expects to change things in the future.
o Bio::Tree and Bio::TreeIO

\- Fixes so that re-rooting a tree works properly

\- Writing out nhx format from a newick/nexus file will properly output
bootstrap information. The use must move the internal node labels over
to bootstraps.
for my $node ( grep { ! $\_->is\_Leaf } $tree->get\_nodes ) {
$node->bootstrap($node->id);
$node->id('');
}
\- Nexus parsing is much more flexible now, does not care about
LF.

\- Cladogram drawing module in Bio::Tree::Draw

\- Node height and depth now properly calculated

\- fix tree pruning algorithm so that node with 1 child gets merged

o Graphics tweaks. Glyph::xyplot improved. Many other small-medium sized
bugs and improvements were added, see Gbrowse mailing list for most of
these.

o Bio::DB::GFF partially supports GFF3. See information about
gff3\_munge flag in scripts/Bio-DB-GFF/bulk\_load\_gff.pl.

o Better location parsing in Bio::Factory::FTLocationFactory -
this is part of the engine for parsing EMBL/GenBank feature table
locations. Nested join/order-by/complement are allowed now

o Bio::PrimarySeqI->translate now takes named parameters

o Bio::Tools::Phylo::PAML - parsing RST (ancestral sequence
reconstruction) is now supported. Parsing different models and
branch specific parametes are now supported.

o Bio::Factory::FTLocationFactory - parse hierarchical locations
(joins of joins)

o Bio::Matrix::DistanceMatrix returns arrayrefs instead of arrays
for getter/setter functions

o Bio::SearchIO

\- blast bug #1739; match scientific notation in score
and possible e+ values

\- blast.pm reads more WU-BLAST parameters and parameters, match
a full database pathname,

\- Handle NCBI WEB and newer BLAST formats specifically
(Query\|Sbjct:) match in alignment blocks can now be (Query\|Sbjct).

\- psl off-by-one error fixed

\- exonerate parsing much improved, CIGAR and VULGAR can be parsed
and HSPs can be constructed from them.

\- HSPs query/hit now have a seqdesc field filled out (this was
always available via $hit->description and
$result->query\_description

\- hmmer.pm can parse -A0 hmmpfam files

\- Writer::GbrowseGFF more customizeable.

o Bio::Tools::Hmmpfam
make e-value default score displayed in gff, rather than raw score
allow parse of multiple records
