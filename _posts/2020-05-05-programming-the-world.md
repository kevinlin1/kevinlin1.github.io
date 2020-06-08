---
layout: post
title: Programming the world
excerpt: >-
  Design principles for the future of computing instruction.
redirect_from:
  - /2020/05/05/Programming-the-World/
---

[Programming is not for computers.](https://doi.org/10.1145/3328778.3366794)

Programming is a form of self-expression reflecting the human behind the machine. Programming amplifies human intent. For better or for worse, the consequences of programming are vast in the internet age. We are truly programming the world: not only in the [physical, IoT sense](https://www.youtube.com/watch?v=10cSIY20vAk), but in affecting human behavior at every scale. Decisions affecting business, government, and daily life are made on the basis of data and algorithms. How should educators serve as responsible stewards of the future?

Microethics and the study of social implications provide a framework for understanding the impacts of these decisions. Programming focusing on the end product leads to narrow definitions of software quality. The new **software engineering** investigates the crucial but often understated development process and program lifecycle in terms of its [broader effects on the world](https://medium.com/bits-and-behavior/21st-grand-challenges-for-computing-education-f5e937d57155).

The goal of an introductory computing course (even one ostensibly about programming) should not be to produce better software engineers. Better software engineers are exactly what they sound like: "better software engineers." Designing education as a pipeline is an incorrect metaphor on many levels, but it's perhaps most saliently realized in how it reproduces the bias and inequity of the status quo.

We should instead strive to construct **a new ethos for computer science through education**: designed in collaboration with students, integrating [intentional teamwork](https://www.pblworks.org/what-is-pbl), empowering students as creators of technologies, exploring the equally technical and social boundaries of computing, situating computing as [explicitly antiracist](https://wac.colostate.edu/books/perspectives/labor/), acknowledging that [learning takes time](https://www.youtube.com/watch?v=srDYfqoUQRw), and understanding the whole human experience.

## Critical programming language learning

The study of programming should involve exploring different forms of expression.

If programming in and of itself is a form of self-expression, then it is necessarily shaped by computing culture. Programming languages themselves are artifacts of this culture: features, functionality, and semantics change over time in response to programmer preferences. Organizations create their own subcultures and dialects in the form of project management processes, style guidelines, and common best practices. Programming and software engineering at large is a community of practice whose participants determine the norms of firstly [what is and is not programming](https://laras126.github.io/pls-webapp/).

But computing culture concerns more than just programming. Computing culture is situated in a broader of context of the problems that it solves. [**Computational teamwork**](https://cacm.acm.org/blogs/blog-cacm/244188-computational-thinking-or-computational-teamwork/fulltext)---intentional, integrative teamwork between both people and machines---is a critical component. How can we help students learn to "work effectively, efficiently, and ethically together" in hybrid teams of people and machines?

Coding is just one (algorithmic) way of communicating mathematical ideas. But just as important is the ability to [communicate these ideas across a variety of media and to a variety of stakeholders](https://cacm.acm.org/news/236858-when-computer-science-majors-take-improv/fulltext): not only in the form of code reviews or technical papers, but also in the form of presentations, emails, tweets, blog posts, and videos. Communication occurs across various media for various recipients with various objectives. Computer programming is not only about coding, but also about [reading, writing, and translating between languages and modalities](https://www.youtube.com/watch?v=g1ib43q3uXQ) to learn effective representations for programs.

## Emergency remote teaching

But where are we today? In the transition to emergency remote teaching, our course is doing well thanks to deep investment in both human capital (undergraduate TAs) and technical capital (infrastructure for online learning). Incidentally, many of these suggestions were just published in the context of teaching an online discrete mathematics class by [Sandy Irani and Kameryn Denaro (2020)](https://www.youtube.com/watch?v=a5PK71a7ShU).

Considering these strengths and the importance of [aligning learning objectives and learning activities](https://laurenmarg.com/2020/04/14/tips-for-teaching-online-from-a-researcher-and-instructor-of-online-learning/), we've focused on redesigning the introductory programming course around [just-in-time teaching](https://cft.vanderbilt.edu/guides-sub-pages/just-in-time-teaching-jitt/) and [pair (or group) programming](https://doi.org/10.1145/2492007.2492020). Online courses benefit from additional points of contact with student, so we adapted best practices on [Humanizing Online Teaching](https://docs.google.com/document/d/1Umj2HpNZcscye2REOZPTONfKMjevC-qBsB5NneJ-HF0/edit) and [Building Rapport to Improve Retention and Success in Online Classes](http://www.rebeccaglazier.net/wp-content/uploads/2019/11/Building-Rapport-to-Improve-Retention-and-Success-Online-Glazier-Legal-Offprint.pdf). Teaching assistants have been pivotal in reaching students. [Videos of the just-in-time teaching](https://loom.com/share/folder/435ec533843a418ea1da768c06cc2d68) are recorded based on the discussions that we have in class. (Loom has been a great help in streamlining the entire process.)

For assessment, we dropped all high-stakes exams. Our weeklong programming assignments have typically had stringent anti-collaboration policies, so they're now appropriately renamed "take-home assessments" reflecting their role in the curriculum. [Two-stage quizzes](https://doi.org/10.1145/3328778.3366938) with recovery and resubmission opportunities is an interesting but currently untested idea that will be implemented next time to reintroduce some of the assessment lost due to removing in-person exams. In the grand scheme of things, these are still mostly baby steps, but steps nonetheless, towards critical programming language learning.

As for pedagogy, I shared the following with students on the first day of class.

## [How learning works](https://courses.cs.washington.edu/courses/cse143/20sp/lessons/00/#how-learning-works)

Learning is a process that requires **deliberate practice**. There are four components to deliberate practice.

1. Sustained motivation.
2. Tasks that build on prior knowledge.
3. Immediate, personalized feedback on tasks.
4. Repetition of all of the above.

Each week in the course will introduce 2 or 3 **lessons**. Each lesson is designed around deliberate practice. You can expect each week in the course to roughly follow this schedule (time distribution in parentheses).

**Before-class introduction (3 hours)**. Prepare your brain to maximize in-class learning by completing the lesson introduction before class. Optionally, watch the lecture video for additional context.

**Lecture meetings (3 hours)**. Engage with your neighbors and the class on the ideas. Clarify questions from the lesson introduction. Seek help and seek to help others. Go beyond getting the correct answer.

**Quiz section meetings (2 hours)**. Check your understanding applying the ideas in more complex situations. Master the lesson by working with TAs and peers.

All lessons will be completed in [ed](https://us.edstem.org/dashboard), our digital learning platform. Lecture videos and lesson content are also posted on the [course website](https://courses.cs.washington.edu/courses/cse143/20sp/).. The course website has a powerful search bar to help you find and review lesson content.

A larger **take-home assessment** will be released at the end of each week. Assessments are submitted through [Grade-It!](https://gradeit.cs.washington.edu/uwcse/) and reviewed by your quiz section TA.

**Take-home assessment (7 hours)**. Apply all of the ideas learned during the week into one big program. In addition to solving the problem (external correctness), assessments will also emphasize [programming style](https://courses.cs.washington.edu/courses/cse143/20sp/style/) (internal correctness).

### External brain

To prepare for the work we will do in lecture meetings, instead of reading quizzes, each week you will create an **external brain** to help guide you to the most important information in each lesson. Each week's external brain will be different, but they will most often involve highlighting details, synthesizing passages, and coming up with general steps for solving common programming problems.

External brains will be submitted through [Gradescope](https://www.gradescope.com/). Submit a PDF document either typed or legibly handwritten. The goal of creating an external brain is to organize information in a way that is the most helpful for your learning, so pick the format that works best for you. There's no such thing as one right way to make an external brain.

**Stop and think**: How does creating an external brain help us learn?

Each lesson contains a mix of reading, quiz questions, and coding challenges. Each of these are important opportunities for learning to occur. Make the most of your learning opportunity by reflecting critically on the following meta-questions as you work through the lesson.

1. Why are we learning this?
1. How does this new concept fit in with everything we know so far?
1. Describe this concept in your own words.
1. Summarize the code in terms of its purpose (not line-by-line).
1. Give a general template or list of steps for solving programming problems of this type.

In addition, there will be stop and think questions like this one embedded within readings. These are good questions to ask and answer in your own words. Collaborate with other students to improve your external brain during each lesson.

## [Learning online](https://courses.cs.washington.edu/courses/cse143/20sp/lessons/00/#learning-online)

We've taken special care to design the course such that all of the work can be done on your own time. However, personalized feedback is a key component of deliberate practice, so we'll still hold online class sessions using [UW Zoom Video Conferencing](https://itconnect.uw.edu/connect/phones/conferencing/zoom-video-conferencing/).

Online classes share the same norms as in-person classes. Participate from a quiet space where you can listen and speak. If you participate from a more public space, be sure you won't be disturbed by others while there. When talking to others, participate with your camera (if you have one) turned on using horizontal (not vertical) video.

### Tips for success

The university has a page on [Tips for Success at the UW](https://webster.uaa.washington.edu/asp/website/study-skills/tips-for-success-at-the-university-of-washington/). Here are a few highlights that will be particularly important for online learning.

**Maintain a regular schedule**. Use a weekly planner or calendar to maintain a regular schedule. Set alarms and reminders before class meeting times. Build in routines such as getting out of bed and dressing for the day (even if you're not going outside).

**Take care of your body, mind, and soul**. Exercise regularly, sleep 6--8 hours every night, and eat well. Studying online can be isolating, so keep up with friends and family as much as possible. Take advantage of opportunities to study with other students using video chat if possible.

**Do not work on your bed**. Humans make spatial associations, so it's especially beneficial to set up a separate space that is dedicated only to study and work. Get oxygen flowing by maintaining a [natural posture](https://thewholeu.uw.edu/2016/07/01/natural-posture/) and incorporating movement such as walking.
