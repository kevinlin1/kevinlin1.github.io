---
layout: page
title: CS 61A
---

## Section 139
- **Course Website**: [cs61a.org][]
- **Lab**: Tuesdays 9:30 - 11:00 am in 330 [Soda][]
- **Discussion**: Thursdays 9:30 - 11:00 am in 540AB [Cory][]
- **Office Hours**: Mondays 3:00 - 4:00 pm in 109 [Morgan][]
- [**Schedule a meeting**][calendar appointment]
- **Email**: <kevinlin1@berkeley.edu>

### Announcements

#### October 27, 2016
- [Another one.][disc07 survey]
- [Quiz 7](quiz/quiz07.pdf) and [solutions](quiz/quiz07_sol.pdf).

#### October 13, 2016
- [This one's not very special.][disc06 survey]
- [Quiz 6](quiz/quiz06.pdf) and [solutions](quiz/quiz06_sol.pdf).

#### October 6, 2016
- [Survey.][disc05 survey]
- [Quiz 5](quiz/quiz05.pdf) and [solutions](quiz/quiz05_sol.pdf).

#### September 29, 2016
- [Survey-survey.][disc04 survey]
- Read [Andrew Huang's Guide to Orders of Growth and Function Runtime][andrew oog guide]. If you'd like more practice, check out the [Course Resources][] page!
- [Quiz 4](quiz/quiz04.pdf) and [solutions](quiz/quiz04_sol.pdf).

#### September 22, 2016
- [Survey.][disc03 survey]
- If you'd like to talk, [let's meet!][calendar appointment] If none of the times work, we can also figure out something [over email][kevinlin1@berkeley.edu].
- [Quiz 3](quiz/quiz03.pdf) and [solutions](quiz/quiz03_sol.pdf).

#### September 8, 2016
- [Yet another survey.][disc02 survey] It never ends.
- Midterm 1 on Thursday, Sept. 15. Study for the midterm using my patent-pending *Efficient Algorithm for Studying*.
  - Now is the time to use the [Course Resources][] page!
  - **Absolutely make sure to read and internalize [Jerry's midterm 1 slides][jerry mt1 slides] and [Andrew Huang's midterm 1 reminders][andrew mt1 doc].**
  - No discussion section next week: extra office hours available by [calendar appointment][]. Lab on Tuesday will be midterm review.
  - If you have a conflict, fill out the [midterm 1 conflict form][mt1 conflict form] by Sunday night.
- Tutor-led guerrilla section on Saturday, Sept. 10 from 12-3 pm in the 247 Cory.
- TA-led midterm 1 review session on Sunday, Sept. 11 from 12-3 pm in 155 Dwinelle.
- Sign up for [Computer Science Mentors group tutoring][csm scheduler].
- [Quiz 2](quiz/quiz02.pdf) and [solutions](quiz/quiz02_sol.pdf).

#### September 1, 2016
- [Survey, round 2!][disc01 survey] This time with 100% more food options!
- Read [Andrew's Environment Diagram Rules](environment-diagrams) and practice, practice, practice until you **love drawing them**. Seriously: they should become one of the most fun parts of the exam.
  - [Albert's Environment Diagrams page][albert environment diagrams] is also a fantastic resource.
  - If intuition behind order of evaluation is still a little confusing, [I have a lot of words for you](python-notional-machine). The [lecture 1 slides][cs61a.org] also have great visuals for breaking down a call expression.
- Read the **Tools** section of [James Maa's *A Beginner's Guide to Computer Science*][james maa advice].
- [Quiz 1](quiz/quiz01.pdf) and [Solutions](quiz/quiz01_sol.pdf).
- Remember the [early submission policy][early policy].

> On each project, you can earn an additional bonus point by submitting the project at least 24 hours before the deadline. In addition, if you submit at least 10 homework assignments 24 hours before the deadline, you can earn one additional bonus point for the semester.

#### August 25, 2016
- Fill out this [quick survey][disc00 survey], pretty please!
- Bookmark the [Course Resources][] page: we'll be keeping it up-to-date.
- Read these advice posts and **really, really take them to heart**.
  - [Owen's *Words of Wisdom (?)*][owen advice].
  - [Tammy's *Course Advice*][tammy advice].
  - The **Intro** to [James Maa's *A Beginner's Guide to Computer Science*][james maa advice]. (Recommended: [*Productivity Hacking Guide*][james maa productivity].)

We've got a long road ahead of us but we can make it to the finish line together! CS 61A is by no means an easy class so I encourage you to find a study partner or a group of study buddies. [*Life is better with a partner.*][syllabus]

You can always get in touch with me [over email][kevinlin1@berkeley.edu], visit my regular office hours listed above, or [meet me by appointment][calendar appointment] (email me if no time works).

**Welcome to CS 61A!**

----------

## Key Topics
- [Python Notional Machine](python-notional-machine)
- [Environment Diagram Rules by Andrew Huang](environment-diagrams)
- [Guide to Orders of Growth and Function Runtime by Andrew Huang][andrew asymptotics]
- [Environment Diagrams][albert environment diagrams], [Order of Operations][albert order of operations], and [Lists][albert lists] by Albert Wu
- Inheritance
- Scheme
- SQL

### An Efficient Algorithm for Studying
1. **Evaluate**: Complete 1 past exam in a quiet, test-taking environment to figure out where you are and which concepts are most challenging for you.
2. **Analyze**: Take some time to figure out not only what you may have missed on the exam, but why. Write it down. Was there a step that you forgot? Or is there a deeper misconception that we need to address? The idea here is that we should narrow things down and study only what we need to study.
3. **Iterate and improve**: Study. Review. Practice. Refer back to the problems that really challenged you. See if you can solve simpler problems first. Start with the most advanced material like guerrilla section worksheets and work your way down to quizzes, worksheets, and labs until you find the level of problems that you're comfortable solving. Then, work your way back up to solving more and more challenging problems. Find help through Piazza, friends, or the course staff until your proficiency increases.
4. **Recurse**: If not satisfied with your understanding of the material, go back to step 1.

#### Tackling Code-Writing Questions
1. Read the question. Read the question again. *Really* read it again. Identify the domain and range. Remember the domain and range when working with the problem later. Write it down. Write it down everywhere if it helps.
2. Study the doctests. Study them intensely. Figure out what the exam is trying to tell you about the problem: **big hints are always given away in the doctest**. Identify a pattern in the solutions! Then, spend some time figuring out a base case that fits the domain and range you identified earlier.
3. Come up with a general idea for solving the problem using the skills you've learned. Does this problem look similar to something you've seen before on the homework? Armed with your experience from homework plus the patterns in the doctest, develop a general idea of how to break down the problem.
4. Write down a rough draft of your code. It probably won't be entirely correct but, after having spent some time thinking about this incomplete solution, you'll have learned a lot about the mechanics of the problem and be much more prepared to try again!
5. Debug. Debug. Debug, debug, debug, debug until your code is flawless. The code won't be right on your first try, but that's entirely normal. **To improve our code, we just need to ask ourselves the right questions.** Imagine if I were there, right next to you. What input would break your program? Think like python: break down each expression and scrutinize it exactly the way python executes your function. You know what the output should look like, so make sure the actual result matches your expectations. If it doesn't match, where is it going wrong? Fix it, and repeat this step until the program is completely bug-free.

----------

## Resources and Links
- [Course Resources][]
- [Python 3 Documentation][python doc]
- [Online Python Tutor][python tutor]
- [Owen's *Words of Wisdom (?)*][owen advice]
- [Tammy's *Course Advice*][tammy advice]
- [James Maa's *A Beginner's Guide to Computer Science*][james maa advice]

### Selected Staff Material
- [Albert's website][albert]
- [Owen's website][owen]
- [Tammy's website][tammy]
- [Vivian's website][vivian]
- [Sumukh's website][sumukh] plus his [CS 42 book][]

### Feedback and Surveys
- [Leave feedback for me anonymously][anonymous feedback]

[kevinlin1@berkeley.edu]: mailto:kevinlin1@berkeley.edu
[cs61a.org]: http://cs61a.org
[syllabus]: http://cs61a.org/articles/about.html
[early policy]: http://cs61a.org/articles/about.html#early-policy
[cs61a piazza]: https://piazza.com/class/irwl7o7shzu70z

[calendar appointment]: https://calendar.google.com/calendar/selfsched?sstoken=UUxUckJmcl80Vm9UfGRlZmF1bHR8NTE5N2NhNWQ2OTI3MjRkZjgzMGFhMmE0MTIxN2U1MWE
[anonymous feedback]: https://docs.google.com/forms/d/e/1FAIpQLSfucwcOEoD1VDpfHVfEUSLIgzojpwIBEjCl6IDKzgrqU_Q-qQ/viewform
[disc00 survey]: https://docs.google.com/forms/d/e/1FAIpQLScqAgS-BRfBZymh7SAKuvMCkbL4jOGzfvrOyL0obbeiZxEJXQ/viewform
[disc01 survey]: https://docs.google.com/forms/d/e/1FAIpQLSfov43B3zDgSJuevM2PC0Ijz3zRs805BQLBGRj70UpfzXFF3w/viewform
[disc02 survey]: https://docs.google.com/forms/d/e/1FAIpQLSda8ZzNnMEUVcvMK6Z4wPgSIVC1XGqhjWRSPWZnMMvKTZRo-w/viewform
[disc03 survey]: https://docs.google.com/forms/d/e/1FAIpQLSez4RyhszB2gExRwvlBtkaWLVqkKtzdmLdGHw0smH6UuCVPzg/viewform
[disc04 survey]: https://docs.google.com/forms/d/e/1FAIpQLSdyLA7yZLE2VlYsXh7GJa0xtXKUoXfzja4bJ5_Pc1Ja5X4gJg/viewform
[disc05 survey]: https://docs.google.com/forms/d/e/1FAIpQLSd7TczE0OKODaiAv6xUqwFcTxptr9Ta8svcanwEF2RwkMLVJw/viewform
[disc06 survey]: https://docs.google.com/forms/d/e/1FAIpQLSeQ7i6Y3WNkROE8bqgEmbGserQ72yc6dIT6lLorPEoYUTRkQQ/viewform
[disc07 survey]: https://docs.google.com/forms/d/e/1FAIpQLSei_TRmTZfH9G8PkqeXqrkb18xoK1DtRk-tM9o_zvopEJZSKg/viewform

[lab 0]: http://cs61a.org/lab/lab00/
[mt1 conflict form]: https://docs.google.com/forms/d/e/1FAIpQLScTmByOMKJ74vcThhsONJymUedgKS9yQ-pXBPuxHWiwsKfghg/viewform

[course resources]: http://cs61a.org/articles/resources.html
[andrew asymptotics]: https://docs.google.com/document/d/1TxfKmM3MlH032hjSUh92I0kQDVcvmitTSzYObGMr8Bk/edit
[andrew oog guide]: https://docs.google.com/document/d/1TxfKmM3MlH032hjSUh92I0kQDVcvmitTSzYObGMr8Bk/edit#heading=h.ldtgx4uhox88
[albert environment diagrams]: http://albertwu.org/cs61a/notes/environments.html
[albert order of operations]: http://albertwu.org/cs61a/notes/oop.html
[albert lists]: http://albertwu.org/cs61a/notes/indexing.html
[python doc]: https://docs.python.org/3/
[python tutor]: http://tutor.cs61a.org/

[albert]: http://albertwu.org/cs61a/
[andrew mt1 doc]: https://docs.google.com/document/d/1yL0H1FYXnqjwmaqTGMkx0lGcGen5yj_deIEF9EoE9HQ/edit
[james maa advice]: http://www.jamesmaa.com/2013/08/26/a-beginners-guide-to-computer-science/
[james maa productivity]: http://www.jamesmaa.com/2012/12/02/james-maas-productivity-hacking-guide/
[jerry mt1 slides]: https://drive.google.com/file/d/0BzajjJ0GTP-CZlNsWnBJTDVqMlk/view
[owen]: http://owenjow.xyz/cs61a/
[owen advice]: http://owenjow.xyz/cs61a/words-of-wisdom/
[sumukh]: http://sumukh.me/?page=cs61a
[cs 42 book]: https://42cs.github.io/book/
[tammy]: http://tmmydngyn.com/cs61a-resources/
[tammy advice]: http://tmmydngyn.com/cs61a-resources/other/exams.html
[vivian]: http://www.vivian.tk/cs61a

[csm]: http://csmentors.berkeley.edu/
[csm scheduler]: https://csmscheduler.herokuapp.com/
[soda]: http://www.berkeley.edu/map?soda
[cory]: http://www.berkeley.edu/map/?cory
[morgan]: http://www.berkeley.edu/map?morgan
