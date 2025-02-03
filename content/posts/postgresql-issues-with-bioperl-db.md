---
author: dag
category:
  - bioperl
  - obda-/-biosql
date: "2003-02-28T16:59:55+00:00"
guid: http://news.open-bio.org/news/?p=72
title: PostgreSQL issues with bioperl-db
url: /2003/02/28/postgresql-issues-with-bioperl-db/

---
Hilmar writes:

Here's the background.

The current code in the bioperl-db adaptors to biosql run the connection with AutoCommit off, which means the client determines the transaction. Load\_seqdatabase.pl (the main script for loading databases into biosql) treats one sequence entry as one transaction. If any sql statement required for loading the sequence fails unexpectedly, the whole transaction is rolled back, otherwise it is committed once the entry and all its annotation went in successfully. The emphasis rests on 'unexpectedly': INSERTs may fail due to unique key violations, which is caught and triggers a look-up of the affected entry by unique key. E.g. a dbxref may already exist; if so, it needs to be looked up in order to establish the association with the bioentry.

Here's the problem.

If within a transaction a particular statement fails, in Oracle and MySQL/InnoDB only that particular statement fails, not the previous ones in the same transaction, nor the subsequent ones. If you commit the transaction, all the succeeded statements' results get committed. In PostgreSQL, however, the entire transaction fails and is invalidated, making all previous and all subsequent statements fail until you call rollback (you cannot call commit on a failed transaction).

The fulll message and email discussion thread can be read at:
[http://bioperl.org/pipermail/bioperl-l/2003-February/011343.html](http://bioperl.org/pipermail/bioperl-l/2003-February/011343.html)
