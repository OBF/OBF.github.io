---
author: davidw
category:
  - biopython
  - blogroll
  - code
  - development
  - documentation
  - howto
  - obf
  - obf-projects
date: "2009-09-22T10:24:57+00:00"
guid: http://news.open-bio.org/news/?p=409
tag:
  - biopython
  - fastq
title: Simpler, optimized format conversion with Biopython
url: /2009/09/22/biopython-convert-function/

---
As per [Peter's recent post](http://news.open-bio.org/news/2009/09/biopython-seqio-index/ "Indexing sequence files with Biopython") we are using this space to show of a couple of the new features in [Biopython](http://biopython.org) 1.52 before it is released. In this post we'll look at the new **convert()** function that both [Bio.SeqIO](http://biopython.org/wiki/SeqIO) and [Bio.AlignIO](http://biopython.org/wiki/AlignIO) will get in Biopython 1.52.

No one has ever complained that bioinformatics just doesn't have enough file formats - you probably frequently find yourself converting sequence files to suit particular applications with **Bio.SeqIO**. At the moment this is usually a two step process, something like this:

`>>> records = SeqIO.parse(in_handle "genbank")
>>> SeqIO.write(records, out_handle, "fasta")`

As of Biopython 1.52, you'll be able to achieve the same result in a single step:

`>>> SeqIO.convert(in_handle, "genbank", out_handle, "fasta")`

In fact, it's even easier than that because the convert function will accept filename strings as well as file handles for both input and output.

Adding the convert function to **Bio.SeqIO** and **Bio.AlignIO** will make your scripts more readable and might even save you a couple of lines of code, but perhaps more importantly it allows for the conversion process to be optimized for the two formats being used. In most cases the same old parse and write functions are called internally, however some key conversions are much faster...

In the above example we are moving from a GenBank file, which probably includes multiple features for each sequence, to a FASTA file, which doesn't include features. If we used the two step process above we'd be spending time reading each sequence's features into memory just to skip them when they get passed to the write function. **Bio.SeqIO.convert()** knows that the sequences in the input file are destined to be written to a FASTA file so it can skip over the features and save a bit of time in doing the conversion.

Obviously, any optimization is most important when its used on very large files, like those produced in next generation sequencing projects. For example, when converting between each of the FASTQ file formats variants with the "SeqIO two step" a significant amount of time is taken creating [SeqRecord objects](http://biopython.org/wiki/SeqRecord) for each record in the input file and decoding the quality scores into numbers. However, none of the attributes or methods of the SeqRecord object are required to do the conversion. For this reason **Bio.SeqIO.convert()** deals with each record as simple strings. This makes it about five times faster - on a par with converters written in C.

The Biopython 1.52 edition of the [Biopython Tutorial & Cookbook](http://biopython.org/DIST/docs/tutorial/Tutorial.html) ( [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)) will cover these new convert functions in more detail.
