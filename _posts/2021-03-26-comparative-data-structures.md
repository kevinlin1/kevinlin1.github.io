---
layout: post
title: Comparative data structures
excerpt: >-
  Designing autograder-free programming assignments for rightful presence.
---

Autograders are a valuable tool for providing automated, immediate feedback to students as they work on programming assignments. They were a cornerstone of [my thesis on teaching CS at scale]({% link _posts/2019-05-28-a-berkeley-view-of-teaching-cs-at-scale.md %}), and every course I've taught has used autograders extensively.

Autograders provide unique affordances that [shape students' programming problem-solving process]({% link _posts/2019-08-29-youre-spamming-the-autograder.md %}). Autograder design not only affects how students solve problems, but also explicitly defines [what kinds of conversations and ideas are valued in the course]({% link _posts/2020-12-22-implementation-of-mastery-grading-toward-rightful-presence.md %}). Autograders focus student attention toward the end programming product. This can be desirable when programming in and of itself is the end goal. But programming alone does not necessarily help students develop a broader range of skills and competencies. Autograders can support students by providing feedback, but they also risk overemphasizing to students the centrality of programming especially when students' ideas about computing are shaped by their experiences in autograder-driven introductory courses.

When it came to designing [Data Structures and Algorithms](https://courses.cs.washington.edu/courses/cse373/21wi/), I deliberately removed autograders from the course. What I really want students to take away from the course is not the struggle of solving the programming assignments---they've already taken introductory programming---but rather 3 bigger-picture learning objectives.

1. Design data structures and algorithms by implementing and maintaining invariants.
1. Analyze the runtime and design values of data structures and algorithms.
1. Critique the application of data structures and algorithms toward complex problems.

None of these learning objectives require programming. Some faculty who are more oriented toward computational complexity theory have taught this course without any programming assignments in the past. But students also desire programming to make the work feel more authentic and situated---perhaps a consequence of our introductory courses. **How do we design a Data Structures and Algorithms course that is not dependent on autograder infrastructure---that engages students in programming activity in service of the learning objectives---and makes space for the rightful presence of more critical and justice-oriented understandings of computing?**

**Comparative data structures** is a pedagogy for the data structures and algorithms curriculum that reframes programming less as a problem-solving activity and more as a design, analysis, and critique activity. Each standardized project in the course contained 3 phases corresponding to the learning objectives.

1. [DNA Indexing](https://courses.cs.washington.edu/courses/cse373/21wi/dna-indexing/)
1. [Content Moderation](https://courses.cs.washington.edu/courses/cse373/21wi/content-moderation/)
1. [Image Processing](https://courses.cs.washington.edu/courses/cse373/21wi/image-processing/)

The **Design** phase emphasizes the idea that programming is not just about solving a problem, but also about choosing between different approaches to solving a problem. For each project, students implement the same interface 4 different ways by applying different data structures and algorithms. For example, an `Autocomplete` interface can be defined using sequential search, binary search, a balanced search tree, or a trie. Testing their implementations is done by checking the implementations against each other. Simpler algorithm designs such as sequential search can be used to verify the correctness of more complex implementations.

The **Analysis** phase asks students to consider the trade-offs between and around what they've built. Given that all the data structures implement the same interface, which implementations are faster than others? We can answer this using either asymptotic analysis or experimental analysis. This approach also raises some important questions for [affordance analysis]({% link _posts/2021-01-05-do-abstractions-have-politics.md %}): data structures and algorithms relate to real-world problems through the ways in which software engineers apply interfaces to simplify and abstract complexity during problem modeling. The interface defines expected behavior no matter which data structure or algorithm implementation we choose to use.

The **Critique** phase extends the dialogue started during affordance analysis and connects it to real-world outcomes. I want students to learn how the design of interfaces shapes the ethical values of a system. In presenting the phases in this order, we emphasize a view of the problem by abstraction level beginning from specific implementation details to generalizable interfaces and finally to broader social outcomes. This makes much more explicit the role that programmers have as the engineers of our social futures.
