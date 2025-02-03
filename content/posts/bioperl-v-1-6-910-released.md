---
author: cjfields
category:
  - bioperl
  - code
  - development
  - obf-projects
date: "2013-09-08T03:48:25+00:00"
guid: http://news.open-bio.org/news/?p=1054
title: BioPerl v.1.6.910 released
url: /2013/09/07/bioperl-v-1-6-910-released/

---
_**UPDATE:**_

As a bit of time has passed since we originally intended to make a new release, I forgot that (in that time period) Carnë Draug had released a split-out version of Bio::Biblio [to CPAN this past March](https://metacpan.org/module/Bio::Biblio).

Unfortunately that release (v1.7) appears to have version collisions with this one (v.1.6.910); therefore I'm packaging a new point release ( **v1.6.920**) that removes Bio::Biblio to prevent this.  That has now been uploaded to CPAN and should be available shortly.

**_ORIGINAL POST:_**

All,

I would like to announce that BioPerl v. 1.6.910 has been released to CPAN and should be showing up imminently.  This is primarily a bug fix release.  Two key items of note:

1. Beyond minor fixes to address problems on other distributions, this will be the last of the BioPerl 1.6 series.  We will be repackaging code into separate repositories and likewise releasing them as separate distributions on CPAN during the next (1.7.x) releases.
1. Two distributions have already been split out:

- Bio::FeatureIO has been moved into a separate distribution.  The code for Bio::FeatureIO is undergoing revision and will be released at a future point.  If you need access to it, it is available [on GitHub](https://github.com/bioperl/Bio-FeatureIO).
- Bio::DB::EUtilities and it's related modules have also been into a separate distribution and are now available on CPAN.  I will be updating the release on that code as well.

The first 1.7 release is scheduled for sometime in **late fall-early winter**, with the primary focus (as mentioned above) being repackaging of core code.

Thanks all!

chris
