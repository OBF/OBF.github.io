---
author: brad
category:
  - bosc/ismb
date: "2003-06-28T09:26:53+00:00"
guid: http://news.open-bio.org/news/?p=102
summary: If you are not lucky enough to be here in wonderfully beautiful Brisbane with beaches next to the river and where every man and woman is a perfect physical specimen, then you can read all about BOSC colored through my mind. Enjoy.
title: They let me into Australia, and this is what I saw
url: /2003/06/28/they-let-me-into-australia-and-this-is-what-i-saw/

---
If you are not lucky enough to be here in wonderfully beautiful Brisbane with beaches next to the river and where every man and woman is a perfect physical specimen, then you can read all about BOSC colored through my mind. Enjoy.

Where the hell am I? I distinctly heard someone refer to me as mate and I was
supposed to be heading to Australia, so I'm thinking that's where I might be.
After three thousand straight hours of airports and planes and ticket counters
where bored [airline workers](http://samolets.com/aviakompanii/) are informing you that you won't reach your
destination until three days after your expected date and offer you a 10
dollar food and beverage coupons for your trouble, it's hard to grasp reality.
And yes, of course I spent that 10 dollars on beer. What the hell else would I
want to buy in the airport? Okay, Bloody Mary's, but I only had 10 dollars so
you gotta make it stretch at those airline prices.


But it's okay. Now it's another morning, another day. Well, maybe it's a
new day. Or maybe it's the last day. Or damn, it could be two days ahead
or three days behind or Christmas or next year's New Year's Eve wooo
everyone let's celebrate the beginning of a new millennium. Woo!
Man, I am totally messed up.


So let me tell you something you should not do. You should not travel across
the United States and then across the world (up and down) in a mad marathon
trip that takes approximately 48 hours of flight delays and being left over in
airports and sitting on plains with old ladies next to you telling you their
life stories and, man, you would have thought she'd have noticed I fell asleep
a half hour ago. Another Fosters please, kind flight attendant. But, yes, you
should not make this kind of trip, then go straight to a conference, try and
run a little meeting of Biopython, take a quick shower, eat a Kabob, start
drinking tasty Australia brews named VB interspersed with Tequila shots, sing
a karaoke song in the worst possible drunken manner at the best Friday night
Karaoke in all of Brisbane according to native Brisbaneans I chatted with,
then wander home completely lost throughout half of Brisbane without a map or
any idea where you are going being assaulted by random threatening Brisbaneans
who happen to up in the middle of the night and then stumbling across people
smoking hookah's right in the middle of the sidewalk whoah where was that bar
I gotta get back there. Do not do this. I did this. It was a mistake. I am in
Australia. And I am completely mad.


It is with this state of mind that I bring you a report for Australia on BOSC.
Good god, this is not an official report sponsored by any reasonable person.
What is it then? It's the kind of rambling I can manage and
it's how BOSC looks through my eyes and do not look too carefully or
scrutinize too closely lest you feel it is your civic duty to have me locked
up immediately as a threat to myself and others. Come on, friends, I am
completely harmless. And this is what I've seen so far in the land down under
at the number one meeting in the entire world of open-source biology folks.

**Python and Systems Biology -- Michiel de Hoon**  

Cool graphics with python. So let's say we've got one hundred million
expression data and we want to make a gene regulatory network from them. To
put it simply, you have information about how genes express and would like to
tie them together in an understandable way. This is the wide and wonderful
world of Systems Biology. And that's where we are today. This involves delving
into the head-splitting mania that is differential equations, and I'm taking
it for granted that there are some pretty smart mathematically inclined folks
are doing things correctly. You can too, as they are all implemented for your
use in Python. As always, open-source is helping you not think; more beer
time. I can steal that phrase this year since Jason isn't here this year. Ha.
Back to the talk -- another thing you might want to do with your gene
expression data is try and predict the regulatory transcription factors causing the
expression patterns. I'm certainly fond of the belief that cis and trans
factors affecting genes are nearly as important as the gene and protein
sequences; so it fills the dorky scientific part of me with delight to think
about understanding and combining these types of factors into analyses. And
all in Python. Always Python. Sweet. Of course, also sweet open-source since
you can get the code and documentation and tutorials about how to get started
programming with Python. We want to help you help yourself.

**Eukaryotic Linear Motifs and Disorder -- Rune Linding**  

This one day I'm walking along, minding my own business, whistling gently the
tune to my favorite Frank Sinatra song, and I run into this protein. Bam,
right outta nowhere. Some of the time you meet a new protein and it's wearing
a Hello My Name Is (my name is, my name is) tag and you are all set and you
can give it a heide-ho and be on your way. But most of the time you meet this
protein and have zero idea what exactly it is called, or what it does. There
are lots of ways to learn how exactly to meet this protein, but what we are
talking about here is learning about the protein by learning it's peptide
motifs. So yeah, peptide motifs are these short linear stretches of protein
sequence which are conserved. They often serve as binding sites for other
proteins. So, an alternative method to learn about proteins is to discover
these regions within your unknown protein, and use these regions to make
predictions about the function of your protein. That's the idea, as my fuzzy
brain can understand it. In addition to this approach, you can also use a more
standard approach to look for functional sites in the proteins. But I dig the
disordered small linear motifs so I rambled on about that the most. Sue me.
There is a nice database to search and classify proteins using these methods,
which is what this talk is all about. As with all good things it's developed
in Python using Biopython. Bonus.

**Sort of like close to Lectin Domains -- Alex Zelensky**  

This domain completely rules. It has more then 2000 references in GenPept and
tons of ligands and groups and types all over vertebrates. So, we have got to
sort this thing out. I completely sympathize with this type of analysis as a
common question a nice laboratory scientist might come up with it -- hey, this
domain seems really cool, can I look at how it works over the world of all the
sequences. You think -- no worries, I'll download a couple of these bad boys
from NCBI, do a little phylogenetic tree (using of course the most appropriate
method for my question (scientific-type insertion sponsored by the Foundation
to Impress Brad's PhD committee and let him graduate and pass all his exams))
and then go to lunch and slug back a couple of martinis. Of course, when you
actually get into it you find that this family you just happened to be
interested in spans every single organism ever sequenced and you realize that
your martini plans with famous supermodels might have to be put on hold for a
year and a half. So this is exactly the problem we are getting into here and
the solution in this case, which makes me really hope that next time I am
interested in a family of proteins I will be interested in this domain, was to
develop an on-line database of these motifs completely sorted out. Beautiful,
MySQL, BioPerl. Life is good and I'm gonna make that lunch date; give Claudia
a call to let her know.

**Nice popular terms like Web Services -- Martin Senger**  

If you ever accidentally forget to uncheck one of those "send me as many mails
as possible" boxes while filling out a form to download Java from the good
folks at Sun, then you will be like me and find your work mailbox completely
filled every day with magazines of complete rubbish called things like "System
Administrator's Weekly." These magazines suck hard. They are killing so many
trees. To the person out there that is sending me these magazines -- please
stop, I never read them. I don't even look at them. I just let them pile up
until they reach a level so high that it is declared a national hazard and I
have to throw them away. My point, however, is that if you glance at the cover
of any of these millions of magazines you will see the words Web Services. You
will see these words over and over and over and over again. We love Web
Services. It will save the world. So what exactly is it. XML, SOAP, web
protocols. Sending data between distributed places using standard
interoperable protocols and specifications. This will likely not go away
anytime soon, so it's a good thing to read at least a page about it so if
someone mentions it -- say, between body shots on a stripper at a local sleazy
dive bar -- you will be able to make a reasonable comment about it. Either
"web services' rulz" or "web services' suck" normally works. Choose your side.
But, I'm distracted. The point is that if you need to get data in the future,
you will likely find that more and more of it will be available through web
services. This is the case in bioinformatics, and the EBI and EMBL folks are
jumping on the bandwagon. An excellent example is OpenBQS -- in short terms
you can get all of MEDLINE through web services. Sweet.
I just want to end this with one point -- Web Services are like high school
sex. I had trouble concentrating on the rest of the talk once I got that
thought in my head. I blame it all on the cheerleaders packing out my Memphis
to LAX flight of hell.
