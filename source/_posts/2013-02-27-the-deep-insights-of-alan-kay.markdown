---
layout: post
title: "The Deep Insights of Alan Kay"
date: 2013-02-27 10:41
comments: false
categories: [software, oop, messaging, smalltalk, lisp, ruby, dart]
---

If you haven't heard of [Alan Kay](http://en.wikipedia.org/wiki/Alan_Kay) you'll likley have heard one of his many 
[famous quotes](http://en.wikiquote.org/wiki/Alan_Kay), the most popular, likely his 1971 gem:

> The best way to predict the future is to invent it.

But for the unfamiliar, Alan has one of the most illustrious careers in computer science who's been awarded both a 
Kyoto Prize and a Turing award for his work on Object Orientated Programming. 
He's also one of the pioneers of Personal Computing, the Graphical User Interface, Object Orientated Programming and the 
inventor of [Smalltalk](http://en.wikipedia.org/wiki/Smalltalk) - one of the most influential languages of all time.

Much of [the](http://www.mprove.de/diplom/referencesKay.html) 
[writing](http://www.viewpointsresearch.org/html/writings.php) of 
[Alan Kay](http://en.wikipedia.org/wiki/Alan_Kay) holds an insightful read into how the 
[power of context (pdf)](http://www.vpri.org/pdf/m2004001_power.pdf) where he recalls the one-of-a-kind environment at 
<a href="http://en.wikipedia.org/wiki/PARC_(company)">Xerox PARC</a> and 
[ARPA](http://en.wikipedia.org/wiki/Advanced_Research_Projects_Agency) which were orientated around 
"visions rather than goals" and "funded people, not projects" which as a result had attracted brilliant minds together 
cultivating different view points essential for progress where he considers:

> Point of view is worth 80 IQ points

His thoughts when reflecting back on that time:

> The ARPA/PARC history shows that a combination of vision, a modest amount of funding, with a felicitous context 
> and process can almost magically give rise to new technologies that not only amplify civilization, but also produce 
> tremendous wealth for the society. 

And that they did, which saw through the creation of the 
[impressive array of technologies invented at PARC](http://www.parc.com/about/) 
which were the foundations for much of personal computing and programming as we know it today, including:

  - Laser Printers
  - Object Orientated Programming / Smalltalk
  - Personal Computers
  - Ethernet / Distributed Computing
  - GUI / Mouse / WYSIWYG

Whilst [ARPA](http://en.wikipedia.org/wiki/DARPA) was responsible for the [ARPANET](http://en.wikipedia.org/wiki/ARPANET) 
phenomena we refer to as the Internet.

<a name="engineering"></a>
## On Software Engineering

What's interesting is that Alan still believes 
[The Computer Revolution Hasn't Happened Yet (pdf)](http://www.viewpointsresearch.org/pdf/m2007007a_revolution.pdf)
where software engineering is progressing inversely to Moore's Law which sees hardware capacity increasing each 
year whilst software becoming un-necessarily bloated, potentially 
> caused by weak and difficult-to-scale ideas and tools, laziness, lack of knowledge, etc.

This ongoing situation was eloquently 
[captured in the funny one-liner](http://www.forbes.com/2005/04/19/cz_rk_0419karlgaard.html):

> What Andy giveth, Bill taketh away

Refering to Andy Grove the then CEO of Intel and Bill Gates of Microsoft.

Improving the current state of software development was the motivation behind the 
[STEPS Toward The Reinvention of Programming (pdf)](http://www.vpri.org/pdf/tr2007008_steps.pdf) research project 
aimed at achieving a "Moore’s Law" Leap in Expressiveness by reducing
> the amount of code needed to make systems by a factor of 100, 1000, 10,000, or more.

His enlightening 2011 talk on 
[Programming and Scaling (video)](http://www.tele-task.de/de/archive/lecture/overview/5819/) 
re-iterates on this, suggests software engineering has stalled and is becoming a lost science that has not been able
to advance at the same pace as hardware or other science and engineering disciplines. That large code-bases are akin to a 
garbage dumping ground, reaching the point where no one is able to comprehend the 100M LOC's used to create 
Vista and Word, which should only be a fraction of their size. He gives the Internet and TCP/IP, LISP Interpeters, 
[Nile (Math DSL for Vector Graphics) and OMeta (OO PEG) (pdf)](http://www.vpri.org/pdf/rn2010001_programm.pdf) 
as examples of elegant software with profound impact and minimal code-bases.

Nile/OMeta DSL is used an example to show how the same functionality could be achieved to build a system from scratch 
in thousands of lines of code rather than the millions found in comparable commercial versions.

This got be curious to find out whether Alan had any further insights on what we could do to improve the current state 
of software development and if there was something missing from our current languages, approaches and tools... 

<a name="oop"></a>
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

Which didn't even require inheritance, which is 
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

Other popular languages embracing Smalltalk's message-passing and late-binding and having implemented its message-based 
[doesNotUnderstand](http://c2.com/cgi/wiki?DoesNotUnderstand) construct include: 
[forwardInvocation](https://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/ObjCRuntimeGuide/Articles/ocrtForwarding.html)
in [Objective-C](http://en.wikipedia.org/wiki/Objective-C), 
[method_missing](http://www.ruby-doc.org/docs/ProgrammingRuby/html/ref_c_object.html#Object.method_missing)
in <a href="http://en.wikipedia.org/wiki/Ruby_(programming_language)">Ruby</a> and more recently 
[noSuchMethod](http://www.dartlang.org/articles/emulating-functions/#interactions-with-nosuchmethod) in
Google's <a href="http://en.wikipedia.org/wiki/Dart_(programming_language)">Dart</a>.

### Tear it down and build something better

Alan has an interesting theory on the best way to advance Computer Science:

> I believe that the only kind of science computing can be is like the science of bridge building. Somebody has to build 
> the bridges and other people have to tear them down and make better theories, and you have to keep on building bridges.

as there are benefits to starting from scratch every few months, which saw him wanting to kill his own Smalltalk and 
starting again:

> It’s well known that I tried to kill Smalltalk in the later ’70s. There were a few years when it was the most wonderful 
> thing in the world. It answered needs in a more compact and beautiful way than anything that had been done before. But 
> time moves on. As we learned more and got more ambitious about what we wanted to do, we realized that there are all 
> kinds of things in Smalltalk that don’t scale the way they should—for instance, the reflection stuff that we had in 
> there. It was one of the first languages to really be able to see itself, but now it is known how to do all levels of 
> reflection much better—so we should implement that.

<a name="messaging"></a>
## On Messaging

As a longtime proponent of
[messaging](https://github.com/ServiceStack/ServiceStack/wiki/What-is-a-message-based-web-service%3F) for remote services, 
I've been benefiting from the inherent 
[advantages in message-based services](https://github.com/ServiceStack/ServiceStack/wiki/Advantages-of-message-based-web-services)
for some time. So I was particularly interested in 
[Alan's thoughts of the subject](http://www.computerworld.com.au/article/352182/z_programming_languages_smalltalk-80/):

> I could see that a more comprehensive basis could be made by going all the way to thinking of efficient whole 
> virtual machines communicating only by messages. This would provide scaling, be a virtual version of what my 
> research community, ARPA-IPTO was starting to do with large scale networking, and also would have some powerful 
> “algebraic” properties (like polymorphism).

He had this to say of the Internet - which he considers is "possibly the only real object-oriented system in working order":

> To me, one of the nice things about the semantics of real objects is that they are  “real computers all the way down 
> (RCATWD)” – this always retains the full ability to represent anything. 
> The old way quickly gets to two things that aren’t computers – data and procedures – and all of a sudden the ability 
> to defer optimizations and particular decisions in favour of behaviours has been lost. In other words, always having 
> real objects always retains the ability to simulate anything you want, and to send it around the planet. ... 
> And RCATWD also provides perfect protection in both directions. We can see this in the hardware model of the 
> Internet (possibly the only real object-oriented system in working order). You get language extensibility almost for 
> free by simply agreeing on conventions for the message forms. My thought in the 70s was that the Internet we were all 
> working on alongside personal computing was a really good scalable design, and that we should make a virtual internet 
> of virtual machines that could be cached by the hardware machines. It’s really too bad that this didn’t happen.
> If 'real objects' are RCATWD, then each object could be implemented using the programming language most appropriate 
> for its intrinsic nature, which would give new meaning to the phrase 'polyglot programming.' 

Where thinking of things as objects and messages would've enabled an un-precedented level of interoperability, reducing 
the un-necessary friction and allowing seamless communication between languages that would've enabled a whole new polygot 
world in which you would be free to choose the best language to implement each domain.

On RPC, and how it distorts developers mindsets in architecting and building systems:

> The people who liked objects as non-data were smaller in number, and included myself, Carl Hewitt, Dave Reed 
> and a few others -- pretty much all of this group were from the ARPA community and were involved in one way or 
> another with the design of ARPAnet->Internet in which the basic unit of computation was a whole computer. But just 
> to show how stubbornly an idea can hang on, all through the seventies and eighties, there were many people who 
> tried to get by with "Remote Procedure Call" instead of thinking about objects and messages. Sic transit gloria mundi.

[Carl Hewitt](http://en.wikipedia.org/wiki/Carl_Hewitt) being the inventor of the 
[Actor Model](http://en.wikipedia.org/wiki/Actor_model)
and [Dave Reed](http://en.wikipedia.org/wiki/David_P._Reed) who was involved in the early development of TCP/IP and 
the designer of UDP.

The last latin phrase translates to 
["Thus passes the glory of the world"](http://en.wikipedia.org/wiki/Sic_transit_gloria_mundi) 
- expressing his dismay on what might have been.

<a name="lisp"></a>
## On LISP

Something that's continually re-iterated in his papers and interviews is 
[his high-regard of LISP](http://www.openp2p.com/pub/a/p2p/2003/04/03/alan_kay.html) which he says had given him
[One of the deepest insights](http://www.vpri.org/pdf/m2004001_power.pdf) which he considers to be the:
> greatest single programming language ever designed

That all [comp-sci grads should learn](http://www.windley.com/archives/2006/02/alan_kay_is_com.shtml):

> Most people who graduate with CS degrees don’t understand the significance of Lisp. 
> Lisp is the most important idea in computer science.

Sadly we didn't have this boat at my University - but as learning new programming paradigms and exploring different views 
are great ways to improve ones developer skills, I had set out to learn some LISP!

In my next post I'll explore the history and beauty of LISP, unlock its secret magical properties Alan was mesmerized with
and explain why it's still one of the most powerful and easiest programming languages to learn today!

<br />

*****

<br />

<a name="learning"></a>
## The Unknown side of Alan Kay

I wanted to end this post talking about a little unknown nugget of what the primary motivation behind the amazing research 
teams Alan was apart of, whose pioneering efforts in advancing computer-science started about 
[40 years ago with the goal](http://www.viewpointsresearch.org/pdf/m2007007a_revolution.pdf):

>  to help children - and thus humanity - to learn and absorb “science in the large”.

Dating as far back as 1968, when he first met [Seymour Papert](http://en.wikipedia.org/wiki/Seymour_Papert) the Author 
of Logo (a language optimized for educational use).

That is, looking at how best to use technology to empower children's ability to learn. One way was showing them how
to build and simulate their own real-world models in software and letting them experiment, tinker, measure and observe 
their behavior.

One of the goals was to change how children were traditionally educated where instead of dispensing them with facts, 
to instead encourage them to observe real-world behavior for themselves and get teachers to think of 
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

In 1995 he helped create the 
<a href="http://en.wikipedia.org/wiki/Etoys_(programming_language)">Etoys computing environment</a>
a media rich authoring environment (built ontop of Squeak / Smalltalk) that was aimed at helping children learn powerful 
ideas by constructing them.

In 2001 he setup the Viewpoints Research Institute, a nonprofit public benefit organization to improve 
"powerful ideas education" for the world's children.

In 2006-2007, the [One Laptop per Child (OLPC)](http://en.wikipedia.org/wiki/One_Laptop_per_Child) project had 
[pre-installed the Squeak Etoys multimedia authoring system](http://wiki.laptop.org/images/2/28/OLPCEtoys.pdf)
on all their OLPC XO-1 educational machines.

*****

This was a fun-fact to discover that one of the most innovative era's in computing history was a by-product of the 
pursuit to improve childrens education! - makes me feel a little better about the world :)
