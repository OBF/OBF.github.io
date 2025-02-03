---
author: heikki
category:
  - bioperl
date: "2003-07-16T02:31:43+00:00"
guid: http://news.open-bio.org/news/?p=107
summary: |-
  Rob Edwards and Heikki Lehvaslaiho have been writing new restriction analysis classes. These will eventually replace the long serving Bio::Tools::RestrictionEnzyme by Steve Chervitz. The first working
  versions are in CVS.

  [A UML graph](http://bio.perl.org/images/bio_restriction.png) shows the class relationships. A more verbose overview is below.
title: new restriction analysis classes
url: /2003/07/15/new-restriction-analysis-classes/

---
Rob Edwards and Heikki Lehvaslaiho have been writing new restriction analysis classes. These will eventually replace the long serving Bio::Tools::RestrictionEnzyme by Steve Chervitz. The first working
versions are in CVS.

[A UML graph](http://bio.perl.org/images/bio_restriction.png) shows the class relationships. A more verbose overview is below.

**Bio::Restriction::Enzyme** class knows (almost) everything there to know about restriction enzymes.

There are two subclasses of Enzyme: 1) Bio::Restriction::Enzyme::MultiSite and 2) Bio::Restriction::Enzyme::MultiCut that handle relatively rare cases when recognition sites of the enzyme is more complex than can be expressed using IUPAC code or there are four cut sites per site.

**Bio::Restriction::EnzymeCollection** object is a set of Enzymes. It is created by Bio::Restriction::IO. This class works like Bio::SeqIO class, but if you call it without parameters, you get a default selection of 530 bare-boned Enzymes.

If you want select your own set, you can read in data from REBASE database flat files. Two formats, _itype2_ and _withrefm_, are now supported.

Any attribute of an Enzyme can easily be used to filter them out of one collection into an other.

**Bio::Restriction::Analysis** uses an EnzymeCollection to cut any Bio::PrimarySeqI implementing sequence into fragments. There are methods to find enzymes that cut the sequence to a given number of time, or do not cut at all, and retrieve the fragments.
