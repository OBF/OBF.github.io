---
author: stajich
category:
  - code
date: "2005-11-06T04:40:41+00:00"
guid: http://bioperl.open-bio.org/?p=7
summary: According to NCBI - BlastXML (and ASN.1) is the only guaranteed _always parseable_ report format that is provided by their web CGI script. Here is some code to specify how the data should be requested (and perhaps this will become the default).
title: Getting BlastXML using RemoteBlast
url: /2005/11/06/getting-blastxml-using-remoteblast/

---
According to NCBI - BlastXML (and ASN.1) is the only guaranteed _always parseable_ report format that is provided by their web CGI script. Here is some code to specify how the data should be requested (and perhaps this will become the default).

```

my $remote_blastxml = Bio::Tools::Run::RemoteBlast->new
      ('-verbose'    => $v,
       '-prog'       => $prog,
       '-data'       => $db,
       '-readmethod' => 'xml',  # this tells the parser to use  blastxml
                                                  # format for parsing
       '-expect'     => $e_val,
       );
 # this  tells NCBI to send you XML back
$remote_blastxml->retrieve_parameter('FORMAT_TYPE', 'XML');

```

See also [wiki page](http://bioperl.org/wiki/Module:Bio::Tools::Run::RemoteBlast) and [NCBI email about Remote BLAST](http://bioperl.org/wiki/NCBI_Blast_email).

-jason
