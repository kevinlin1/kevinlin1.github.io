---
layout: post
title: You're spamming the autograder
excerpt: >-
  A lesson in user-testing, expectations management, and course integration.
---

> Autograders provide instant feedback on student work, but they can also harm learning if students grow dependent on autograder feedback to solve problems. The resulting autograder-driven development cycle occurs when students make minor adjustments to their code seemingly at random, submit code to the autograder, and repeat until their program passes all of the given tests. Anecdotal evidence from other instructors suggested that rate-limiting student submissions on the server-side autograder to 3 or 4 submissions per hour was an effective intervention. We hypothesized that introducing a 3-5 minute “cooldown timer” on the client-side autograder could mitigate student over-reliance on autograder feedback by requiring students to spend more time independently debugging, planning, and evaluating their changes before receiving autograder feedback. However, a lack of user-testing, expectations management, and course integration led to students and course staff alike perceiving the cooldown timer as an inconvenience more than a learning opportunity.

[Slides](https://docs.google.com/presentation/d/1WO7fxvEAZnfCv8oqTrbHjm5_a0uAkv4u8sw9bQ_mSqM/edit?usp=sharing)

## It seemed like a good idea at the time

Autograders provide instant feedback to students, clarify assignment grading, and reduce staff overhead. However, immediate access to autograders comes with an inherent risk when students, often in a rush to complete an assignment on time, switch to an autograder-driven development cycle where they make minor adjustments to their code seemingly at random, submit it to the autograder, and repeat until their program passes all of the given tests. This learning process is problematic because feedback is not taken into account as students make changes to their code and potentially resulting in GPS Syndrome.

Our autograder infrastructure consisted of two parts: a client with a small set of local tests for instant feedback, and a server with the full set of tests for final grading. The autograder client automatically logs timestamps of student work in case the student's computer is unable to post student work immediately to the server. Previous instructors for the course had positive experiences rate limiting student submissions on the server-side, allowing students to iterate as frequently as they liked on their own computers using the built-in tests, but only being able to submit graded work to the server 3 or 4 times per hour. We hypothesized that further limiting access on the client-side would reduce the tendency toward autograder-driven development.

To address this, we added a cooldown timer to the autograder client. After the student's first 2 attempts, the autograder client would read the time of the latest backup from the metadata logs and prevent the autograder from running if less than a certain amount of time had elapsed, starting with a 3 minute cooldown that increased to 5 minutes after their next successful attempt.

This change, unfortunately, did not land well. While there was no complaining on the online course forum, the most immediate pushback was from course staff. On the third day of class, the cooldown timer was reduced to 60 seconds after a negative reception on the first assignment. Along with this change, the client would now print a descriptive message for students, "You're spamming the autograder," and give a generic suggestion, "If you're stuck on `{question}`, try talking to your neighbor, asking for help, or running your code in interactive mode: `python3 -i {files}`."

As it turns out, students did not appreciate this change either. The cooldown period was quickly perceived as an annoyance rather than an opportunity for learning. WIth only a 60-second timer, the intended benefit of students planning out their changes in advance was never actually realized. Without explicit instructions on how to work with their neighbor, or how to use Python’s interactive mode, the generic suggestion fell on deaf ears. Instead, the cooldown period only prevented students from immediately fixing syntax errors, forcing them to wait an excruciating minute after correcting a typo. In order to work around the cooldown timer, staff even internally shared a clever shell command that deleted the autograder client logs before running the autograder.

All popular changes are memorialized as art, and this is [no exception][].

[no exception]: https://inst.eecs.berkeley.edu/~cs61a/su17/proj/scheme_gallery/#you-re-spamming-the-autograder

## Learning from our mistakes

Three major lessons come to mind.

### Dogfooding is good, user testing is better

Gather data. Instead of just imagining what would happen as a result of a change, actually test it before deployment. Dogfooding, where staff test their own tools, could have revealed some of the problems with the change. However, because staff workflows are different from student workflows, this might not have been sufficient to uncover all of the problems. Proper evaluation of the 60-second cooldown could have revealed that it would slow down students fixing syntax errors without necessarily discouraging autograder-driven development. Small prototypes can be developed to test the waters without committing full resources.

### Communicate changes and suggest a workflow

This change was deployed largely behind-the-scenes and without proper instructional integration. Students were not told why they were being slowed down, and the staff alongside students may have just found the cooldown time counterproductive as 60 seconds is not long enough to assist another student in the meantime. Neither staff nor students had a plan for how to use those 60 seconds, resulting in what was perceived as wasted time. The original intent for the module may have been diluted by pushback over the first three days of class.

### Be explicit about the value of learning process

We know that prompting students to try strategies like self-explanation can improve student performance, especially on cognitively demanding tasks such as debugging a program. One addition made after the end of the course was to automatically suggest a problem-solving strategy for the student to try out while they waited. Had this been implemented in the original rollout and integrated into the course messaging and learning activities, student and staff reception may have been more positive.

This result also suggests an interesting question about the appropriate time and place for formative feedback vs. summative feedback. Limits on summative feedback are perceived as an acceptable learning hurdle, while limits on formative feedback hinder students. Other ways to tackle the problem, such as [autograder test unlocking][], could be perceived as more justified by students. These indirect interventions may be even more effective than this direct intervention.

[autograder test unlocking]: https://youtu.be/polTBnMXGQI?t=2120
