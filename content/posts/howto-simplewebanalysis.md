---
author: heikki
category:
  - bioperl
date: "2003-11-24T15:10:56+00:00"
guid: http://news.open-bio.org/news/?p=116
summary: |-
  Need to write a wrapper around sequence analysis service in a web form?
  Richard Adams has written
  [a HOWTO document about his\
  Bio::Tools::Analysis modules](http://cvs.bioperl.org/cgi-bin/viewcvs/viewcvs.cgi/*checkout*/bioperl-live/doc/howto/html/SimpleWebAnalysis.html?rev=1.1&cvsroot=bioperl). Available in CVS or in the latest developer release. See into BIOPERL/doc/howto/{sgml\|html\|pdf\|txt}
  for the SimpleWebAnalysis document in your favourite format.
title: 'HOWTO: SimpleWebAnalysis'
url: /2003/11/24/howto-simplewebanalysis/

---
Need to write a wrapper around sequence analysis service in a web form?
Richard Adams has written
[a HOWTO document about his\
Bio::Tools::Analysis modules](http://cvs.bioperl.org/cgi-bin/viewcvs/viewcvs.cgi/*checkout*/bioperl-live/doc/howto/html/SimpleWebAnalysis.html?rev=1.1&cvsroot=bioperl). Available in CVS or in the latest developer release. See into BIOPERL/doc/howto/{sgml\|html\|pdf\|txt}
for the SimpleWebAnalysis document in your favourite format.

Summary:

Richard has written a superclass
Bio::Tools::Analysis::SimpleAnalysisBase, which implements
Bio::SimpleAnalysisI and inherits from Bio::WebAgent. Adding a new
form-based sequence service is easily done by sub-classing,
specifying a some parameters and overriding just three methods. Nine
different services have been added to date, with more to come.
