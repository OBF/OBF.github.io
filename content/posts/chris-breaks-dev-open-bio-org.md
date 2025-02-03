---
author: dag
category:
  - general
date: "2003-02-17T07:02:56+00:00"
guid: http://news.open-bio.org/news/?p=64
title: Chris breaks dev.open-bio.org
url: /2003/02/17/chris-breaks-devopen-bioorg/

---
Urgent notice --> Primary CVS server has been relocated to pub.open-bio.org

"dev.open-bio.org" -- our primary developer server is down in Boston with a corrupt password file. Chris blames the Solaris audit subsystem for not liking root commands issued via SSH connections :)

We have moved the CVS repositories to a Linux box called "pub.open-bio.org". Developer accounts have been created **but with different passwords**. Email the OBF Sysadmin team at [root-l@open-bio.org](mailto:root-l@open-bio.org) to get your new password.

Note: This news affects developers only (ie people who have write/commit access to one or more codebase repositories). Our Anonymous CVS server ( [cvs.open-bio.org](http://cvs.open-bio.org)) is unaffected.
