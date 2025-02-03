---
author: peterc
category:
  - biopython
  - code
  - development
  - obf
  - obf-projects
date: "2010-08-18T20:52:54+00:00"
guid: http://news.open-bio.org/news/?p=722
tag:
  - biopython
title: Biopython 1.55 beta released
url: /2010/08/18/biopython-1-55-beta-released/

---
We've just released a _beta_ of Biopython 1.55 for user testing.

Since [Biopython 1.54](http://news.open-bio.org/news/2010/05/biopython-release-154/) was released three months ago, we've made a good start on work for Python 3 support (via the 2to3 script), but as a side effect of this we've had to update quite a lot of the older parts of the library. Although the unit tests are all fine, there is a small but real chance that we've accidentally broken things - which is why we're doing this beta release.

In terms of new features, the most noticeable highlight is that the command line tool application wrapper classes are now executable, which should make it much easier to call external tools. This is described in the updated [documentation](http://www.biopython.org/wiki/Documentation).

Note we are phasing out support for Python 2.4. We will continue to support it for at least one further release (i.e. Biopython 1.56). This could be delayed given feedback from our users (e.g. if this proves to be a problem in combination with other libraries or a popular Linux distribution).

(At least) 10 people have contributed to this release (so far), including 5 new people:

- Andres Colubri (first contribution)
- Carlos Rios Vera (first contribution)
- Claude Paroz (first contribution)
- Eric Talevich
- Frank Kauff
- Joao Rodrigues (first contribution)
- Konstantin Okonechnikov (first contribution)
- Michiel de Hoon
- Peter Cock
- Tiago Antao

Source distributions and Windows installers are available from the [downloads page](http://www.biopython.org/wiki/Download) on the [Biopython website (biopython.org)](http://www.biopython.org).

So, please let us know what works and what doesn’t through the [mailing lists](http://biopython.org/wiki/Mailing_lists) (or [bugzilla](http://bugzilla.open-bio.org/)).
