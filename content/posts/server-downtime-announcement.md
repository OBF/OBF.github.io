---
author: dag
category:
  - biodas
  - biojava
  - biomoby
  - bioperl
  - biopython
  - general
  - obda-/-biosql
date: "2003-08-30T21:07:42+00:00"
guid: http://news.open-bio.org/news/?p=111
summary: |-
  Hi Everyone,

  Apologies for the mass cross-posting but this email is about server and IP changes that will affect all of our projects and servers.

  Simply put -- Wyeth, the company that provides us with our hosting and wonderful T3 connection to the internet is cutting their internet connection circuits over from one ISP to a different Tier 1 internet backbone.
title: Server downtime announcement
url: /2003/08/30/server-downtime-announcement/

---
Hi Everyone,

Apologies for the mass cross-posting but this email is about server and IP changes that will affect all of our projects and servers.

Simply put -- Wyeth, the company that provides us with our hosting and wonderful T3 connection to the internet is cutting their internet connection circuits over from one ISP to a different Tier 1 internet backbone.

Technically the changeover will be swift as the circuit and new routers/firewalls are already in place. Should be a matter of bringing down the old gear and lighting up the new stuff.

The backbone change will have a significant affect on us though -- all of our server IP addresses will change.

The change is scheduled for the evening (EST/EDT timezone) of September 2nd 2003. I'll be onsite at Wyeth in the datacenter as the change occurs so that I can bring down our servers and plug in the new IP addresses.

The really nice thing is that all of our primary and secondary DNS nameservers are hosted at places other than Wyeth. This means that we can almost instantly be pushing out the new correct IP addresses for all of our open-bio.org, biojava.org etc. domain names.

If I can get my act together during the day on Tuesday I'll start seeding our DNS servers with shorter TTL values which will speed up the spread of the new information.

For people with 'fresh' DNS data our servers will appear back on the internet within 30 minutes or so. For people behind nameserver caches that do not refresh all that often please expect our servers to "vanish" from the internet for a period of about 8-24 hours while the new information propagates out through the internet.

Regards,
Chris
open-bio.org
