---
author: dag
category:
  - biomoby
date: "2003-02-26T21:10:31+00:00"
guid: http://news.open-bio.org/news/?p=70
summary: |-
  Date: February 24, 2003
  Author: Lincoln Stein
  Version: early

  This report concerns the messaging layer of the Moby project, that
  point at which semantic information is exchanged between the
  data consumer (i.e. the biologist) and the data provider (i.e. the
  model organism system administrator).
title: TECHNICAL REPORT ON MOBY WEB MESSAGING LAYER
url: /2003/02/26/technical-report-on-moby-web-messaging-layer/

---
Date: February 24, 2003
Author: Lincoln Stein
Version: early

This report concerns the messaging layer of the Moby project, that
point at which semantic information is exchanged between the
data consumer (i.e. the biologist) and the data provider (i.e. the
model organism system administrator).

There are a wide variety of possible messaging systems. Here are a
number of prominent ones listed in rough chronological order.

1) Custom messaging system using raw TCP/IP
2) Custom messaging system using BEEP (an IEEE applications
protocol framework)
3) ASN.1 exchange
4) Microsoft DCOM
5) REST
6) CORBA
7) XML-RPC
8) SOAP
9) .NET

For the purposes of this assessment, I ignored 1, 2, 3 and 4. I
rejected custom messaging because it is a fallback position. We
should only reinvent the wheel if we are absolutely certain that none
of the other will meet our requirements. Exchange of messages via
ASN.1 streams and Microsoft DCOM can rightly be treated as legacy
solutions that have found important places in niche applications but
are not accepted as solutions for enabling the exchange of semantic
information across administrative domains. SOAP arises from, and
supersedes, XML-RPC, and so are folded together. I will not consider
NET because its marketing literature gives me a headache. This
leaves REST, CORBA, and SOAP.

I will now consider these in chronological order.

\-\-\------------------------------------------------------------------

REST
\-\-\--

REST stands for REpresentation State Transfer, and is a term coined by
Roy Fielding in his graduate thesis to describe a style of information
architecture that had already become the de facto standard for the
World Wide Web. According to Fielding, REST is suited for scaleable
applications in which relatively large hypermedia representations of
information resources are exchanged within the "anarchic network."

Key Features:

a) Resources are identified using stable addresses, the URI.

b) Resources are never exchanged themselves. Instead representations
of resources are exchanged. A particular resource, such as a database
entry, may be represented in multiple ways, e.g. as an HTML file or a
postscript file. Resources are viewed as changing with time.

c) REST has many nouns, but very few verbs. Its verbs follow the CRUD
paradigm, and consist of PUT, GET, POST and DELETE. Its nouns are an
extensible set of hypermedia representations.

d) REST is stateless, and places the burden of maintaining session
information squarely on the client.

e) REST is close to the transport layer, and allows but does not
require applications to be concerned with performance issues
such as caching, parsing, and rendering latency.

Discussion:

Probably the most unique aspect of REST is its use of URIs to address
each resource. For example, in a DAS application, a URI can be used
to identify a particular segment of a genome:

http://my.site/das/d-melanogaster/r3.1/2R

This identifies the genome of drosophila melanogaster, assembly
release version 3.1, chromosome arm 2R. To fetch the list of features
from this region, one would issue a GET request on the following URL:

GET http://my.site/das/d-melanogaster/r3.1/2R/features

To address an individual feature named "exon00001", one refers to this

GET http://my.site/das/d-melanogaster/r3.1/2R/features/exon00001

To add a new feature to the chromosome, one issues a PUT:

PUT http://my.site/das/d-melanogaster/r3.1/2R/features/exon00002

Updates and deletes are handled similarly.

REST is elegant because it allows very generic software to be written.
For example, caching code does not have to know anything about the
contents of the data it caches, and fetching code can simply hand off
the data it receives to the appropriate helper application. However,
it is unclear to me how REST can be used to handle transformative
tasks. For example, do we transform genes into GO\_terms this way?

GET http://my.site/das/d-melanogaster/genes/notch/GO\_terms

If we want to pass parameters to the request, do we do it with a query
string?

GET http://my.site/das/d-melanogaster/genes/notch/GO\_terms?descendents=true

Who is using REST:

In one sense, everyone is. In another sense, no one. Aside from
WebDAV, there are very few "pure REST" applications out there. There
are many almost-REST services, but a variety of common practices, such
as the use of cookies, interferes with REST by confusing the semantics
of stateless information transfer operations.

DAS/1 is fairly close to a REST application, but it does some things
that are discouraged by the REST design, such as using POST to mean
GET.

Software support:

There is significant infrastructural support for REST services. It's
the web!

==================================================================

CORBA
