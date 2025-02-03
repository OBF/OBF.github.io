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
date: "2009-12-14T14:03:41+00:00"
guid: http://news.open-bio.org/news/?p=513
summary: This post is about paired end data (FASTA or FASTQ) and manipulating it with Biopython's [Bio.SeqIO](http://biopython.org/wiki/SeqIO) module (see also [FASTQ conversions](http://news.open-bio.org/news/2009/09/biopython-convert-function/) & [speeding up FASTQ](http://news.open-bio.org/news/2009/09/biopython-fast-fastq/)).
tag:
  - biopython
  - fastq
title: Interleaving paired FASTQ files with Biopython
url: /2009/12/14/interleaving-paired-fastq-files-with-biopython/

---
This post is about paired end data (FASTA or FASTQ) and manipulating it with Biopython's [Bio.SeqIO](http://biopython.org/wiki/SeqIO) module (see also [FASTQ conversions](http://news.open-bio.org/news/2009/09/biopython-convert-function/) & [speeding up FASTQ](http://news.open-bio.org/news/2009/09/biopython-fast-fastq/)).

There are two main ways of presenting paired end data in FASTA or FASTQ files:

- Paired files, with matching entries for the forward and reverse reads (probably the norm with Illumina data)
- Single files, with alternating entries for the forward and reverse reads (used by Velvet)

Converting between these two is a relatively common operation, and is normally pretty easy. There was a [short example](http://lists.open-bio.org/pipermail/biopython/2009-September/005584.html) of how you might do this in Biopython on a recent (September 2009) Velvet users/Biopython mailing list discussion. That script didn't check the record IDs matched up (but neither does the Perl script shuffleSequences\_fastq.pl included with Velvet for this task).

It would be safer to check the record IDs do match. However, there are several different naming schemes for reads, most typically suffixes of `/1` and `/2`, but also things like `.f` and `.r` get used. In the case of FASTQ files from the NCBI SRA, the reads have no suffixes, so to feed those into Velvet you may want to check they are equal and then add a suffix as shown below.

` `

```
#This Python script requires Biopython 1.51 or later
from Bio import SeqIO
import itertools

#Setup variables (could parse command line args instead)
file_f = "SRR001666_1.fastq"
file_r = "SRR001666_2.fastq"
file_out = "SRR001666_interleaved.fastq"
format = "fastq" #or "fastq-illumina", or "fasta", or ...

def interleave(iter1, iter2) :
    for (forward, reverse) in itertools.izip(iter1,iter2):
        assert forward.id == reverse.id
        forward.id += "/1"
        reverse.id += "/2"
        yield forward
        yield reverse

records_f = SeqIO.parse(open(file_f,"rU"), format)
records_r = SeqIO.parse(open(file_r,"rU"), format)

handle = open(file_out, "w")
count = SeqIO.write(interleave(records_f, records_r), handle, format)
handle.close()
print "%i records written to %s" % (count, file_out)

```

This example uses the [SRR001666](http://www.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?cmd=viewer&m=data&s=viewer&run=SRR001666) files from the [NCBI SRA FTP site](ftp://ftp.ncbi.nlm.nih.gov/sra/static/SRX000/SRX000430/).

Now that works fine, and just by changing the filenames and the format name this could be used on FASTA data (or another supported file format). The bad news is it took 14 minutes to produce a 2GB FASTQ. However, going a little more low-level [as discussed before](http://news.open-bio.org/news/2009/09/biopython-fast-fastq/) can really pay off. This FASTQ-only version takes just 2 minutes:

` `

```
#This Python script requires Biopython 1.51 or later
from Bio.SeqIO.QualityIO import FastqGeneralIterator
import itertools

#Setup variables (could parse command line args instead)
file_f = "SRR001666_1.fastq"
file_r = "SRR001666_2.fastq"
file_out = "SRR001666_interleaved.fastq"

handle = open(file_out, "w")
count = 0

f_iter = FastqGeneralIterator(open(file_f,"rU"))
r_iter = FastqGeneralIterator(open(file_r,"rU"))
for (f_id, f_seq, f_q), (r_id, r_seq, r_q)
in itertools.izip(f_iter,r_iter):
    assert f_id == r_id
    count += 2
    #Write out both reads with "/1" and "/2" suffix on ID
    handle.write("@%s/1n%sn+n%sn@%s/2n%sn+n%sn"
                 % (f_id, f_seq, f_q, r_id, r_seq, r_q))
handle.close()
print "%i records written to %s" % (count, file_out)
```

You can make this a little faster still by missing out most of the validation done by the Biopython FASTQ parser - but personally I wouldn't take that risk. I'd much rather know about any errors in the data.

Peter

P.S.

Things get more interesting if you want to do quality filtering or trimming. If only one of a pair passes the quality assurance step, then you may want to keep it and treat it as an unpaired read. To give such cleaned up data to Velvet, you would need one file of alternating paired end reads, and a separate file of the orphaned effectively unpaired reads. That deserves another post going into more detail...
