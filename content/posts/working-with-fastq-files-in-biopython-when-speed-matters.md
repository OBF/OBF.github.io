---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - documentation
  - howto
  - obf-projects
date: "2009-09-25T11:49:53+00:00"
guid: http://news.open-bio.org/news/?p=432
tag:
  - biopython
  - fastq
title: Working with FASTQ files in Biopython when speed matters
url: /2009/09/25/biopython-fast-fastq/

---
[Biopython 1.51](http://news.open-bio.org/news/2009/08/biopython-1-51-released/) onward includes support for Sanger, Solexa and Illumina 1.3+ FASTQ files in [Bio.SeqIO](http://biopython.org/wiki/SeqIO), which allows a lot of neat tricks very concisely. For example, the [tutorial](http://biopython.org/DIST/docs/tutorial/Tutorial.html) ( [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)) has examples finding and removing primer or adaptor sequences.

However, because the Bio.SeqIO interface revolves around [SeqRecord objects](http://biopython.org/wiki/SeqRecord) there is often a speed penalty. For example for [FASTQ files](http://en.wikipedia.org/wiki/FASTQ_format), the quality string gets turned into a list of integers on parsing, and then re-encoded back to ASCII on writing.

The new [Bio.SeqIO.convert(...)](http://news.open-bio.org/news/2009/09/biopython-convert-function/) function in [Biopython 1.52](http://news.open-bio.org/news/2009/09/biopython-release-152/) onwards makes converting from FASTQ to FASTA, or between the FASTQ variants about five times faster. It can do this because it doesn't bother with creating any objects - it just uses Python strings.

You can use the same approach in your own scripts. For example, suppose you have a Solexa FASTQ file where you want to trim all the reads, taking just the first 21 bases (say). Why might you want to do this? Well, in Solexa/Illumina there is a general decline in read quality along the sequence, so it can make sense to trim, and some algorithms like to have all the input reads the same length. Here is how I would write this using the standard Bio.SeqIO functions:

```
from Bio import SeqIO
records = (rec[:21] for rec in SeqIO.parse(open("untrimmed.fastq"), "fastq-solexa"))
handle = open("trimmed21.fastq", "w")
count = SeqIO.write(records, handle, "fastq-solexa")
handle.close()
print "Trimmed %i FASTQ records" % count
```

This works, and is very simple and general. The same template can be used on any file formats supported by [Bio.SeqIO](http://biopython.org/wiki/SeqIO). However, it might be a bit slow for large next generation sequence files.

Instead, we can get a little more low level - and work directly with strings. This requires you to know more about the details of the FASTQ file format. Parsing FASTQ files is surprising complicated (with nasty things like line wrapping technically allowed), so we'll still get Biopython to do that bit - but not bother with constructing SeqRecord objects and decoding the FASTQ quality strings. On the other hand, doing the FASTQ output explicitly isn't actually too bad once you know how things work:

```
from Bio.SeqIO.QualityIO import FastqGeneralIterator
trim = 21
handle = open("trimmed21.fastq", "w")
for title, seq, qual in FastqGeneralIterator(open("untrimmed.fastq")) :
    handle.write("@%sn%sn+n%sn" % (title, seq[:trim], qual[:trim]))
handle.close()
```

Again, the solution is a very short script - but this time it is much less flexible, and not nearly as clear what is going on. On the bright side, it is many times faster. Deciding on this trade-off is down to you, but I hope this blog post has highlighted the potential usefulness of the FastqGeneralIterator function in Bio.SeqIO.QualityIO, which you might otherwise have overlooked. To find out more, please read the built in documentation (also available [online](http://biopython.org/DIST/docs/api/Bio.SeqIO.QualityIO-module.html#FastqGeneralIterator "Documentation for Bio.SeqIO.QualityIO function FastqGeneralIterator")):

```
from Bio.SeqIO.QualityIO import FastqGeneralIterator
>>> help(FastqGeneralIterator)
...

```

Please sign up to the [Biopython mailing list](http://biopython.org/wiki/Mailing_lists) if you want to discuss this topic further.

Peter

_Update_: A similar parser for FASTA files for looping over the records as strings was added in Biopython 1.61,

```
>>> from Bio.SeqIO.FastaIO import SimpleFastaParser
>>> help(SimpleFastaParser)
...
```
