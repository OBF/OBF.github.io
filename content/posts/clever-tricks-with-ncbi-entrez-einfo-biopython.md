---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - development
  - documentation
  - howto
  - obf
date: "2009-06-21T21:42:05+00:00"
guid: http://news.open-bio.org/news/?p=359
tag:
  - biopython
title: Clever tricks with NCBI Entrez EInfo (& Biopython)
url: /2009/06/21/ncbi-einfo-biopython/

---
Constructing complicated NCBI Entrez searches can be tricky, but it turns out one of the [Entrez Programming Utilities](http://eutils.ncbi.nlm.nih.gov/corehtml/query/static/eutils_help.html) called [Entrez EInfo](http://eutils.ncbi.nlm.nih.gov/corehtml/query/static/einfo_help.html) can help.

For example, suppose you want to search for mitochondrial genomes from a given taxa - either just in the [Entrez web interface](http://www.ncbi.nlm.nih.gov/sites/entrez "NCBI Entrez"), for use in a script with [EFetch](http://eutils.ncbi.nlm.nih.gov/corehtml/query/static/esearch_help.html>ESearch</a> (where you might also download them with <a href=)).

I knew from past experience about using `name[ORGN]` in Entrez to search for an organism name - but how would you specify just mitochondria? I actually worked this out from the NCBI help and exploring the Entrez website's advanced search - but it took a while.

There is an easier way to find out the search fields available in Entrez! Just recently I came across an interesting [blog post from Neil Saunders](http://nsaunders.wordpress.com/2009/05/27/querying-ncbi-entrez-database-fields-using-ruby/) (written a couple of weeks ago) showing how Entrez EInfo provides information about the search fields in XML format, and how you can use Ruby to process this.

[Biopython](http://biopython.org) can do this too of course - using [Bio.Entrez](http://www.biopython.org/DIST/docs/tutorial/Tutorial.html#chapter:entrez) this took just a few lines of Python:

`>>> from Bio import Entrez
>>> data = Entrez.read(Entrez.einfo(db="genome"))
>>> for field in data["DbInfo"]["FieldList"] :
...     print "%(Name)s, %(FullName)s, %(Description)s" % field
...
ALL, All Fields, All terms from all searchable fields
UID, UID, Unique number assigned to each sequence
FILT, Filter, Limits the records
WORD, Text Word, Free text associated with record
TITL, Title, Words in definition line
KYWD, Keyword, Nonstandardized terms provided by submitter
AUTH, Author, Author(s) of publication
JOUR, Journal, Journal abbreviation of publication
VOL, Volume, Volume number of publication
ISS, Issue, Issue number of publication
PAGE, Page Number, Page number(s) of publication
ORGN, Organism, Scientific and common names of organism, and all higher levels of taxonomy
ACCN, Accession, Accession number of sequence
PACC, Primary Accession, Does not include retired secondary accessions
GENE, Gene Name, Name of gene associated with sequence
PROT, Protein Name, Name of protein associated with sequence
ECNO, EC/RN Number, EC number for enzyme or CAS registry number
PDAT, Publication Date, Date sequence added to GenBank
MDAT, Modification Date, Date of last update
SUBS, Substance Name, CAS chemical name or MEDLINE Substance Name
PROP, Properties, Classification by source qualifiers and molecule type
SQID, SeqID String, String identifier for sequence
GPRJ, Genome Project, Genome Project
SLEN, Sequence Length, Length of sequence
FKEY, Feature key, Feature annotated on sequence
RTYP, Replicon type, Replicon type
RNAM, Replicon name, Replicon name
ORGL, Organelle, Organelle
`

That gives us a list of all the fields we can currently search on in the Genome database (and you could use the same code for any of the other NCBI databases in Entrez - they probably all have different searchable fields). Very handy! The ones in bold are discussed below.

So for my particular search, using "ORGL" to filter on organelle looks sensible, and after a bit of trial and error on the website I ended up with `mitochondrion[ORGL]` as a useful filter (not mitochondrial, or mitochondria).

I already knew about using "ORGN" to filter on the organism, either by species name or with a suitably formatted NCBI taxon ID (which you can get by searching or browsing the Entrez taxonomy database), e.g. `txid9443[ORGN]` gives [primates](http://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=9443).

Putting these together, to get [all the primate mitochondria in the Entrez genome database](http://www.ncbi.nlm.nih.gov/sites/entrez?db=genome&term=txid9443[ORGN]%20AND%20mitochondrion[ORGL]) you could use:

> txid9443\[ORGN\] AND mitochondrion\[ORGL\]

Note that you have to use "AND" in upper case.

I think we'll have to add something along these lines to the [Biopython Tutorial and Cookbook](http://www.biopython.org/DIST/docs/tutorial/Tutorial.html) ( [PDF](http://www.biopython.org/DIST/docs/tutorial/Tutorial.pdf))... _Update: That's done now and will be included with our next release_ :)

Entrez rocks! (although their documentation could use a few more examples).

Peter
