---
layout: post
title: Comparative data structures
excerpt: >-
  Designing autograder-free programming assignments for data structures.
---

Autograders are a valuable tool for providing automated, immediate feedback to students as they work on programming assignments. Autograders represented one cornerstone of my thesis, [*A Berkeley View of Teaching CS at Scale*]({% link _posts/2019-05-28-a-berkeley-view-of-teaching-cs-at-scale.md %}). But I also wanted to consider exploring the antithesis. What would a large-enrollment computing course feel like without autograding infrastructure?

Autograders provide unique affordances that influence students' programming problem-solving process. The design of the autograding infrastructure can even [elicit memorable emotional responses]({% link _posts/2019-08-29-youre-spamming-the-autograder.md %}). Autograders may even function as surrogate instructors when we consider the role of personalized feedback in deliberate practice. This outcome likely occurs in our very large courses, but can also occur in smaller courses too when students work on a program "together" with their autograder. But, most importantly, autograders focus student attention toward the programming product---the artifact constructed as a result of programming.

Sometimes, we want students to focus on the programming product when programming in and of itself is the end goal. But if we want to develop a broader range of students' computing skills, turning attention away from programming might help, especially when our introductory courses conflate programming with computer science. This conflation has important consequences for how students perceive programming skill as it relates to their computing disciplinary identity. Autograders can certainly support students by providing feedback, but they also risk overemphasizing to students the centrality of programming.

When it came to designing [Data Structures and Algorithms](https://courses.cs.washington.edu/courses/cse373/21wi/), I deliberately removed autograders from the course. What I really want students to take away from the course is not the ups and downs that students experienced through solving the programming assignments, but rather 3 bigger-picture learning objectives.

1. Design data structures and algorithms by implementing and maintaining invariants.
1. Analyze the runtime and design values of data structures and algorithms.
1. Critique the application of data structures and algorithms toward complex problems.

None of these learning objectives require programming. Some faculty who are more oriented toward computational complexity theory might even teach this course without any programming assignments at all. But students also desire programming to make the work feel more authentic and situated---perhaps a consequence of our introductory courses. Simultaneously, I also wanted to create a course that could create a space for a broader variety of student perspectives and contributions toward a more critical and justice-oriented understanding of computing.

**Comparative data structures** is a pedagogy for the data structures and algorithms curriculum that reframes programming as a design activity: a means to an end rather than end unto itself. Each standardized project in the course was divided into 3 phases corresponding to the course-level learning objectives: design, analysis, and critique.

1. [DNA Indexing](https://courses.cs.washington.edu/courses/cse373/21wi/dna-indexing/)
1. [Content Moderation](https://courses.cs.washington.edu/courses/cse373/21wi/content-moderation/)
1. [Image Processing](https://courses.cs.washington.edu/courses/cse373/21wi/image-processing/)

The **Design** phase emphasizes the idea that programming is not just about solving a problem, but also about choosing between different approaches to solving a problem. For each project, we expected students to create at least 4 approaches for solving the same problem. The key to building an autograder-free programming assignment lies in defining the approaches such that they implement the same interface. Building a hash table-optimized binary heap priority queue will be tricky---especially without an autograder---but it can be made more tractable by asking students to first build a relatively-simple unsorted array priority queue and use that implementation to verify the correctness of more complex implementation.

The **Analysis** phase asks students to consider the trade-offs between and around what they've built. Given that all of the data structures implement the same interface, which implementations are faster than others? We can answer this using either asymptotic analysis or experimental analysis. This approach also raises some important questions for affordance analysis too: if we define our implementations according to an interface, it's ultimately the interface that matters rather than the underlying implementations that we so cherish in data structures. When programmers apply this interface to solve a problem, what questions and concerns should we raise?

The **Critique** phase extends the dialogue started through affordance analysis and connects it to real-world outcomes. When tracing the path from design to analysis to critique, I want students to be able to see how the design of the interface shapes final values through the interface's affordances. In presenting the phases in this order, we also emphasize a view of the problem in its abstraction levels beginning from the most specific implementation details to the generalizable interfaces and finally to the broader social outcomes produced by the system. This makes much more explicit the role that programmers have as the engineers of social futures: the responsibility that they have not only to consider the products that they build, but even how their individual engineering decisions shape the impacts of those products.
