---
author: dag
category:
  - obda-/-biosql
date: "2003-05-23T23:51:30+00:00"
guid: http://news.open-bio.org/news/?p=91
title: BioSQL and Bioperl-db inching towards release
url: /2003/05/23/biosql-and-bioperl-db-inching-towards-release/

---
Hilmar writes:

I got the Oracle version of the biosql schema fully migrated, at least as far as I can tell from here. I'm going to commit the new version some time today. There will also be a sql\*plus migration script from pre-Singapore to the current version that supposedly keeps your data intact (be sure to read the disclaimer though).

This means we're getting ready to release Biosql 1.0, possibly as early as next week. If anyone sees any problems with the current schema that he/she thinks should be corrected before this release, please speak up now. I guess I should make an effort and generate an updated ERD before release; the dated ones are confusing wrt the current schema. If there is consensus I'll put out a release candidate early next week.

Bioperl-db should be working against the mysql, PostgreSQL, and Oracle versions (once I've committed that one). The major deficiency here is POD documentation of the modules, specifically updating old modules, and adding/updating the SYNOPSIS sections. I guess a programmer's guide would also be helpful. For the next weeks to come I'm unfortunately not in a position to be able to spend the time it would require to bring the POD documentation up to speed. Would anyone else care to help out? What is generally people's take on how good the documentation should be before we release this? Maybe not care too much and just go ahead to have something officially blessed that can be downloaded?

Jason, with respect to the marker database in bioperl-db, what is your vote on keeping it in the distribution? The problem is that the schema is MySQL-specific, so if someone wants biosql on Pg or Oracle you still have to set up Mysql in order to make all tests pass. An option could be to check the driver in the markerdb-related tests and skip everything if it's not mysql.

The next feature I'm going to add to biosql is a table for expression data that basically resembles the data cube with various dimensions (roughly, bioentry, term \[quantitation type\], term \[sample annotation\]). No LIMS info (yet) other than sample annotation as far as it fits the term table. In my view, this would be a post-1.0 thing. Do people agree?
