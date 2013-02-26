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
<a href="http://en.wikipedia.org/wiki/PARC_(company)">Xerox PARC</a> 
whose creative works have formed much of personal computing and programming as we know it today.

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
re-iterates on this, suggests software engineering has stalled and is becoming a lost science that has not been able
to keep pace with the advancement in hardware or mechanical engineering. That has become like a garbage dumping ground 
which has reached a point where no one is able to comprehend the 100M LOC's used to create Vista and Word which 
should only be a fraction of their size. He gives the Internet and TCP/IP, LISP Interpeters, 
[Nile (Math DSL for Vector Graphics) and OMeta (OO PEG) (pdf)](http://www.vpri.org/pdf/rn2010001_programm.pdf) 
as examples of elegant software with profound impact and minimal code-bases.

This got me curious on whether he had further insights on what we could improve with the current state of software 
development and if there was something missing from our current languages and tools. 

## On Object Orientated Programming

My first point of research was to find out his thinking behind his original 
[vision for Object Orientated Programming](http://www.purl.org/stefan_ram/pub/doc_kay_oop_en) which were influenced
by his background as a Micro Biologist: 

> I thought of objects being like biological cells and/or individual computers on a network, 
> only able to communicate with messages

and a Mathematician:

> My math background made me realize that each object could haveseveral algebras associated with it, 
> and there could be families of these, and that these would be very very useful.

Who after studying Lisp was heavily influenced by it's extreme late-binding and powerful meta capabilities:

> The second phase of this was to finally understand LISP and then using this understanding to make much nicer and 
> smaller and more powerful and more late bound understructures. 

who from that point on became a strong advocate for dynamic languages for 
[the future of software engineering (pdf)](http://squab.no-ip.com/collab/uploads/61/IsSoftwareEngineeringAnOxymoron.pdf):

> Until real software engineering is developed, the next best practice is to develop with a dynamic system that 
> has extreme late binding in all aspects.

primarily as they are more easily able to be changed:

> Late binding allows ideas learned late in project development to be reformulated into the project with 
> exponentially less effort than traditional early binding systems (C, C++, Java, etc.)

with the potential for applying incremental on-the-fly changes and faster iteration times:

> One key idea is to keep the system running while testing and especially while making changes. Even major changes 
> should be incremental and take no more than a fraction of a second to effect.

that's currently [lacking in statically-typed languages](http://queue.acm.org/detail.cfm?id=1039523):

> If you’re using early-binding languages as most people do, rather than late-binding languages, then you really 
> start getting locked in to stuff that you’ve already done. You can’t reformulate things that easily.

Surprisingly his thoughts behind OOP were limited to only this narrow scope:

> OOP to me means only messaging, local retention and protection and hiding of state-process, 
> and extreme late-binding of all things. It can be done in Smalltalk and in LISP. 
> There are possibly other systems in which this is possible, but I'm not aware of them.

With no mention of inheritance, which is 
[not like we know it today](http://lists.squeakfoundation.org/pipermail/squeak-dev/1998-October/017019.html):

>  I'm sorry that I long ago coined the term "objects" for this topic because it gets many people to focus on the 
lesser idea.

Where the big missing piece lacking in mainstream typed OO languages today is:

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
<a href="http://en.wikipedia.org/wiki/Ruby_(programming_language)">Ruby</a> and more recently 
Google's <a href="http://en.wikipedia.org/wiki/Dart_(programming_language)">Dart</a>

## On Messaging

As a longtime proponent for the use
[messaging](https://github.com/ServiceStack/ServiceStack/wiki/What-is-a-message-based-web-service%3F) for any type
of remote service, I was already aware of the inherent 
[advantages message-based services](https://github.com/ServiceStack/ServiceStack/wiki/Advantages-of-message-based-web-services)
had. So I was very interested in 
[Alan's thoughts of the subject](http://www.computerworld.com.au/article/352182/z_programming_languages_smalltalk-80/):

> I could see that a more comprehensive basis could be made by going all the way to thinking of efficient whole 
> virtual machines communicating only by messages. This would provide scaling, be a virtual version of what my 
> research community, ARPA-IPTO was starting to do with large scale networking, and also would have some powerful 
> “algebraic” properties (like polymorphism).

On the Internet:

> To me, one of the nice things about the semantics of real objects is that they are  “real computers all the way down 
> (RCATWD)” – this always retains the full ability to represent anything. 
> The old way quickly gets to two things that aren’t computers – data and procedures – and all of a sudden the ability 
> to defer optimizations and particular decisions in favour of behaviours has been lost.  In other words, always having 
> real objects always retains the ability to simulate anything you want, and to send it around the planet. ... 
> And RCATWD also provides perfect protection in both directions. We can see this in the hardware model of the 
> Internet (possibly the only real object-oriented system in working order). You get language extensibility almost for 
> free by simply agreeing on conventions for the message forms. My thought in the 70s was that the Internet we were all 
> working on alongside personal computing was a really good scalable design, and that we should make a virtual internet 
> of virtual machines that could be cached by the hardware machines. It’s really too bad that this didn’t happen.
> If 'real objects' are RCATWD, then each object could be implemented using the programming language most appropriate 
> for its intrinsic nature, which would give new meaning to the phrase 'polyglot programming.' 

On RPC:

> The people who liked objects as non-data were smaller in number, and included myself, Carl Hewitt, Dave Reed 
> and a few others -- pretty much all of this group were from the ARPA community and were involved in one way or 
>another with the design of ARPAnet->Internet in which the basic unit of computation was a whole computer. But just 
> to show how stubbornly an idea can hang on, all through the seventies and eighties, there were many people who 
> tried to get by with "Remote Procedure Call" instead of thinking about objects and messages. Sic transit gloria mundi.


## On LISP

Something that's continually re-iterated in his papers and interviews is 
[his high-regard of LISP](http://www.openp2p.com/pub/a/p2p/2003/04/03/alan_kay.html) which he considers to be the:
> greatest single programming language ever designed

Which [he thinks all comp-sci grads should learn](http://www.windley.com/archives/2006/02/alan_kay_is_com.shtml):

> Most people who graduate with CS degrees don’t understand the significance of Lisp. 
> Lisp is the most important idea in computer science.

Sadly this wasn't me either - but since learning new programming paradigms and exploring different views are great 
ways to improve developer skills, I set out to learn some LISP!

In my next post I'll explore the history and beauty of LISP, unlock its secret magical properties that explains why 
it's still one of the most powerful and easiest programming languages to learn today!

<br />

*****

<br />

I wanted to end this post talking about a little known fact around what the primary motivation behind his teams 
pioneering work that was responsible for much of the innovations that advanced computer-science. 

Dating as far back as 1968, when he met Seymour Papert the Author of Logo (a language optimized for educational use) 
he [started his research with the goal](http://www.viewpointsresearch.org/pdf/m2007007a_revolution.pdf):

> to help children – and thus humanity – to learn and absorb “science in the large”.

that is, looking at how best to use technology to empower children's ability to learn. One way was showing them how
to build and simulate real-world models with a computer, letting them measure, experiment and observe behavior as 
they tinkered with them.

One of his goals was to change how children were educated where instead of dispensing them with facts, 
to instead encourage them to observe real-world behavior for themselves and get teaches to think of 
[children as thinking beings in their own right](http://www.donhopkins.com/drupal/node/140)
> rather than as "defective adults who have to be fixed by education"

This effective method of learning was termed 
<a href="http://en.wikipedia.org/wiki/Constructionism_(learning_theory)">Constructionist learning</a> and
defined by Papert in his 1987 Constructionism publication: 
[A New Opportunity for Elementary Science Education](http://nsf.gov/awardsearch/showAward?AWD_ID=8751190)

Alan envisaged the [Dynabook](http://en.wikipedia.org/wiki/Dynabook) concept in 1968 and later published the concept 
in a 1972 paper titled [A personal computer for children of all ages](http://www.mprove.de/diplom/gui/kay72.html). 
This was the project that drove both the creation of the graphical user interface and the development of Smalltalk 
in as early as 1972.

In 1995 he went on to create the 
<a href="http://en.wikipedia.org/wiki/Etoys_(programming_language)">Etoys computing environment</a>
a media rich authoring environment (built ontop of Squeak/Smalltalk) where kids can create and tweak models of 
real-life objects. 

In 2001 he setup the Viewpoints Research Institute, a nonprofit public benefit organization incorporated in 2001 
to improve "powerful ideas education" for the world's children, 

In 2006-2007, Etoys was used by the [One Laptop per Child (OLPC)](http://en.wikipedia.org/wiki/One_Laptop_per_Child) 
project, on their OLPC XO-1 educational machine which is now preinstalled on all of the XO-1 laptops.

This was a fun-fact to discover that one of the most innovative era's in computing history was a by-product of the 
pursuit to improve childrens education.
