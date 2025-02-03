---
author: peterc
category:
  - biopython
  - code
  - community
  - development
  - obf
date: "2009-03-17T14:52:02+00:00"
guid: http://news.open-bio.org/news/?p=250
tag:
  - biopython
  - development
title: Biopython and version control systems
url: /2009/03/17/biopython-and-version-control-systems/

---
Initially for evaluation purposes only, Giovanni and Bartek have setup a mirror of [Biopython on GitHub](http://github.com/biopython/), which is automatically updated from the OBF hosted [Biopython CVS repository](http://www.biopython.org/wiki/CVS). See our [git migration wiki page](http://biopython.org/wiki/GitMigration) for details. If this is favorably received, then moving Biopython from CVS to git seems likely at some point this year.

Originally, all the OBF hosted projects used [CVS](http://www.nongnu.org/cvs/) for their source code repositories. At the start of 2008, [BioPerl](http://www.bioperl.org) and [BioJava](http://www.biojava.org) moved over to [Subversion (SVN)](http://subversion.tigris.org/), followed by [BioSQL](http://www.biosql.org). [Biopython](http://www.biopython.org) was originally going to do the same, but this didn't actually happen. Having all the Bio\* projects using the same version control system would have simplified server administration for the OBF, but using SVN wouldn't really have made that much difference to Biopython development. Discussion on the [Biopython development mailing list](http://biopython.org/pipermail/biopython-dev/) has since shifted towards next-generation distributed version control systems like [git](http://git-scm.com/) or [Bazaar](http://bazaar-vcs.org/).

Quote from Linus Torvalds,

> The slogan of Subversion for a while was ‘CVS done right’, or something like that, and if you start with that kind of slogan, there's nowhere you can go. There is no way to do CVS right.

In addition to creating the Linux kernel, Linus Torvalds more recently wrote [git](http://git-scm.com/), a prominent example of a distributed version control system. Rather than switching from CVS to SVN, the [BioRuby](http://www.bioruby.org) project choose instead to use git, hosted on [github](http://github.com) (see the [BioRuby repository](http://github.com/bioruby/bioruby/tree/master)). Biopython is considering doing something similar - using a _distributed_ version control system like git should make it easier for potential Biopython contributors to manage their own local copies of Biopython under version control.

Peter, on behalf of the Biopython developers
