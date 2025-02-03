---
author: dag
category:
  - bioperl
date: "2003-04-17T20:09:46+00:00"
guid: http://news.open-bio.org/news/?p=89
title: new tab sequence format
url: /2003/04/17/new-tab-sequence-format/

---
Heikki writes:

Philip Lijnzaad has written a new sequence format module called 'tab'.
It is in CVS. Here is the blurb he wrote:

It is very useful when doing large scale stuff using the Unix command
line utilities (grep, sort, awk, sed, split, you name it). Imagine
that you have a format converter 'seqconvert' along the following
lines:

```
my $in  = Bio::SeqIO->newFh(-fh => *STDIN , '-format' => $from);
my $out = Bio::SeqIO->newFh(-fh=> *STDOUT, '-format' => $to);
print $out $_ while <$in>;

```

then you can very easily filter sequence files for duplicates as:

```
$ seqconvert < foo.fa -from fasta -to tab | sort -u |
seqconvert -from tab -to fasta > foo-unique.fa

```

Or grep \[-v\] for certain sequences with:

```
$ seqconvert < foo.fa -from fasta -to tab | grep -v '^S[a-z]*control'|
seqconvert -from tab -to fasta > foo-without-controls.fa

```

Or chop up a huge file with sequences into smaller chunks with:

```
$ seqconvert < all.fa -from fasta -to tab | split -l 10 - chunk-
$ for i in chunk-*; do seqconvert -from tab -to fasta <$i> $i.fa; done
# (this creates files chunk-aa.fa, chunk-ab.fa, ..., each containing
# 10 sequences)

```
