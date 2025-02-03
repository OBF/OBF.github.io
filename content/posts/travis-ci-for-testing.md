---
author: peterc
category:
  - bioperl
  - biopython
  - bioruby
  - blogroll
  - code
  - community
  - development
  - obf
  - obf-projects
date: "2012-07-30T13:24:09+00:00"
guid: http://news.open-bio.org/news/?p=949
title: Travis-CI for Testing
url: /2012/07/30/travis-ci-for-testing/

---
Earlier this year [BioRuby](http://bioruby.org) and then [Biopython](http://biopython.org) and [BioPerl](http://bioperl.org) started using [Travis-CI.org](http://travis-ci.org), a hosted continuous integration service for the open source community, to run their unit tests automatically whenever their [GitHub](http://github.com) repositories are updated:

- [![BioRuby on Travis-CI.org](https://secure.travis-ci.org/bioruby/bioruby.png?branch=master)](http://travis-ci.org/bioruby/bioruby/)[BioRuby](http://travis-ci.org/bioruby/bioruby/)
- [![Biopython on Travis-CI.org](https://secure.travis-ci.org/biopython/biopython.png?branch=master)](http://travis-ci.org/biopython/biopython/)[Biopython](http://travis-ci.org/biopython/biopython/)
- [![BioPerl on Travis-CI.org](https://secure.travis-ci.org/bioperl/bioperl-live.png?branch=master)](http://travis-ci.org/bioperl/bioperl-live/)[BioPerl](http://travis-ci.org/bioperl/bioperl-live/)

The BioRuby team are also using Travis-CI for automated testing of their new 'plugin' ecosystem, BioRuby Gems, or [BioGems](http://www.biogems.info/).

Travis-CI gives us continuous testing, but for the moment only covers [one operating system](http://about.travis-ci.org/docs/user/ci-environment/) (currently 32 bit Ubuntu Linux using Virtual Machines). This automated testing is therefore complementary to our existing [OBF BuildBot server](http://testing.open-bio.org/) which aims to run nightly tests on volunteer developer machines setup to cover a broad range of operating systems and configurations.

However, Travis-CI are working on a new feature - [automatic testing of pull requests](http://about.travis-ci.org/blog/announcing-pull-request-support/), currently only available on a donation basis - which the OBF was happy to support.

What this means is that when a contributor has some code ready for integration, they can issue a [GitHub pull request](https://help.github.com/articles/using-pull-requests/), and then Travis-CI will automatically run the unit tests with those proposed changes. This is something that currently the core-developers would normally do manually as part of evaluating proposed changes, so having this happen automatically should be a big help.

We're excited about making more use of Travis-CI for other [OBF projects](/wiki/Projects). Thus far we've been really impressed with Travis-CI.
