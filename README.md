---
title: README
---

This is an attempt to automatically convert a Mediawiki XML export
from http://www.open-bio.org into markdown (using pandoc) as a git
repository to be hosted using GitHub Pages (rendered using Jekyll).
https://help.github.com/articles/using-jekyll-with-pages/

The conversion is via a Python script (calling pandoc and git), see:
https://github.com/peterjc/mediawiki_to_git_md

I'm using a manually compiled table mapping MediaWiki usernames
to GitHub accounts - if I have mis-identified you, please email
me during this testing period and I'll remove the false mapping.
I failed to match about 80 accounts on the wiki (half single
contributions, the rest up to 5 edits).

This site ought to be viewable via https://OBF.github.io/
and this page as *html* at https://OBF.github.io/README.html
and https://github.com/OBF/OBF.github.io/blob/master/README.md
in the original source *markdown* view on GitHub.

Branches: GitHub pages will automatically show the ``master`` branch
on https://OBF.github.io/ which I am therefore using for live
testing of the automated imports. This means I will regularly
re-write git history with replacement ``master`` branches.
Each time I will return to the ``pre_auto_import`` branch.
