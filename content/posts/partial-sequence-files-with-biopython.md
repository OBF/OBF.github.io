---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - howto
  - obf
  - obf-projects
date: "2010-04-27T13:03:04+00:00"
guid: http://news.open-bio.org/news/?p=659
tag:
  - biopython
title: Partial sequence files with Biopython
url: /2010/04/27/partial-seq-files-biopython/

---
This is another blog post to highlight one of the neat tricks you'll be able to do with Biopython 1.54 (which you can help test with the [Biopython 1.54 beta](http://news.open-bio.org/news/2010/04/biopython-1-54-beta-released/) release).

It is often useful to be able to extract a few records from a larger sequence file - for example, some sequences of interest from a full UniProt or GenBank dump. One obvious way to try to do this is to parse the file into an object representation (i.e. `SeqRecord` objects using `Bio.SeqIO.parse(...)`), filter to pick out the entries you want, and then write them back to disk (using `Bio.SeqIO.write(...)`). However, for complex file formats like GenBank this can be lossy ( `Bio.SeqIO` does not support a 100% identical round trip), and Biopython don't currently support writing out the SwissProt plain text format used by UniProt. So, that approach won't work.

[Biopython 1.52](http://news.open-bio.org/news/2009/09/biopython-release-152/) introduced a new [indexing function](http://news.open-bio.org/news/2009/09/biopython-seqio-index/), `Bio.SeqIO.index(...)`, which allows a large multi-sequence file to be treated like a Python dictionary - parsing requested records on request. This has been enhanced for Biopython 1.54 with a method `get_raw(...)` to extract the raw for a record as a string.

How is this useful? Well, take your large (UniProt) file, index it, then extract the records you want and write them to your output file unmodified:

```
from Bio import SeqIO
uniprot = SeqIO.index("uniprot_sprot.dat", "swiss")
handle = open("selected.dat", "w")
for acc in ["P33487", "P19801", "P13689", "Q8JZQ5", "Q9TRC7"]:
    handle.write(uniprot.get_raw(acc))
handle.close()

```

Another neat use of this functionality would be to sort entries in a sequential file format, and there is an example of that in the [Biopython Tutorial](http://biopython.org/DIST/docs/tutorial/Tutorial.html) ( [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf)).
