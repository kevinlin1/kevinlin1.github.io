---
layout: post
title: Data Structures Course Transformation
excerpt: >-
  Design principles for the intersection of theoretical and practical CS.
---

For the past 20 or more years, data structures courses have struggled with an identity crisis.

> I first taught the data structures course in 1979. The data structures we covered then--arrays, linked lists, trees, and hash tables--are those we cover now. Programming environments are much different now, though; most come with extensive class libraries that provide implementations of the standard data structures. A big question I see for CS 2 is, to what extent should we continue to focus on implementations at the expense of various other topics (described below)?

This was written by [Mike Clancy in 1997](https://users.cs.duke.edu/~ola/woduds/clancy.html). Modern computing courses grapple with the increasing diversity of fundamental programming abstractions, toeing the line between teaching the inner workings of data structures and the application of data structures. [Porter et al. (2018)](https://doi.org/10.1145/3159450.3159457) suggest the following learning goals for "Basic Data Structures".

1. Analyze runtime efficiency of algorithms related to data structure design.
1. Select appropriate abstract data types for use in a given application.
1. Compare data structure tradeoffs to select the appropriate implementation for an abstract data type.
1. Design and modify data structures capable of insertion, deletion, search, and related operations.
1. Trace through and predict the behavior of algorithms (including code) designed to implement data structure operations.
1. Identify and remedy flaws in a data structure implementation that may cause its behavior to differ from the intended design.

Data structures courses often work via case study, examining the design decisions (invariants), algorithm ideas, and complexity tradeoffs of "arrays, linked lists, trees, and hash tables". The value of a case study is in the opportunity to learn a variety of programming templates, or "reusable abstractions of programming knowledge" ([Xie et al. 2019](https://doi.org/10.1080/08993408.2019.1565235)). Data structures instructors are responsible for designing a productive sequencing of topics that minimizes misconceptions ([Lewis et al. 2019](https://doi.org/10.1017/9781108654555.028)), provides sufficient opportunities for deliberate practice and productive failure to refine [representations and solution methods](https://www.manukapur.com/productive-failure/), while developing a supportive classroom climate ([Barker et al. 2002](https://doi.org/10.1145/563340.563354)). These challenges can be abstracted into three broad areas: content design, instructional design, and classroom design.

## Data Structures

Programming can be motivating because computers can bring mathematical ideas to life. But programming is not an efficient way to learn data structures. (Programming is not necessarily the most efficient way to learn programming, either.) Programming makes process explicit but obscures it behind syntax. Data structures represent one of infinitely many possible states; programming represent generalized algorithms that operate on any such state. Data structures change; programming is static. The kinds of concepts and thinking taught through programming data structures are orthogonal to using data structures: the crux of the identity crisis.

This course inherits the approach of exploring data structures via case study, but we emphasize learning primarily through problem solving and analysis. Data structures ideas are introduced before class via short readings. Each class session is spent discussing guided questions in class that move from superficial application towards deeper reasoning about the fundamental properties of data structures and algorithms. Every class session is worksheet-centered, moving the focus away from the screen and back to the seats.

Drawing on research in equitable student-centered learning, classroom instruction emphasizes collaborative problem solving with group random call ([Knight et al., 2016](https://doi.org/10.1187/cbe.16-02-0109)). Though not fully committed to more structured pedagogies like process-oriented guided inquiry learning (POGIL), we draw inspiration from its emphasis on making problem solving process visible by setting subgoals ([Loksa et al. 2016](https://doi.org/10.1145/2858036.2858252), [Lin and DeLiema 2019](https://doi.org/10.1145/3287324.3293712)) and leveraging student inquiry as a opportunities for student-centered reflection rather than teacher-centered explanation. In this way, the time spent in class is proportional to the kinds of knowledge students are expected to produce on exams.

## Computer Programming

What kinds of perspectives and experiences do students need to succeed as programmers and more broadly as computer scientists? Values and skills are perhaps more important than the concepts that we aim to teach an introductory course.

The pedagogic challenge of developing an introductory programming course is in its emphasis on the value of programming products. Computer programming as a learning context is realistic and motivating but also highly volatile---the instructor has limited control over individual student learning experiences. Novice experiences with programming will almost invariably involve bugs because ideas do not translate perfectly to programming environments. Introductory computer programming courses often address inequities in learning experience by implementing changes along two axes.

1. Redesigning the programming environment. Computer scientists have long considered what programming language and development environment is the best for teaching an introductory programming course. There are clear applications for more humanistic programming language design, better visualizations of program state, and machine learning for feedback at scale.
2. Reframing the programming experience. If a goal of an introductory course is to integrate students into the programming community of practice, then part of the design must work with students' perspectives on computing. Teachers, as the dominant force for classroom socialization, set the norms for the community. How ideas are communicated and valued in a classroom determines the framing within which students interpret the value of their own ideas.

Fundamentally, both approaches are grounded in the idea that learning programming is about learning process. On one level, the process is the algorithm idea programmed into code. On another level, the process is the learning of how to program, similar to how one might learn to understand relationships in the sciences and produce artifacts in the arts. Among many other reasons, computer programming is challenging because **learning the process** (of how to program) often gets in the way of **learning about process** (of programs themselves). Programming is an act of self-expression; programming assignments are canvas upon which these self-expressions unfold. For better and for worse, both programming products and programming process reflect the creator.

Compounding these effects is the institutional challenge of developing an introductory programming course (especially one used in competitive admission) within the frame of fixed time and fixed learning ([Guzdial 2020](https://computinged.wordpress.com/2020/01/27/thorndike-won-dewey-lost-the-most-important-thing-to-know-about-the-us-education-system/)). Introductory courses are situated in a broader social context that requires institutional change to move away from systems that disempower students towards systems that lead to equitable outcomes. Computing may play a promising role in reimagining the way we assess and, therefore, the way we teach introductory courses in the future, such as the [Computer-based Testing Facility](http://zilles.cs.illinois.edu/cbtf.html). However, it will require humanity, not technology, to be the arbiters of such institutional change.

## Programming the World

Although computer science values processes and algorithms, the past decade has made it clear that the data are now as important as the data structures.

**Data Structures** as a title itself is a bit of misnomer: we teach the mathematical structures but rarely discuss the underlying data. Algorithms as we know them in this course are perfect: code is "beautiful", correct solutions are better than incorrect solutions, and simple algorithms better than complex ones. Without data and decision-making, data structures are mathematical implementations of abstract data types while algorithms are perfect solutions to real-world problems. Teaching data structures and algorithms as mathematical ideas is a political choice that positions computer science as morally neutral and disinterested in issues of justice.

Data structures courses paint the illusion of a pristine world, diverting attention away from the [broader challenges of computing education](https://medium.com/bits-and-behavior/21st-grand-challenges-for-computing-education-f5e937d57155) ([Knight and Pearl 2000](https://doi.org/10.1023/A:1005177227794)): content to measure the difficulty of a problem by runtime or space complexity; the quality of a piece of software by internal craftsmanship rather than external impact; the value of a software developer by individual productivity rather than collective contribution. These values define the CS majors that we graduate, the CS-intended that we don't, and everyone else who never takes a CS course because it's "not for them."

Computing curricula of the future will grapple with these political issues whether they want to or not. As it stands, our silence is making the choice for us. An alternative theory of instruction will need to address problems of inequity not only about students within (and without) the classroom, but also the values embedded in our CS education. Change will require support from stakeholders at the administrative level, department level, and the student level and explicitly acknowledge the role of computing in society as a force that can be leveraged to maintain the status quo more readily than to change the status quo.
