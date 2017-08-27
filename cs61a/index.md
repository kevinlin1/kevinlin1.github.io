---
layout: page
title: CS 61A
---

## Fall 2017

- **Lab**: 139B W 10:30-11:59 AM ([Soda][] 277)
- **Discussion**: 139C F 10:30-11:59 AM ([Soda][] 380)
- **Office Hours**: M/W 6:30-8 PM ([Cory][], [check schedule][oh])
- **[Make an appointment][calendar appointment]**
- **[Anonymous Feedback][]**
- **Email**: <kevinlin1@berkeley.edu>

### [How to Learn Computer Science](/gbo)

High-level learning techniques for how to succeed in CS 1 courses like CS 61A,
crammed into a 40-minute presentation for Golden Bear Orientation Fall 2017.

Most of the wordier advice I have to give has now been integrated with the
course website as part of a big redesign this semester so everyone can access
it more easily.

But since you're already here, let me share with you some additional insight
into the research that interests me and motivates the work I do for CS 61A.

#### Metacognition & Mental Representations

Here's a selection of recent [computing education research][cer] papers that
provide insight into the learning processes that motivate how we learn CS.

[cer]: https://faculty.washington.edu/ajko/cer

- [Computing Mentorship in a Software Boomtown: Relationships to Adolescent
Interest and Beliefs (Ko, Davis)](https://faculty.washington.edu/ajko/papers/Ko2017Mentorship.pdf)
- [Programming, Problem Solving, and Self-Awareness: Effects of Explicit
Guidance (Loksa, Ko, et al.)](http://dl.acm.org/authorize?N04874)
- [Using Tracing and Sketching to Solve Programming Problems: Replicating and
Extending an Analysis of What Students Draw (Cunningham, Blanchard, Guzdial)](https://doi.org/10.1145/3105726.3106190)

One of the most useful skills acquired in the process of learning computer
science is metacognition: an understanding of your own thought processes and,
in particular, how much you know or don't know about a concept. Experienced
programmers excel at metacognition. They still make the same mistakes just like
everyone else, and they still have to answer the question, "Why isn't it
working?" just as often as everyone else.

What sets an experienced programmer apart is their ability to pull themselves
away from the immediate frustration of a bug in the code and reconsider all the
possible options. They've learned *how to ask the right questions* to
themselves and adjust their solution bit-by-bit.

When faced with broken code, here are some of the questions I like to ask
myself.

1. *Why* is this not working? Answering this question usually requires digging
   below the surface and looking at the context of the problem, so we might
then ask,
2. *Where* is it not working *as expected*? There are two parts to this
   question that are important to answer.
    - We reframe the goal of "why" in terms of "where" which allows us to look
      critically at specific portions of the code. This reduces the range of
possibile changes down to a specific area and lets us ask even more specific
questions about our code.
    - In addition, we care why it is not working *as we expected it to*. One
      interesting observations that has been made about programming is that
there are actually no such things as bugs or programming errors in the world,
just **miscommunication**. Python executes code in a certain, predetermined
pattern but the code we write and *our* understanding of Python is often
incomplete which leads to perceived bugs. Let's try to rephrase the problem
from solving bugs to reconciling with Python because, somewhere Python and I
disagree on how to interpret the code. Where I see *this*, Python really sees
it as *that*.
3. *What would happen* if I tried changing *this* value to *that*? Now that
we've narrowed down where the problem must be, we can attempt to write a fix
and reconcile with Python. The key to **learning** and overcoming this
miscommunication in the future is not to edit code and make modifications
blindly, but to *understand and envision Python's process*. Think of it as if
you're arguing with a friend: empathize! Put yourself in their shoes! Think
like Python!

The most effective and the most natural learning happens after we've walked
through the path of **why**, **where**, and **what-if**. The key to becoming a
great programmer is to learning how to *ask and answer increasingly-specific
questions*.

----------

## Resources and Wisdom

- [CS 61A Summer 2017][su17] (my lectures are the ones marked *Video*)
    - [Recursion][]
- [Python 3 Documentation][python doc]
- [Online Python Tutor][python tutor]
- [Owen's *Words of Wisdom (?)*][owen advice]
- [Tammy's *Course Advice*][tammy advice]
- [James Maa's *A Beginner's Guide to Computer Science*][james maa advice]
    - [*Productivity Hacking Guide*][james maa productivity]
- [Philip Guo on *How To Be Effective*][philip guo advice]
- [Brian Harvey on *Why SICP matters*][bh advice]

[su17]: http://inst.eecs.berkeley.edu/~cs61a/su17/
[recursion]: https://docs.google.com/presentation/d/1IfXHf_LkgmHK5X9z5EVMovmY6b371uNlG3IzSnc7zbg/edit?usp=sharing
[python doc]: https://docs.python.org/3/
[python tutor]: http://tutor.cs61a.org/
[owen advice]: http://owenjow.xyz/cs61a/words-of-wisdom/
[tammy advice]: http://tmmydngyn.com/cs61a-resources/other/exams.html
[james maa advice]: http://www.jamesmaa.com/2013/08/26/a-beginners-guide-to-computer-science/
[james maa productivity]: http://www.jamesmaa.com/2012/12/02/james-maas-productivity-hacking-guide/
[philip guo advice]: http://www.pgbovine.net/productivity-tips.htm
[bh advice]: https://people.eecs.berkeley.edu/~bh/sicp.html

### Selected Staff Material

- [Albert's website][albert]
- [Allen's website][allen]
- [Tammy's website][tammy]
- [Vivian's website][vivian]

[albert]: http://albertwu.org/cs61a/
[allen]: http://aguo.us/cs61a/
[tammy]: http://tmmydngyn.com/cs61a/
[vivian]: http://www.vivi.sh/cs61a

[calendar appointment]: https://calendar.google.com/calendar/selfsched?sstoken=UUxUckJmcl80Vm9UfGRlZmF1bHR8NTE5N2NhNWQ2OTI3MjRkZjgzMGFhMmE0MTIxN2U1MWE
[anonymous feedback]: https://docs.google.com/forms/d/e/1FAIpQLSfucwcOEoD1VDpfHVfEUSLIgzojpwIBEjCl6IDKzgrqU_Q-qQ/viewform

[soda]: http://www.berkeley.edu/map?soda
[cory]: http://www.berkeley.edu/map/?cory
[morgan]: http://www.berkeley.edu/map?morgan
[oh]: https://cs61a.org/office-hours.html
