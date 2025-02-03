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
  - obf
  - obf-projects
date: "2010-04-30T07:49:45+00:00"
guid: http://news.open-bio.org/news/?p=677
tag:
  - biopython
  - fastq
title: Illumina FASTQ files - Read Segment Quality Control Indicator
url: /2010/04/30/illumina-q2-trim-fastq/

---
In another quirk to the [FASTQ story](http://news.open-bio.org/news/2009/12/nar-fastq-format/), recent Illumina FASTQ files don't actually use the full range of PHRED scores - and a score of 2 has a special meaning, _The Read Segment Quality Control Indicator_ (RSQCI, encoded as 'B').

Hats off to _Dr Torsten Seemann_ for raising awareness of this issue in [his post on the seqanswers.com forum](http://seqanswers.com/forums/showpost.php?p=17491&postcount=3), referring to a presentation by _Tobias Mann_ of Illumina which says:

> _The Read Segment Quality Control Indicator:_
>
> _- At the ends of some reads, quality scores are unreliable. Illumina has an algorithm for identifying these unreliable runs of quality scores, and we use a special indicator to flag these portions of reads_
>
> _- A quality score of 2, encoded as a "B", is used as a special indicator. A quality score of 2 does not imply a specific error rate, but rather implies that the marked region of the read should not be used for downstream analysis._
>
> _- Some reads will end with a run of B (or Q2) basecalls, but there will never  be an isolated Q2 basecall._

So, armed with this knowledge, you might want to apply a simple trimming criteria to any Illumina FASTQ files - remove anything after and including a PHRED quality score of 2 (encoded as ASCII 'B').

We could do this with the rich object orientated `SeqRecord` based API in Biopython, but when [dealing with massive FASTQ files](http://news.open-bio.org/news/2009/09/biopython-fast-fastq/) this overhead matters. Instead we'll stick with plain Python strings:

`from Bio.SeqIO.QualityIO import FastqGeneralIterator
handle = open("B_trimmed.fastq", "w")
min_length = 10
for title, seq, qual in FastqGeneralIterator(open("untrimmed.fastq")) :
    #Find the location of the first "B" (PHRED quality 2)
    trim = qual.find("B")
    if trim == -1:
        #No need to trim
        handle.write("@%sn%sn+n%sn" % (title, seq, qual))
    elif trim >= min_length:
        #Take everything up to the first B
        handle.write("@%sn%sn+n%sn" % (title, seq[:trim], qual[:trim]))
handle.close()`

In practice the above can trim too much - you can still get isolated "B" characters in the middle of a read, where it is just a low quality score. Instead, we can trim any trailing "B" characters - which will do the same thing on RSQCI based FASTQ files where the "B" should only appear at the end:

`from Bio.SeqIO.QualityIO import FastqGeneralIterator
handle = open("B_trimmed.fastq", "w")
min_length = 10
for title, seq, qual in FastqGeneralIterator(open("untrimmed.fastq")) :
    qual = qual.rstrip("B") #Remove any trailing B characters
    length = len(qual)
    if length >= min_length:
        seq = seq[:length] #trim to match
        handle.write("@%sn%sn+n%sn" % (title, seq, qual))
handle.close()`

You could easily modify this example to read from stdin and write to stdout (see this [cookbook example](http://www.biopython.org/wiki/Reading_from_unix_pipes)), or take filenames as command line arguments to turn this into a general purpose "FASTQ B-trimming script".
