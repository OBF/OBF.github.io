---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - howto
  - obf
  - obf-projects
date: "2012-03-02T16:56:38+00:00"
guid: http://news.open-bio.org/news/?p=889
tag:
  - biopython
title: Cross-links in GenomeDiagram
url: /2012/03/02/cross-links-in-genomediagram/

---
I've just finished writing up an example for the Biopython Tutorial of the new GenomeDiagram functionality added in [Biopython 1.59](http://news.open-bio.org/news/2012/02/biopython-1-59-released/). You can now control the start and end points of individual tracks, and you can add cross-links between regions of different tracks, as shown here:

[![GenomeDiagram with cross-links between tracks](https://news.obf.io/wp-content/uploads/2012/03/three_track_cl2-1024x724.png)](/wp/wp-content/uploads/2012/03/three_track_cl2.png)

This example attempts a simplified reproduction of Figure 6 in [Proux et al. (2002)](http://dx.doi.org/10.1128/​JB.184.21.6026-6036.2002), and shows three related phage genomes one above the other. Different classes of genes have been given different colors, while the strength of the red shaded cross-links indicates the percentage identity of the linked genes. Note there are some minor differences in the GenBank annotation we've used and the genes shown in the original figure.

Note while this example is in the [Tutorial HTML](http://biopython.org/DIST/docs/tutorial/Tutorial.html) and [PDF](http://biopython.org/DIST/docs/tutorial/Tutorial.pdf) online, it was not in the zip/tarball for Biopython 1.59, and nor was the [Proux\_et\_al\_2002\_Figure\_6.py](https://github.com/biopython/biopython/blob/master/Doc/examples/Proux_et_al_2002_Figure_6.py) script. It will be in future releases.

Another motivating use case for this functionality was to produce vector images of whole genome alignments in the style of the [Artemis Comparison Tool (ACT)](http://www.sanger.ac.uk/resources/software/act/) or [Mauve](http://asap.ahabs.wisc.edu/mauve/). We've got a poster printer in the building just crying out to be used for showing whole genome comparison of a dozen bacteria strains!
