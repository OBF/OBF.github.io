---
author: peterc
category:
  - biopython
  - blogroll
  - code
  - community
  - development
  - obf
  - obf-projects
date: "2011-08-18T17:06:47+00:00"
guid: http://news.open-bio.org/news/?p=840
tag:
  - biopython
  - development
  - news
  - open-source
  - release
  - releases
title: Biopython 1.58 released
url: /2011/08/18/biopython-1-58-released/

---
Source distributions and Windows installers for **Biopython 1.58** are available from the [downloads page](http://biopython.org/wiki/Download) on the [Biopython website](http://biopython.org) and from the [Python Package Index (PyPI)](http://pypi.python.org/pypi/biopython).

A new interface and parsers for the [PAML (Phylogenetic Analysis by Maximum Likelihood)](http://abacus.gene.ucl.ac.uk/software/paml.html) package of programs, supporting codeml, baseml and yn00 as well as a Python re-implementation of chi2 was added as the `Bio.Phylo.PAML` module.

Bio.SeqIO now includes read and write support for the [SeqXML](http://seqxml.org), a simple XML format offering basic annotation support. See [Schmitt et al (2011) in Briefings in Bioinformatics](http://dx.doi.org/10.1093/bib/bbr025).

Bio.SeqIO now includes read support for ABI files ("Sanger" capillary sequencing trace files, containing called sequence with PHRED qualities).

The Bio.AlignIO "fasta-m10" parser was updated to cope with the marker lines as used in [Bill Pearson's FASTA](http://fasta.bioch.virginia.edu/fasta_www2/fasta_list2.shtml) version 3.36, without this fix the parser would only return alignments for the first query sequence.

The Bio.AlignIO "phylip" parser and writer now treat a dot/period in the sequence as an error, in line with the official PHYLIP specification. Older verions of our code didn't do anything special with this character. Also, support for "phylip-relaxed" has been added which allows longer record names as used in [RAxML](http://wwwkramer.in.tum.de/exelixis/software.html) and [PHYML](http://www.atgc-montpellier.fr/phyml/).

Of potential interest to anyone subclassing Biopython objects, any remaining "old syle" Python classes have been switched to "new style" classes. This allows things like defining properties.

Bio.HMM's Viterbi algorithm now expects the initial probabilities explicitly.

Many thanks to the Biopython developers and community for making this release possible, especially the following contributors:

- Aaron Gallagher (first contribution)
- Bartek Wilczynski
- Bogdan T. (first contribution)
- Brandon Invergo (first contribution)
- Connor McCoy (first contribution)
- David Cain (first contribution)
- Eric Talevich
- Fábio Madeira (first contribution)
- Hongbo Zhu
- Joao Rodrigues
- Michiel de Hoon
- Peter Cock
- Thomas Schmitt (first contribution)
- Tiago Antao
- Walter Gillett
- Wibowo Arindrarto (first contribution)
