---
author: hilmar
category:
  - obda-/-biosql
date: "2008-03-07T01:04:37+00:00"
guid: http://news.open-bio.org/news/?p=146
summary: After a long wait and several earlier attempts, version 1.0.0 (code-named Tokyo, see below) of BioSQL has finally been released. The release can be downloaded at [http://biosql.org/DIST/](http://biosql.org/DIST/) as .tar.gz, .tar.bz, and Zip (which also has Windows-style end-of-line characters) archives. The [full release announcement](http://lists.open-bio.org/pipermail/biosql-l/2008-March/001190.html) can be found in the BioSQL mailing list archives, and in the distribution itself.
title: BioSQL v1.0.0 released
url: /2008/03/06/biosql-v100-released/

---
After a long wait and several earlier attempts, version 1.0.0 (code-named Tokyo, see below) of BioSQL has finally been released. The release can be downloaded at [http://biosql.org/DIST/](http://biosql.org/DIST/) as .tar.gz, .tar.bz, and Zip (which also has Windows-style end-of-line characters) archives. The [full release announcement](http://lists.open-bio.org/pipermail/biosql-l/2008-March/001190.html) can be found in the BioSQL mailing list archives, and in the distribution itself.

This version of the schema has essentially been the same since November 2004. Software that worked with schema versions downloaded from CVS (or, as of lately, svn) after November 2004 should work with all 1.0.x releases. The release contains the core BioSQL schema for several RDBMSs (MySQL, PostgreSQL, Oracle, HSQLDB, and Apache Derby), accompanying documentation, and a Perl script to preload or update the NCBI taxonomy.

BioSQL is a generic, extensible relational model for sequences, sequence features, their annotation, and ontology terms. It is also designed as the interoperable persistence interface between the Bio\* projects. Additional information regarding BioSQL, including links to language bindings, a roadmap to future releases and enhancements, and possible local optimizations is available from the [BioSQL website](http://biosql.org/).

This release and the accompanying work was irreversibly set in motion at the BioHackathon 2008 in Tokyo, and would not have happened without the active encouragement from several hackathon participants, especially Heikki Lehvähslaiho, Mark Schreiber, Richard Holland, and Raoul Bonnal. In recognition of this, and in keeping with an informal tradition held up since the first BioHackathon, I am code-naming the 1.0.x release series the Tokyo release series of BioSQL.

Enjoy!
