---
layout: post
title: On GPS Syndrome
excerpt: >-
    The code is never the focal point.
---

I often see students suffer from **[GPS Syndrome][]**, a term coined by [Kristin Stephens-Martinez](https://users.cs.duke.edu/~ksm/) from her experiences as a UC Berkeley introductory computer science teaching assistant.

[GPS Syndrome]: https://ksm-cs.blogspot.com/2019/10/gps-syndrome.html

> When a teacher provides scaffolding to a student, but does not fade it appropriately over time, leaving it there for too long. This results in a student that cannot function without the scaffolding.
>
> I call it GPS syndrome because it's similar to when I have driven to a place many times, but still need the GPS to help me get there every time. I cannot actually get to the place without it.
>
> The same idea applies, but it is when the student cannot get to the answer on their own because they have only learned how to do it with help and prompting from the teacher.

Typically, GPS Syndrome occurs in large-scale office hours when there are many assistants, many students, and an online office hours queue to coordinate help requests and helpers. Helpers are conditioned by certain sociopsychological influences to continue perptuating the GPS Syndrome in spite of its potential to harm students in the long-run.

The norms and expectations of office hours enable this practice to continue. The use of online office hours queue and a large number of assistants further reinforces the purpose of office hours as a streamlined and commoditized service, one in which help is rendered by means of brief one-on-one tutorial sessions. The online office hours queue models students as `User` objects and students' learning needs as `Ticket` objects that helpers resolve in first-come, first-served order. Furthermore, helpers teach the same way that they were taught; to do otherwise would be uncomfortable and foreign.

Curiously, both experienced and inexperienced instructors exhibit these behaviors but through different symptoms. While inexperienced instructors typically provide more direct guidance, experienced instructors may incorporate other teaching methodology such as the Socratic Method. However, Socratic questioning can sometimes turn into a vehicle for direct instruction rather than giving students an opportunity to seriously consider the question in its entirety.

Consider the following hypothetical scenario.

> A student walks into office hours and signs up on the online office hours queue. They have a question about recursion, and want help solving their homework problem. You're up to help them resolve their question. To humanize the process, you introduce yourself to them, and also learn their name. (Surprisingly, in almost all instances I've observed, helpers don't think to do this.)
>
> The student starts by saying, "I've written the recursive call, but I don't know why it's not giving the right answer."
>
> You fall back onto your usual starter question to buy more time: "Can you explain what you've done so far?" As the student explains their approach to solving the problem, you're interrogating the code in your mind to look for flaws in their approach or places where their description does not match up with what the code actually does.
>
> Ah, you find the issue. You stay quiet and nod to show that you're following along, all the while formulating your questions to ask the student in order to get them on the right track.
>
> Then, you rattle off your questions. Some questions are difficult for the student to answer because they don't know the bug, and because they haven't thought about all of the things you've thought about. You adapt by asking more directed or specific questions to drill down into the misconception. Socratic questions continue to be asked until the student gets it and figures out what they need to change.
>
> Oh, but they have a bug in their fix, so you stick around to ask a few more questions to probe at the true source of the problem. This goes on for a while.
>
> Finally, after about 25 minutes of back-and-forth questioning and clarification, the bug has been fixed all without directly stating a single thing.

The problem with this form of help is that it still induces GPS Syndrome, but in a more roundabout way. While Socratic questioning helped the student gain a better idea of the entire line of reasoning involved in drilling down to the bug, they're not in any better position to ask those questions on their own.

In the literature, this kind of help-seeking would be categorized as executive rather than instrumental because it is focused on the product rather than the process. It's a common way students get answers from teachers. This kind of help is not necessarily bad, especially because some bugs involve details or assumptions about the programming environment that the student couldn't have known about. But for the majority of problems that involve students stuck due to higher-level problems with their approach, this pedagogy can lead to GPS Syndrome.

At some level, every student's programming question has to do with a bug: the misalignment between how the programmer expects the program to behave and the program's true behavior. But the process by which we show students how to diagnose the bug is where pedagogy comes into play.

My working hypothesis is that this instantiation of GPS Syndrome arises from discussing the problem at too low of an abstraction level. When the instructor asks the student to explain what they've done so far, this entails direct discussion of the code, the product, rather than the process. Kristin describes a few suggestions in the [GPS Syndrome][] document for addressing the issue, including searching online, understanding the test cases, understanding the error message. In each case, the code is never the focal point.

A strategy I find useful is to discuss the different examples that motivated the student's approach to solving the problem. What are the examples the student has considered? What are the holes in those examples? The most basic program that can be written to solve a problem can simply take any input in the domain of the function and pass it into a massive switch statement that directly returns the expected output. What methodology is being used to reduce or simplify the problem and capture its regularities? Does it account for the entire range of possible inputs?

If the student needs additional help, one thing helpers can do is suggest smaller, analogous problems, and describe the solution process for the analogous problems. Or, breakdown the analogous problem and show how it behaves and its connection to the problem at hand.

Some of these questions may require asking even higher level questions about what actually is the expected behavior of the program, and identify patterns in the output to figure out the source of the issue.

A useful heuristic for determining how much a help session is geared toward directly discussing code is in the artifacts produced from the help session. One of sufficient (but not necessary) conditions for GPS Syndrome is a help session that fails to produce any artifacts: there are no diagrams drawn on whiteboards, there are no external visualizations, and no space for planning
the fix; the student often won't even look away from their screen.
