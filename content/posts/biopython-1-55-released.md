---
author: peterc
category:
  - biopython
  - code
  - development
  - obf
  - obf-projects
date: "2010-08-31T22:49:52+00:00"
guid: http://news.open-bio.org/news/?p=736
tag:
  - biopython
title: Biopython 1.55 released
url: /2010/08/31/biopython-1-55-released/

---
The Biopython team is proud to announce Biopython 1.55, a new stable release, about three months after our last stable release ( [Biopython 1.54](http://news.open-bio.org/news/2010/05/biopython-release-154/)) and the [beta release](http://news.open-bio.org//news/2010/08/biopython-1-55-beta-released/) earlier in August.

A lot of work has been towards Python 3 support (via the 2to3 script), but unless we broke something you shouldn't notice any changes ;)

In terms of new features, the most noticeable highlight is that the command line tool application wrapper classes are now executable, which should make it much easier to call external tools. This is described in the updated [documentation](http://www.biopython.org/wiki/Documentation).

Additionally GenBank and EMBL parsing has been sped up, the [BioSQL](http://www.biopython.org/wiki/BioSQL) classes act more like Python dictionaries, and Bio.PDB should handle model numbers and a missing element column better.

Note we are phasing out support for Python 2.4. We will continue to support it for at least one further release (i.e. Biopython 1.56). This could be delayed given feedback from our users (e.g. if this proves to be a problem in combination with other libraries or a popular Linux distribution).

(At least) 12 people have contributed to this release, including 6 new people - thank you all:

- Andres Colubri (first contribution)
- Carlos Rios Vera (first contribution)
- Claude Paroz (first contribution)
- Cymon Cox
- Eric Talevich
- Frank Kauff
- Joao Rodrigues (first contribution)
- Konstantin Okonechnikov (first contribution)
- Michiel de Hoon
- Nathan Edwards (first contribution)
- Peter Cock
- Tiago Antao

Source distributions and Windows installers are available from the [downloads page](http://www.biopython.org/wiki/Download) on the [Biopython website (biopython.org)](http://www.biopython.org).

As usual, feedback is most welcome on the [mailing lists](http://biopython.org/wiki/Mailing_lists) (or [bugzilla](http://bugzilla.open-bio.org/)).
