---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - obf-projects
date: "2010-11-18T15:09:15+00:00"
guid: http://news.open-bio.org/news/?p=751
tag:
  - biopython
  - development
title: Biopython dropping Python 2.4 Support?
url: /2010/11/18/dropping-python24-support/

---
This is a reminder that the forthcoming Biopython 1.56 release is _planned_ to be our last release to support Python 2.4.

Looking back, we supported Python 2.3 for about six years - it was released July 2003, and [Biopython 1.50](http://news.open-bio.org/news/2009/04/biopython-release-150/) released in April 2009 was the last to support it. Similarly, Python 2.4 was released six years ago (November 2004).

Dropping Python 2.4 support will allow use to assume standard library modules like the [ElementTree XML parser](http://docs.python.org/library/xml.etree.elementtree.html) and [SQLite 3 support](http://docs.python.org/library/sqlite3.html) will be available. There are also several [new language features in Python 2.5+](http://docs.python.org/whatsnew/2.5.html) which will be useful, and it should make supporting Python 3 a little easier as well.

Most operating systems which come with Python now ship with Python 2.5 or later, with the notable exception of [CentOS](http://centos.org) where Python 2.4 is still used. Also, those of you running a Linux server may still be running an old but still supported OS - for example the [Ubuntu](http://www.ubuntu.com/) 6.06 LTS (Dapper Drake) server edition is maintained until June 2011, and comes with Python 2.4.

If you would be negatively affected by Biopython dropping support for Python 2.4, please let us know as soon as possible, ideally via the [mailing list](http://biopython.org/wiki/Mailing_lists).

Thank you.
