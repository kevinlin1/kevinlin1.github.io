---
layout: post
title: Mindstorms
excerpt: >
  A review of Papert's seminal work in modern context, 38 years later.
---

*This is a first draft and very rough around the edges.*

At 21 years young, it seems like I'm slowly but surely catching up to
*Mindstorms*.

> In my vision, space-age objects, in the form of small computers, will cross
> these cultural barriers to enter the private worlds of children everywhere.
> They will do so not as mere physical objects. This book is about how
> computers can be carriers of powerful ideas and of the seeds of cultural
> change, how they can help people form new relationships with knowledge that
> cut across the traditional lines separating humanities from sciences and
> knowledge of the self from both of these. It is about using computers to
> challenge current beliefs about who can understand what and at what age. It
> is about using computers to question standard assumptions in developmental
> psychology and in the psychology of aptitudes and attitudes. It is about
> whether personal computers and the cultures in which they are used will
> continue to be the creatures of "engineers" alone or whether we can construct
> intellectual environments in which people who today think of themselves as
> "humanists" will feel part of, not alienated from, the process of
> constructing computational cultures.

*Mindstorms* touches on such a broad base of ideas about the nature of learning
and the nature of personal experience and the social psychology intertwining
the two. If you aren't familiar with the work, here are a few readers who touch
on the key arguments of the work.

* [Mindstorms: what did Papert argue and what does it mean for learning and
  education? (Andy Ko)][andy]
* [Mindstorms: Children, Computers, and Powerful Ideas (Tom Kersten)][tom]

[andy]: https://medium.com/bits-and-behavior/mindstorms-what-did-papert-argue-and-what-does-it-mean-for-learning-and-education-c8324b58aca4
[tom]: https://tomkersten.com/book-reports/mindstorms/

----------

Piagetian *constructivism* is a central idea of *Mindstorms*, whereby knowledge
is constructed from an exploratory process, an active learning-by-doing where
the system is understood through observation and interaction with the system.

It's an idea that's been a deeply-rooted philosophy of the EECS department here
at UC Berkeley. We challenge students to solve new, never-before-seen problems
by applying and recombining their existing ideas in creative ways.

In CS 61A, students are first introduced to the Python programming language.
There are many formal ways to define what Python is and what it isn't, but I've
always thought of it best as a playground governed by its own physics. We can
ask the Python interpreter questions to learn more about its behavior. The
rules of the Python playground are relatively simple to learn, but limitless in
the ways they can be combined.

CS 61A asks students, given a system governed by these basic principles, these
simple *atoms*, so to speak, how can we combine them into *molecules* and
compose larger programs and systems? What are the general structures and
patterns that can be used to achieve this?

Yet the Python playground is quite different from the Logo playground in its
scope, execution, and context. There's a tension and hesitancy I've always felt
in the air around the nature of learning. As we students grow older, the stakes
grow greater too: learning cannot be done in and of itself. Getting stuck isn't
something that is just a matter of inconsequential play because there are
external measures and standards of proficiency, rates at which we are forced to
grow, or face a socioeconomic natural selection. In spite of the fact that we
know that a grade point can't define us, that numeric, well-distributed measure
still has a demonstrably powerful impact towards the opportunities afforded to
students. Whether you'll have a shot at graduate school and academia, whether
you'll have the opportunity to do research with your professor, whether your
resume lands on the upper half or bottom half of the stack (although [not as
much anymore][nace]), or even whether you think of yourself as a "[computer
scientist][lscs]", is all determined in large part by grade.

[nace]: http://www.naceweb.org/about-us/press/2017/the-key-attributes-employers-seek-on-students-resumes/
[lscs]: https://eecs.berkeley.edu/academics/undergraduate/cs-ba

I can't help but be reminded of the things I've heard about CS 10. Programming
in Scratch, a visual programming language, is often looked down upon by
students who haven't tried it. What might be more unfortunate is that, amongst
students who have taken CS 10, feedback on how useful it's been in later
courses has been tepid at best, perhaps because there isn't a one-to-one
mapping from topic X to topic Y, entirely discounting the importance of
[network effects][]. Maybe it has to do with UC Berkeley culture, but there's a
seriousness toward making progress that I think cannot be understated, and its
impact is not always for the better.

[network effects]: http://www.tandfonline.com/doi/abs/10.1076/csed.12.1.141.8211

Worse yet, it impacts students disproportionately. On a student forum,
Professor Sahai [once wrote][sahai],

> The student who was firing on all cylinders and only then able to hit high
> marks in high school --- the pain that awaits them here makes me shudder at
> times. It isn't the party line, but I have to say it out of compassion for
> students: I think that this university doesn't always support all the
> high-striving students that it admits. And that isn't fair. If we take
> someone on striving, we should have supportive paths for people who are
> striving. But we largely don't. So students make heroic efforts. And maybe
> that grows their character and makes them better people. But there is a
> pretty wide stream of tears that flows through Strawberry Creek into the Bay.

To be fair, Anant also points out that,

> We in EECS support students pretty well. It is not clear other departments
> here do as much as we do. But as I said before, all of our support is
> predicated on students being able to put in the time. We currently have no
> real mechanisms to support students who are simply hitting their maximum
> waking hours limit.

[sahai]: https://www.reddit.com/r/berkeley/comments/24x0d9/professor_anant_sahai_as_a_berkeley_undergraduate/chbmywn/

There's no shortage of services we offer to students, but the question is no
longer one of, "Are we reaching students?" but instead, "Are we reaching *the
students we need to reach*?" There exist students in the bottom of an [uncanny
valley][]: too far along to turn back yet not far enough to make it past the
glass ceiling. It maddens, depresses, pains me that all this progress we've
made is built over 'Strawberry Creek'.

[uncanny valley]: http://tvtropes.org/pmwiki/pmwiki.php/Main/UncannyValley

It's a sobering realtiy we live in today. But it's one that we're working hard
to change. I don't want to make it sound like we haven't achieved anything, or
that we're not doing everything within our power to make things *better*, but
this is the enemy we're facing today. The EECS Department has done a tremedous
job, but we're still a long way to our destination.

In [*Why Structure and Interpretation of Computer Programs matters*][sicp],
Brian Harvey writes,

> In my experience, relatively few students appreciate how much they're
> learning in my course while they're in it.

[sicp]: https://people.eecs.berkeley.edu/~bh/sicp.html

We all leave CS 61A, SICP, *Mindstorms*, or whatever it is, with [different
feelings][wangg]. I can't say I agree with George here, but I think this
feeling of uncertainty is a real feeling shared by many students. What's the
point of learning all this?  Is this real programming? Why should *I* put my
life in your hands? That's the kind of weight that comes with being an
educator. We create a vast world of possibility, a playground built on basic
principles and containing several challenges along the way not just because we
want to watch students suffer but precisely because we can't help but want to
share that feeling of failure, re-learning, and perseverance that comes from
attaining knowledge through personal experience. There are some feelings that
can't be told or taught; they can only be experienced. And these are the ideas
in *Mindstorms* that resonate most strongly with me.

[wangg]: https://news.ycombinator.com/item?id=4787137

Through all of this, there's still more we can learn from *Mindstorms*. "[A]
world in which there were hundreds of powerful representations spanning all
kinds of knowledge, carefully crafted by researchers and educators as
personally meaningful, powerful representations serving as entry points into
everything humanity has learned." (Andy Ko)

We're all part of different worlds of possibility crafted by others, thrown
into the darkness, forced to learn, and we come out of it with a greater
appreciation of the world and a new perspective on life. One role of an
educator, then, might be to be a guiding light, a source of inspiration, hope,
physical, living, breathing proof of what can be achieved.

> The LOGO teacher will answer questions, provide help if asked, and sometimes
> sit down next to a student and say: “Let me show you something.” What is
> shown is not dictated by a set syllabus. Sometimes it is something the
> student can use for an immediate project. Sometimes it is something that the
> teacher has recently learned and thinks the student would enjoy. Sometimes
> the teacher is simply acting spontaneously as people do in all unstructured
> social situations when they are excited about what they are doing.

So let there be light.
