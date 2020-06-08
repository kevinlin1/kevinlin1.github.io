---
layout: post
title: Mindstorms
excerpt: >-
  A review of Papert's seminal work in modern context, 38 years later.
---

At 21 years young, it seems like I'm slowly but surely catching up to Seymour Papert's *Mindstorms*.

> In my vision, space-age objects, in the form of small computers, will cross these cultural barriers to enter the private worlds of children everywhere. They will do so not as mere physical objects. This book is about how computers can be carriers of powerful ideas and of the seeds of cultural change, how they can help people form new relationships with knowledge that cut across the traditional lines separating humanities from sciences and knowledge of the self from both of these. It is about using computers to challenge current beliefs about who can understand what and at what age. It is about using computers to question standard assumptions in developmental psychology and in the psychology of aptitudes and attitudes. It is about whether personal computers and the cultures in which they are used will continue to be the creatures of "engineers" alone or whether we can construct intellectual environments in which people who today think of themselves as "humanists" will feel part of, not alienated from, the process of constructing computational cultures.

*Mindstorms* touches on such a broad base of ideas about the nature of learning and the nature of personal experience and the social psychology intertwining the two. If you aren't familiar with the work, here are a few readers who touch on the key arguments of the work.

* Andy Ko: [Mindstorms: what did Papert argue and what does it mean for learning and education?][andy]
* Tom Kersten: [Mindstorms: Children, Computers, and Powerful Ideas][tom]

[andy]: https://medium.com/bits-and-behavior/mindstorms-what-did-papert-argue-and-what-does-it-mean-for-learning-and-education-c8324b58aca4
[tom]: https://tomkersten.com/book-reports/mindstorms/

---

Piagetian constructivism is a central idea of *Mindstorms*, whereby knowledge is constructed from an exploratory process, an active learning-by-doing where the system is understood through observation and interaction with the system.

It's an idea that's been a deeply-rooted philosophy of the EECS Department here at UC Berkeley. We challenge students to solve new, never-before-seen problems by applying and recombining their existing ideas in creative ways.

In CS 61A, students are first introduced to the Python programming language. There are many formal ways to define what Python is and what it isn't, but I've always thought of it best as a playground governed by its own physics. We can ask the Python interpreter questions to learn more about its behavior. The rules of the Python playground are relatively simple to learn, but limitless in the ways they can be combined.

CS 61A asks students: given a system governed by these basic principles, these simple atoms, so to speak, how can we combine them into molecules and compose larger programs and systems? What are the general structures and patterns that can be used to solve problems?

It would be nice if things were as simple as this. Yet the Python playground is quite different from the Logo playground in its scope, nature, and context. There's a tension around the nature of learning in higher education. As we students grow older, the stakes grow greater too: learning is not and end in itself. The context for the playfulness and exploration which facilitate the kind of idealized, naturalistic learning are hard to come by. Getting stuck isn't something that is just a matter of inconsequential play because there are external measures and standards of proficiency, rates at which we are forced to grow, or face a socioeconomic natural selection. In spite of the fact that we know that a grade point can't define us, that numeric, well-distributed measure still has a demonstrably powerful impact towards the opportunities afforded to students. Whether you'll have a shot at graduate school and academia, whether you'll have the opportunity to do research with your professor, whether your resume lands on the upper half or bottom half of the stack (although [not as much anymore][nace]), or even whether you think of yourself as a "[computer scientist][lscs]", can be influenced in large part by a grade.

[nace]: http://www.naceweb.org/about-us/press/2017/the-key-attributes-employers-seek-on-students-resumes/
[lscs]: https://eecs.berkeley.edu/academics/undergraduate/cs-ba

Worse yet, it impacts students disproportionately. On a student forum, Professor Sahai [once wrote][sahai],

> The student who was firing on all cylinders and only then able to hit high marks in high school --- the pain that awaits them here makes me shudder at times. It isn't the party line, but I have to say it out of compassion for students: I think that this university doesn't always support all the high-striving students that it admits. And that isn't fair. If we take someone on striving, we should have supportive paths for people who are striving. But we largely don't. So students make heroic efforts. And maybe that grows their character and makes them better people. But there is a pretty wide stream of tears that flows through Strawberry Creek into the Bay.

To be fair, Anant also points out that,

> We in EECS support students pretty well. It is not clear other departments here do as much as we do. But as I said before, all of our support is predicated on students being able to put in the time. We currently have no real mechanisms to support students who are simply hitting their maximum waking hours limit.

[sahai]: https://www.reddit.com/r/berkeley/comments/24x0d9/professor_anant_sahai_as_a_berkeley_undergraduate/chbmywn/

The course community surrounding CS 61A and several other introductory CS courses is incredibly rich. The course staff is directed to reach out and check in with students. Tutors hold extra review sessions and office hours to provide additional touch points for practice. Programs such as [CS Scholars][] provide an additional space for students to build a community and support each other. Several student organizations provide additional tutoring and mentoring, available for the broad spectrum of students or tailored to particular identity or affinity groups.

[CS Scholars]: https://eecs.berkeley.edu/cs-scholars

In spite of these services we offer to students, the social dynamics at play make it difficult reach the students we really most need to reach. There are many reasons why students struggle. Many students have to contend with far more than just learning: as earners, as caretakers, as parents, as siblings, as friends, as citizens, and as humans. Students enter with different prior experiences, and as our courses grow larger and more standardized, we lose the ability to personalize the learning experience to meet students wherever they stand. How do we help students find communities that matter to them, and that can support them through times of hardship that will be inevitable in college life and beyond? And there are an untold number of students who are dismotivated and disengaged from the idea altogether due to some combination of these factors.

In [*Why Structure and Interpretation of Computer Programs matters*][sicp], Brian Harvey writes,

> In my experience, relatively few students appreciate how much they're learning in my course while they're in it.

[sicp]: https://people.eecs.berkeley.edu/~bh/sicp.html

We all leave CS 61A, SICP, *Mindstorms*, or whatever it is, with [different feelings][wangg]. This feeling of uncertainty is shared by many students. What's the point of learning all this? Is this real programming? Why should a student put their future in your hands? That's the kind of weight that comes with being an educator. We create a vast world of possibility, a playground built on basic principles. But the constraints of a course and the delivery of learning outcomes necessitates forcing functions such as assignments and assessments. Learning happnes in context, and there can be a compelling argument that today's higher education landscape is in conflict with the kinds of experiences of failure, struggle, and, ultimately, perseverance, that are so crucial to learning CS as we to teach it today.

[wangg]: https://news.ycombinator.com/item?id=4787137

What's the role of the educator through all of this? There's one quote of Papert's which feels particularly salient in spite of all the differences and all the challenges.

> The LOGO teacher will answer questions, provide help if asked, and sometimes sit down next to a student and say: "Let me show you something." What is shown is not dictated by a set syllabus. Sometimes it is something the student can use for an immediate project. Sometimes it is something that the teacher has recently learned and thinks the student would enjoy. Sometimes the teacher is simply acting spontaneously as people do in all unstructured social situations when they are excited about what they are doing.
