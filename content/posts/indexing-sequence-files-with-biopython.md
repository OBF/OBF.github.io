---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - documentation
  - howto
  - obf-projects
date: "2009-09-21T17:37:12+00:00"
guid: http://news.open-bio.org/news/?p=396
tag:
  - biopython
  - fastq
title: Indexing sequence files with Biopython
url: /2009/09/21/biopython-seqio-index/

---
The forthcoming release of [Biopython 1.52](http://news.open-bio.org/news/2009/09/biopython-release-152/) will include a couple of nice improvements to the [Bio.SeqIO module](http://biopython.org/wiki/SeqIO), and here we're going to introduce the new **index** function. This will of course be covered in the [Biopython Tutorial & Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html) ( [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)) once this code is released.

Suppose you have a _large_ sequence file with many many individual sequences in it. This could be next generation sequence data for example, maybe a FASTQ, FASTA or QUAL file. Or, it might be a big annotation rich file, such as the whole of UniProt, or a chunk of GenBank.

The **Bio.SeqIO.parse(...)** function lets you iterate over all the records in a file, one by one. This allows you to process each sequence in turn, keeping only one in memory at a time. This approach is _very_ valuable for dealing with big files.

However, sometimes you can't just loop over the records in the order found in the file. You may _require_ random access. In Python, the natural API here is a dictionary - for example looking up the records via their ID string. This is how the existing **Bio.SeqIO.to\_dict(...)** function works. It is just a helper function to build an _in memory_ dictionary of a collection of SeqRecord objects. However, because everything is kept in memory (RAM), this only works on small or medium sized files. :(

So, what should you do when you have a very large file, and it is no longer possible to load everything into memory at once? Well, you might consider using a [BioSQL](http://biosql.org) database - this is probably quite a sensible option for something like GenBank data. However, for next generation sequencing data this is probably overkill. This is where the new **Bio.SeqIO.index(...)** function comes in. It behaves like a Python dictionary, but doesn't keep everything in memory at once!

What **Bio.SeqIO.index(...)** does is first quickly scan the file looking for the position of each new record, and records this information against the record ID string. This still requires a reasonable amount of memory, but works fine even for millions of entries in a file. Then, when you ask for a particular record, it jumps to the relevant part of the file, and then parses the data into a SeqRecord.

For example, consider the FASTQ file SRR014849.fastq (available [compressed at the NCBI](ftp://ftp.ncbi.nlm.nih.gov/sra/static/SRX003/SRX003639/SRR014849.fastq.gz)). The **Bio.SeqIO.index(...)** function takes a minimum of two arguments, the filename and the file format:

`
>>> from Bio import SeqIO
>>> data = SeqIO.index("SRR014849.fastq", "fastq")
>>> len(data)
94696
>>> data.keys()[:3]
['SRR014849.80961', 'SRR014849.80960', 'SRR014849.80963']
>>> print data["SRR014849.290838"].seq
TGAGAATTTTTATTTTCAAGGGTTGGAACCGAAGGGTTTGAATTCAAACCCTTTCGGTTCCAACCCGACAAGTCATCGATGTTG
>>> print data["SRR014849.290838"].letter_annotations["phred_quality"]
[20, 18, 24, 25, 33, 26, 37, 33, 22, 11, 1, 22, 37, 33, 22, 10, 25, 31, 26, 36, 32, 16, 33, 26, 31, 25, 33, 25, 31, 25, 22, 33, 26, 35, 30, 12, 35, 31, 17, 19, 30, 20, 33, 26, 27, 31, 27, 6, 36, 32, 15, 33, 29, 10, 27, 32, 24, 30, 25, 30, 20, 24, 13, 35, 31, 13, 27, 26, 28, 32, 24, 28, 28, 27, 22, 22, 26, 28, 26, 24, 27, 30, 22, 27]`

In this case the FASTQ file is only 24MB (so the example is easy to try at home), but the same approach works just as well on a 1GB FASTQ file :)

This will be covered in more detail by the new edition of the [Biopython Tutorial & Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html), and once you have Biopython 1.52 or later installed don't forget about the built in help:

`>>> from Bio import SeqIO
>>> help(SeqIO.index)
...
`

Biopython 1.52 will index most of the file formats that can already be parsed with the SeqIO library - but not any multiple alignment formats. There is a table on the [Bio.SeqIO wiki page](http://biopython.org/wiki/SeqIO).

Enjoy!

Peter

P.S. Note that random access to all the records in a sequence file isn't the only potential benefit of using **Bio.SeqIO.index(...)**. Suppose you are only interested in a few entries in a large file. You could use a for loop with **Bio.SeqIO.parse(...)**, but this will mean every single record gets parsed and turned into a SeqRecord. If instead you used **Bio.SeqIO.index(...)** then only the few records you care about get parsed and turned into SeqRecord objects. This can save a lot of time, especially for an annotation rich format like SwissProt or GenBank.
