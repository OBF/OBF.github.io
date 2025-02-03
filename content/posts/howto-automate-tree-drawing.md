---
author: stajich
category:
  - howto
date: "2007-06-15T18:01:13+00:00"
guid: http://bioperl.org/news/2007/06/15/howto-automate-tree-drawing/
title: HOWTO automate tree drawing
url: /2007/06/15/howto-automate-tree-drawing/

---
I updated the [Trees HowTo](http://bioperl.org/wiki/HOWTO:Trees#Making_Images_of_Trees) with some code demonstrating how to automatically generate postscript trees from newick or nexus tree files. This uses the `Bio::Tree::Draw::Cladogram` module that will draw Phylograms or Cladograms. With a few unix tools ( [eps2png](http://search.cpan.org/dist/eps2png/) and epstopdf \[part of [TeX](http://ctan.org/)\]) you can generate png and pdf files automatically making this an easy addition to phylogenetic pipelines that generate webpages as well as stand alone applications.
