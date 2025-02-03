---
author: stajich
category:
  - development
date: "2006-03-24T00:28:26+00:00"
guid: http://bioperl.org/news/2006/03/23/developer-accounts-re-issued/
title: Developer accounts re-issued
url: /2006/03/23/developer-accounts-re-issued/

---
We are moving developer repository to a new server which will require you to get a new developer account.
To fix your local repository you should be able to run this on your local repository:

```
 $ find bioperl -name 'Root' | xargs perl -i.backup -p -e 's/pub.open/dev.open/'

```

or just check out a clean version.

Note that before (and sometime ON) the 25th of March anything that is committed to the dev machine CVS repository will likely get wiped out so it is best to either hold off commits on the 25th or keep copies of stuff around.

If you are a developer and did NOT get an email from Chris Dagdigian about server stuff you need to email the helpdesk with your existing login to pub.open-bio.org at [support-AT-open-bio.org](mailto:support-AT-open-bio.org).
