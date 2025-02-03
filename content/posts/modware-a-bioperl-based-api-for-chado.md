---
author: just
category:
  - code
date: "2006-05-18T18:00:55+00:00"
guid: http://bioperl.org/news/2006/05/18/modware-a-bioperl-based-api-for-chado/
title: 'Modware: a BioPerl based API for Chado'
url: /2006/05/18/modware-a-bioperl-based-api-for-chado/

---
We are announcing a new Sourceforge Project called Modware. It is an object-oriented API written in Perl that creates BioPerl object representations of biological features stored in a Chado database. It basically creates a Bio::Seq object for chromosomes in Chado and creates Bio::SeqFeature::Gene objects for protein coding transcripts stored in Chado. Things like contigs are represented as Bio::SeqFeature::Generic objects. We also provide many methods for manipulating these objects once they are in memory.

For download please visit our Sourceforge project page:
[http://sourceforge.net/projects/gmod-ware](http://sourceforge.net/projects/gmod-ware)

For API documentation and some short examples of selected use cases visit our project home page:
[http://gmod-ware.sourceforge.net/](http://gmod-ware.sourceforge.net/)
