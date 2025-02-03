---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - documentation
  - obf
  - obf-projects
date: "2010-04-05T16:37:11+00:00"
guid: http://news.open-bio.org/news/?p=643
tag:
  - biopython
title: Making Biopython SeqIO and AlignIO easier
url: /2010/04/05/biopython-seqio-and-alignio-easier/

---
One of the small changes coming in Biopython 1.54 (which you can try out already using the [Biopython 1.54 beta](http://news.open-bio.org/news/2010/04/biopython-1-54-beta-released/)) is to [Bio.SeqIO](http://www.biopython.org/wiki/SeqIO) and [Bio.AlignIO](http://www.biopython.org/wiki/AlignIO). Previously the input and output functions had required file _handles_, but they will now also accept _filenames_.

This is a case of _practicality beats purity_ (to quote [the Zen of Python](http://www.python.org/dev/peps/pep-0020/)), and is particularly handy when doing very short scripts or working at the Python prompt.

For example, filtering a FASTA file to take only entries with a minimum length of 100 can be done like this (with handles):

`from Bio import SeqIO
in_handle = open("example.fasta", "rU")
out_handle = open("long.fasta", "w")
records = (rec for rec in SeqIO.parse(in_handle, "fasta") if len(rec)>100)
SeqIO.write(records, out_handle, "fasta")
in_handle.close()
out_handle.close()`

Using filenames it becomes much more concise - just three lines:

`from Bio import SeqIO
records = (rec for rec in SeqIO.parse("example.fasta", "fasta") if len(rec)>100)
SeqIO.write(records, "long.fasta", "fasta")`

This also means Python and Biopython beginners can postpone learning about file handles a little longer, although that may not be an entirely good thing ;)
