---
author: stajich
category:
  - bioperl
date: "2004-12-29T21:54:47+00:00"
guid: http://news.open-bio.org/news/?p=125
summary: |-
  I just wanted to use the end of the year as a chance to reflect on what
  we've accomplished in 2004 and think about what 2005 holds for Bioperl.
  [List Message](http://portal.open-bio.org/pipermail/bioperl-l/2004-December/017736.html)
title: Bioperl 2005 Summary
url: /2004/12/29/bioperl-2005-summary/

---
I just wanted to use the end of the year as a chance to reflect on what
we've accomplished in 2004 and think about what 2005 holds for Bioperl.
[List Message](http://portal.open-bio.org/pipermail/bioperl-l/2004-December/017736.html)

What happened in 2004?
First of all, this year has been really has been productive at a level
perhaps only appreciated by the folks who read the bioperl-guts-l list
which lists the CVS commits. New modules, bugfixes and code
improvements have been steadily making their way into the codebase.
Not only has there been lots of traffic, but more people are
contributing code and fixes.

We have also seen increased contributions to the HOWTOs which we hope
will be an effective place to explain how to use sets of modules to
complete a particular task. We are continually working to improve the
documentation. This is a balance between a developer trying to get
something accomplished for their own research and wanting other people
to use their code (and not wanting to field lots of emails about a
particular module). Open source software written solely by
volunteers suffers from a reward system which values code over
documentation and writing tutorials. We welcome ideas on changes which
would help this and are currently thinking about ways to reward the
productive documenters as well as coders.

We had a chance to have a 5 day Bootcamp in June thanks to Sylvain
Foisy, the University of Montreal and the Quebec Bioinformatics Network
(BioneQ). We hope to do another one of these in 2006. If there is a
general interest in more widespread Bioperl tutorials please forward
them to myself or the bioperl list and we can consider how something
like this could be organized in conjunction with a conference or
meeting.

How popular is Bioperl?
The 2002 paper has 60+ citations according to Web of Science and we're
seeing use in a broader context than just sequence analysis. At least
one published paper about modules which were already part of the
codebase has appeared suggesting software availability and
collaboration can happen prior to publication. The website has been
consistently gets around 300,000 hits per month which isn't bad
considering that the content doesn't change very much and this is just
a site for one toolkit for specific aspect of science. The bioperl-l
mailing list has seen an average 341 mails per month (not correcting
for spam) which has seen a lot of questions answered and ideas hashed
out.

How can you help out?
I want to use this chance to also appeal to those who use Bioperl and
have been sitting on your hands waiting to jump in. It is a
collaborative project that only works if new people jump in an
contribute ideas and manpower. We've had many examples of people who
have just jumped on board the project, fixed some bugs, contributed a
module and went on their merry way. We've also had other people who
have jumped in, contributed code, and found themselves fully engaged in
the project and its internal workings almost immediately. Not to wax
poetic, but it was about 5 years ago that fresh out of college, I
started reading the mailing list, read Steve Chervitz's email plea for
people to ["ask not what Bioperl can do for you, ask what you can do for Bioperl"](http://bioperl.org/pipermail/bioperl-l/1999-December/003354.html) and
just jumped right in. I can only hope to influence some more folks who
might have wanted to contribute but were waiting for the invitation.
Well come on over, we'd love to have you taking part.

As for some specifics.
\- Parsing of Species information out from the ORGANISM lines in
SwissProt, GenBank, and EMBL is pretty spotty and could take some work.
\- Some more parsers for formats that people have asked for - a Spidey
parser (NCBI's mRNA -> genomic alignment tool)
\- Work on the Structure modules for dealing with protein structure
data
\- Integrate new applications into bioperl-run and further cleanup the
existing modules so they are more consistent
\- Volunteer to be the next release master.

What does the future hold for Bioperl?
We expect to have a 1.5 release of bioperl in 1st quarter of 2005 -
this is the domain of Aaron Mackey who agreed to be the release master
(who has his hands full right now, but I'm sure will ask for help when
he needs it). This should incorporate many new modules and bug fixes
but be compatible with the 1.4 API as well. Details on the schedule
for 1.5 sometime after the holidays.

The future depends entirely on who steps up to work on the project next
year. In 2005, I am resolving to limit myself from the front guard of
mailing list question answering. This is in part finish my PhD
research and focus on building more specific tools to support my
research questions, but also it is time for other people to contribute
and share the spotlight and be a know-it-all. Bioperl is very much a
labor of love and it is an integral part of the tools I use in my own
work so I expect to focus more directly on those things I need in the
coming year and help out where I can.

My hope is that some of the new folks who have stepped up to contribute
will help by continuing the course we have set to have high quality
releases, a full test suite, POD documentation for every module, and
overall documentation for using modules in HOWTOs and tutorials. If
there are new or unexplored areas the project should consider I hope
that you will speak up and suggest them.

There is discussion underfoot that a new Bioperl object model may be
born. This has been called Bioperl2 and Bioperl-NG. The idea is it
would try and create a leaner and cleaner code base which is does
things like event-based parsing, autogenerated code for things like
getters/setters, and could do things faster and easier than we are
currently. Generally there is a lot of legacy code and legacy design
in Bioperl and it would be beneficial to have a project that was free
of these constraints. At the same time there is an expectation that a
project like this would also need to achieve something more than what
the current bioperl API cannot do so it incumbent on the new project to
have goals that are higher than what Bioperl can do.

Thank you
I'd like to finally thank some people who have done a lot this year.
Of course I'm not going to remember to name everyone, but I just wanted
to highlight some folks who have endeavored not only get the toolkit to
do what they want, but also to help out other people get started with
it.

The people who have kept the project going. These are usual suspects
how have labored to do the dirty grunt work cleaning up boring bugs,
adding documentation, preparing a release, keeping the servers going,
etc. They also code too, but wanted to highlight that they have really
been critical to keeping the project going by doing the things that
most people don't want to bother with.
Brian Osborne
Aaron Mackey
Chris Dagdigian
Kyle Jenson (mailing list and site searching at
[http://search.open-bio.org](http://search.open-bio.org))

Some usual suspects who have been helping maintain their modules and
generally being Bioperl knowledgeable on the list:
Scott Cain
Steve Chervitz
Allen Day
Donald Jackson
Stefan Kirov
Hilmar Lapp
Josh Lauricha
Heikki Lehvaslaiho
Chris Mungall
Jurgen Plentinckx
Lincon Stein

There are new several people who have taken up the slack as those
before them have drifted onto other commitments. (metaphoric slack of
course, not trying to accuse anyone of being a 'slacker'). Thanks for
jumping in, fixing bugs, running tests, giving feedback, and just
getting involved. It is really encouraging when the project can be a
2-way street and not just a one way flow information going out from a
few people who post answers to the list.
Richard Adams
Sean Davis
Rob Edwards
Nathan Haigh
Marc Logghe
Barry Moore
Remo Sanges
James Thompson
Koen van der Drift (Bioperl available via fink on OS X)

Thanks also to Peter van Heusden and Electric Genetics which are
undertaking a code audit of Bioperl and should have many helpful
feedback points for us.

I've probably forgotten some people, please post a followup if I have
neglected someone as I would like you to be recognized for your work
since we don't give out a whole lot else right now.

A safe and prosperous New Year to you all.

Jason Stajich on behalf of the Bioperl core developers.
