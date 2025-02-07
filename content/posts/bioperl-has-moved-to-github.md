---
author: cjfields
category:
  - bioperl
  - blogroll
  - code
  - community
  - development
  - documentation
  - general
  - obf
  - obf-projects
date: "2010-05-14T04:18:33+00:00"
guid: http://news.open-bio.org/news/?p=695
title: BioPerl has moved to GitHub
url: /2010/05/14/bioperl-has-moved-to-github/

---
BioPerl has migrated to [git](http://git-scm.com/) and [GitHub](http://github.com/bioperl)!  We have also set up a mirror set of several key repositories at the great public git hosting site [repo.or.cz](http://repo.or.cz/w).

If you are a current BioPerl developer (had a previous account for direct access to our prior Subversion repository), please sign up for a GitHub account and let us know your user ID.  Also, add the extra email [![](/wp-content/uploads/2010/05/generic.jpg)](/wp-content/uploads/2010/05/generic.jpg) (where 'DEVNAME' is your **original Subversion account ID**).  This should map any previous commits from the older Subversion and CVS repository to your new GitHub account.

The following are ways everyone can download the latest code.

## Using git

Note you can replace 'bioperl-live.git' with any of the repository names (bioperl-db, bioperl-run, etc).  For BioPerl developers (GitHub collaborators) you have a choice of SSH or HTTP:

```
  git clone git@github.com:bioperl/bioperl-live.git
```

```
  git clone https://bioperl@github.com/bioperl/bioperl-live.git
```

The open read-only link (for everyone):

```
  git clone git://github.com/bioperl/bioperl-live.git
```

or using the mirror site:

```
  git clone git://repo.or.cz/bioperl-live.git
```

## Using SVN (read-only)

We will also support read-only access to GitHub with Subversion.  We may allow write support at some later point.  To use svn:

```
  svn checkout http://svn.github.com/bioperl/bioperl-live.git
```

## Direct downloads

Tagged releases can be found here:

[http://github.com/bioperl/bioperl-live/downloads](http://github.com/bioperl/bioperl-live/downloads)

The latest source code here:

[http://github.com/bioperl/bioperl-live/archives/master](http://github.com/bioperl/bioperl-live/archives/master)

## **Forking BioPerl and Pull Requests**

We intend on using git and GitHub to their fullest.  With that in mind, we encourage users to [fork](http://help.github.com/forking/) BioPerl code, make changes, commit them to your forked repository, and submit [pull requests](http://github.com/guides/pull-requests).

## Documentation

We're also in the process of updating our local developer documents for help with those who haven't used git before.  In particular, we have a [Using Git](http://www.bioperl.org/wiki/Using_Git) page, and have added [RSS feeds](http://www.bioperl.org/wiki/Tracking_Git_commits) for our repository commits.

Enjoy!

chris

**Update:** SVN version fixed, thanks to DaveMessina++ for pointing it out.
