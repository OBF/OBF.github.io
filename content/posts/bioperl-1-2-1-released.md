---
author: dag
category:
  - bioperl
date: "2003-04-01T02:56:44+00:00"
guid: http://news.open-bio.org/news/?p=86
summary: |-
  The release is available at
  [http://www.bioperl.org/ftp/DIST/bioperl-1.2.1.tar.gz](  http://www.bioperl.org/ftp/DIST/bioperl-1.2.1.tar.gz)
  and is propagating around CPAN now.
title: Bioperl-1.2.1 released
url: /2003/03/31/bioperl-121-released/

---
The release is available at
[http://www.bioperl.org/ftp/DIST/bioperl-1.2.1.tar.gz](  http://www.bioperl.org/ftp/DIST/bioperl-1.2.1.tar.gz)
and is propagating around CPAN now.

The main bug fixes in this release are:

\- inclusion of WrapperBase, making StandAloneBlast work from the
release

\- fixes and cleanup of Bio::Coordinate

\- fixes to Bio::Index::EMBL and bpindex

The 1.2.1 release does see some major additions in the Ontology area.
These were not present in the 1.2 release, so nothing should break. The
inclusion of these modules into the stable branch (something which
normally should not happen) was specifically so that the bioperl-db
project, the bioperl bindings of the cross-language BioSQL project can
be targetted to work with the 1.2 stable series, rather than the
development releases. We (the core) believe that this was the best
solution, encouraging a stable release of bioperl-db (due out I suspect in
a month or so - Hilmar Lapp is the driver for this).

As always, the release was herded out by the Bioperl developers. Special
mention goes to both Jason Stajich and Heikki Lehvaslaiho for their bug
fixing and tweaking, and to Hilmar Lapp for the ontology modules.

Enjoy!
