---
author: peterc
category:
  - biopython
  - code
  - development
  - obda-/-biosql
  - obf-projects
date: "2010-11-26T16:05:56+00:00"
guid: http://news.open-bio.org/news/?p=756
tag:
  - biopython
  - development
  - release
title: Biopython 1.56 released
url: /2010/11/26/biopython-1-56-released/

---
The Biopython team is pleased to release Biopython 1.56, almost exactly three months after our last stable release ( [Biopython 1.55](http://news.open-bio.org/news/2010/08/biopython-1-55-released/)).

The `Bio.SeqIO` module has been updated to support protein EMBL files (used for the patents database), IMGT files (a variant of the EMBL file format, with help from Uri Laserson), and UniProt XML files (thanks to Andrea Pierleoni). Also the `SeqFeature` object gained some new methods, and the `Bio.Seq` translation function can now be used with an arbitrary genetic code.

`Bio.Entrez` will now try to download any missing NCBI DTD files and cache them in the user's home directory, and includes the latest current DTD files.

The provisional [BioSQL](http://biosql.org) SQLite Schema we've been using since [Biopython 1.53](http://news.open-bio.org/news/2009/12/biopython-release-153/) is now official, and has been updated slightly.

For population genetics, `Bio.PopGen.FDist` now supports the DFDist command line tool as well as FDist2.

Note that [as previously announced](http://news.open-bio.org/news/2010/11/dropping-python24-support/), this is expected to be **our last release to support Python 2.4**. We also support Python 2.5, 2.6 and 2.7, while work is on going for Python 3.

(At least) 13 people have contributed to this release, including 6 new people - thank you all:

- Andrea Pierleoni (first contribution)
- Bart de Koning (first contribution)
- Bartek Wilczynski
- Bartosz Telenczuk (first contribution)
- Cymon Cox
- Eric Talevich
- Frank Kauff
- Michiel de Hoon
- Peter Cock
- Phillip Garland (first contribution)
- Siong Kong (first contribution)
- Tiago Antao
- Uri Laserson (first contribution)

Source distributions and Windows installers are available from the [downloads page](http://www.biopython.org/wiki/Download) on the [Biopython website (biopython.org)](http://www.biopython.org).

As usual, feedback is most welcome on the [mailing lists](http://biopython.org/wiki/Mailing_lists) (or [bugzilla](http://bugzilla.open-bio.org/)).
