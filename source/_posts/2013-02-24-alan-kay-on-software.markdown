---
layout: post
title: "Alan Kay on Software"
date: 2013-02-24 01:26
comments: true
categories: [software, oop, messaging, smalltalk, lisp, ruby, dart]
---

If you haven't heard of [Alan Kay](http://en.wikipedia.org/wiki/Alan_Kay) you will have likley have heard one 
of his many [famous quotes](http://en.wikiquote.org/wiki/Alan_Kay), the most popular, likely his 1971 gem:

> The best way to predict the future is to invent it.

But for the unfamiliar, Alan has one of the most illustrious careers in computer science who's been awarded 
both a Kyoto Prize and a Turing award for his work on Object Orientated Programming.
He is one of the pioneers of Personal Computing, the Graphical User Interface, Object Orientated Programming and the 
inventor of [Smalltalk](http://en.wikipedia.org/wiki/Smalltalk) - one of the most influential languages of all time.

Much of [the](http://www.mprove.de/diplom/referencesKay.html) 
[writing](http://www.viewpointsresearch.org/html/writings.php) of 
[Alan Kay](http://en.wikipedia.org/wiki/Alan_Kay) holds a insightful read into how the 
[power of context (pdf)](http://www.vpri.org/pdf/m2004001_power.pdf) impacts learning and goes on to provide a glimpse 
of the incredible innovation he was surrounded with during his time working on
[ARPA](http://en.wikipedia.org/wiki/Advanced_Research_Projects_Agency) and at 
[Xerox PARC](http://en.wikipedia.org/wiki/PARC_(company)) whose creative works have formed much of personal computing 
and programming as we know it today.

## On Software Engineering

What's interesting is that Alan believes 
[The Computer Revolution Hasn't Happened Yet (pdf)](http://www.viewpointsresearch.org/pdf/m2007007a_revolution.pdf)
and that software engineering is progressing inversely to Moore's Law which sees hardware capacity increasing each 
year whilst software becoming un-necessarily bloated potentially 
> caused by weak and difficult-to-scale ideas and tools, laziness, lack of knowledge, etc.

Improving the current state of software development was the motivation behind the 
[STEPS Toward The Reinvention of Programming (pdf)](http://www.vpri.org/pdf/tr2007008_steps.pdf) research project 
which aims at achieving a "Moore’s Law" Leap in Expressiveness by reducing
> the amount of code needed to make systems by a factor of 100, 1000, 10,000, or more.

His enlightening 2011 talk on 
[Programming and Scaling (video)](http://www.tele-task.de/de/archive/lecture/overview/5819/) 
re-iterates on this, suggests software engineering has stalled and is becoming a lost science, which has become like
a garbage dumping ground where no one is able to comprehend the 100M LOC's used to create Vista and Word which should 
only be a fraction of their size. He gives the Internet and TCP/IP, LISP Interpeters, 
[Nile (Math DSL for Vector Graphics) and OMeta (OO PEG)](http://www.vpri.org/pdf/rn2010001_programm.pdf) 
as examples of elegant software with profound impact and minimal code-bases.

This got me curious on whether he had further insights on what we could improve with the current state of software 
development and if there was something missing from our current languages and tools. 

## On Object Orientated Programming

My first point of research was to find out his thinking behind his original 
[vision for Object Orientated Programming](http://www.purl.org/stefan_ram/pub/doc_kay_oop_en) which were influenced
by his Micro Biologist: 

> I thought of objects being like biological cells and/or individual computers on a network, 
> only able to communicate with messages

and Mathematics backgrounds:

> My math background made me realize that each object could haveseveral algebras associated with it, 
> and there could be families of these, and that these would be very very useful.

Who after studying Lisp was heavily influenced by it's extreme late-binding and powerful meta capabilities:

> The second phase of this was to finally understand LISP and then using this understanding to make much nicer and 
> smaller and more powerful and more late bound understructures. 

and from that point on became a strong advocate for dynamic languages for 
[the future of software engineering (pdf)](http://squab.no-ip.com/collab/uploads/61/IsSoftwareEngineeringAnOxymoron.pdf):

> Until real software engineering is developed, the next best practice is to develop with a dynamic system that 
> has extreme late binding in all aspects.

primarily because they are more easily able to be changed:

> Late binding allows ideas learned late in project development to be reformulated into the project with 
> exponentially less effort than traditional early binding systems (C, C++, Java, etc.)

with the potential for applying incremental on-the-fly changes and faster iteration times:

> One key idea is to keep the system running while testing and especially while making changes. Even major changes 
> should be incremental and take no more than a fraction of a second to effect.

Surprisingly his thoughts behind OOP were limited to only this narrow scope:

> OOP to me means only messaging, local retention and protection and hiding of state-process, 
> and extreme late-binding of all things. It can be done in Smalltalk and in LISP. 
> There are possibly other systems in which this is possible, but I'm not aware of them.

Which is [not like we know it today](http://lists.squeakfoundation.org/pipermail/squeak-dev/1998-October/017019.html):

>  I'm sorry that I long ago coined the term "objects" for this topic because it gets many people to focus on the 
lesser idea.

The big missing piece not embraced by mainstream typed OO languages today is:

> The big idea is "messaging"

He advocates focus should instead be on messaging and the loose-coupling and interactions of modules rather
than their internal object composition:

> The key in making great and growable systems is much more to design how its modules communicate rather than 
> what their internal properties andbehaviors should be.

And finds [static type systems too crippling](http://queue.acm.org/detail.cfm?id=1039523):

> I'm not against types, but I don't know of any type systems that aren't a complete pain, 
> so I still like dynamic typing.

Other than Smalltalk and LISP, other popular languages embracing Smalltalk's message-passing and late-binding include: 
[Objective-C](http://en.wikipedia.org/wiki/Objective-C), 
[Ruby](http://en.wikipedia.org/wiki/Ruby_(programming_language)) and more recently 
Google's [Dart](http://en.wikipedia.org/wiki/Dart_(programming_language)). 

## On LISP

Something that's continually re-iterated in his papers and interviews is 
[his high-regard of LISP](http://www.openp2p.com/pub/a/p2p/2003/04/03/alan_kay.html) which he considers to be the:
> greatest single programming language ever designed

Which [he thinks all comp-sci grads should learn](http://www.windley.com/archives/2006/02/alan_kay_is_com.shtml):

> Most people who graduate with CS degrees don’t understand the significance of Lisp. 
> Lisp is the most important idea in computer science.

Sadly this wasn't me either - but since learning new programming paradigms and exploring different views are great 
ways to improve developer skills, I set out to learn me some LISP!

In my next post I explore the history and beauty of LISP, unlock its secrets and explain why it's still one of the 
most powerful and easiest programming languages to learn today!

*****

I wanted to end this post talking about the kind of man Alan is, as I had originally expected a man with such a 
innovative and distinguished career to be driven by the purity of Science and the pursuit of knowledge itself. 

He has instead spent a significant part of his career (dating as far back as 1968, when he met Seymour Papert 
the Author of Logo - a language optimized for educational use) looking at how best to use technology to empower 
children and how computers could help them learn by allowing them to experiment and simulate real world models).
His goal was to think of [children as thinking beings in their own right](http://www.donhopkins.com/drupal/node/140)
> rather than as "defective adults who have to be fixed by education"

In this goal he envisaged the [Dynabook](http://en.wikipedia.org/wiki/Dynabook) concept in 1968 and later 
published the concept in a 1972 paper titled 
[A personal computer for children of all ages](http://www.mprove.de/diplom/gui/kay72.html) whilst he was still 
working for Xerox Palo Alto Research Center. This was the project that drove both the creation of the graphical user 
interface and the development of Smalltalk in as early as 1972.

In 1995 he went on to create [Etoys computing environment](http://en.wikipedia.org/wiki/Etoys_(programming_language))
a media rich authoring environment where kids can create and tweak models of real-life objects. 

In 2001 he setup the Viewpoints Research Institute, a nonprofit public benefit organization incorporated in 2001 
to improve "powerful ideas education" for the world's children, 

In 2006-2007, Etoys was used by the [One Laptop per Child (OLPC)](http://en.wikipedia.org/wiki/One_Laptop_per_Child) 
project, on their OLPC XO-1 educational machine which is now preinstalled on all of the XO-1 laptops.

It was nice to see that one of the most innovative era's in computing history was a by-product in the pursuit to improve 
children education.
