---
author: peterc
category:
  - obda-/-biosql
date: "2008-08-13T11:38:39+00:00"
guid: http://news.open-bio.org/news/?p=165
title: BioSQL v1.0.1 released
url: /2008/08/13/biosql-v101-released/

---
This is a belated news entry announcing the second BioSQL v1.0 (code-named Tokyo) release, v1.0.1, which was made on August 2, 2008. It is available from the [BioSQL downloads](http://www.biosql.org/wiki/Downloads) page.

This version of the schema should be fully backwards compatible with the v1.0.0 schema for nearly all software and queries. The only change is relaxing a column width constraint. Migration scripts are for those who want to simply upgrade their existing database.

In addition, the script load\_ncbi\_taxonomy.pl has been fixed to no longer require the taxon primary key and the NCBI taxon ID to be identical. The Bio\* language bindings should not be affected by this change.

For full details, see [Hilmar's official announcement](http://lists.open-bio.org/pipermail/biosql-l/2008-August/001311.html) on the BioSQL mailing list
