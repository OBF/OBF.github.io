---
author: dag
category:
  - biodas
  - bioperl
date: "2003-05-24T00:04:03+00:00"
guid: http://news.open-bio.org/news/?p=93
summary: |-
  Tony writes:
  {{ double-space-with-newline }}
  I have just checked in to the Bio::Das perl beta CVS repository ("Bio-Das2")
  a collection of modules that creates a minimal DAS reference server from a
  single AGP file (or a directory of one or more files). There is also a
  sample server script in the "eg" directory.

  Briefly, the server is started using something like:

  ```
  cd ./eg
  ./agpserver --dsn ncbi31 --port 3000 --agpfile ./AGP/chr1.agp

  ```

  It can then be used by a DAS client in the normal way. It is simple (no
  frills!) and capable of serving assembly information, entry\_points, DSN
  info, features across a segment and features by ID. No other DAS commands
  are supported yet.
title: AGP-bases DAS reference server available
url: /2003/05/23/agp-bases-das-reference-server-available/

---
Tony writes:


I have just checked in to the Bio::Das perl beta CVS repository ("Bio-Das2")
a collection of modules that creates a minimal DAS reference server from a
single AGP file (or a directory of one or more files). There is also a
sample server script in the "eg" directory.

Briefly, the server is started using something like:

```
cd ./eg
./agpserver --dsn ncbi31 --port 3000 --agpfile ./AGP/chr1.agp

```

It can then be used by a DAS client in the normal way. It is simple (no
frills!) and capable of serving assembly information, entry\_points, DSN
info, features across a segment and features by ID. No other DAS commands
are supported yet.

I wrote it because our chromosome finishers needed to be able to view
assemblies as they updated their AGPs. We have a little web-based
ensembl-ish graphical viewer that displays the assembly.

The server uses either DBD::CSV (default) or Mysql for backend SQL storage.
The former so that anybody can run a server anywhere without having to be DB
savvy, the latter for better performance. It simply goes:

```
./agpserver
--dsn                  Name for this DAS datasource
--agpdir <./dirname>        Directory holding AGP file(s)
or
--agpfile         Single AGP file
--port              DAS server port (default = 9999)
--tmpdir           CSV temp. directory (default = /tmp)
[  --backend mysql          Use a mysql backend (default = csv)
--dbhost          Mysql server hostname
--dbname          Mysql database name
--username        Mysql username (needs write access)
--password    Mysql password
--dbport          Mysql server port (default =3306)
]

```

eg:

```
./agpserver --dsn ncbi31 --agpdir ./TEST --port 3000
Loading AGP file: chrX.agp
Loading AGP file: chrY.agp
Please contact me at this URL: http://hostname:3000/das/dsn/{command}

```
