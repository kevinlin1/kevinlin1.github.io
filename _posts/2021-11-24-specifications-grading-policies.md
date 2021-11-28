---
layout: post
title: Specifications grading policies
excerpt: >-
  How to get your LMS to work with your grading policies, not against them.
---

[Kristin Stephens-Martinez](https://users.cs.duke.edu/~ksm/) invited [Brett Wortzman](https://homes.cs.washington.edu/~brettwo/) and me to season 3 of the [CS-Ed Podcast](https://csedpodcast.org/), where we discussed our grading philosophies in our large, programming-focused CS1 and CS2 courses. I wanted to provide some more context about our grading policies and the surrounding infrastructures that I've designed to support them.

One way to understand a grading system is in terms of two components: (1) the grading policies and (2) the tools that are used to communicate progress during the term. Grading policies affect the tools we might want to use. When I teach a large 4-credit course with many assignments that factor into the final grade, I want tools that help students get a better sense of their progress through the course. But our tools don't need to rely on assignment grades to communicate progress: when I teach a small 1-credit seminar with no submitted assignments and participation-based grading, there are no assignment grades to rely on. Instead, I might rely on classroom observation and notetaking tools to help me identify participatory inequity and use that information to inform my pedagogy and communication.

This interface between policies and tools is a contended space, with instructors on one side designing grading policies and educational technology companies on the other side providing tools. Although every instructor has different views on grading, tools often lead us to assume specific approaches. For example, many autograding tools provide a single, summative, numeric evaluation of student submissions---simplifying multiple dimensions of quality down into a single number. Learning management systems like to maintain assignment grades as numbers, which affords calculating students' final grades using a weighted average. Student progress in these tools are represented using numbers. It's in this context that Robert Talbert reminds us the importance of [maintaining humanity in higher education in a high-tech world](https://rtalbert.org/maintaining-humanity-in-higher-education-in-a-high-tech-world/).

Specifications-based grading policies attempts to design grading to support growth mindset and build empathy between students and instructors in spite of larger university administration that use grades as a mechanism to separate students and sow distrust. Over the past couple years, I've experimented with 3 different specifications-based grading policies that wrestle with these tensions. Although none of these practices represent truly just grading policies, they are in my view a step forward from our traditional practices because they provide a foundation for enabling more creative assessment in large courses. All of these are at best imperfect solutions.

## Single-rating grading

Under single-rating grading, most assignments in the course are assigned a single rating representing the quality of the work with respect to the assignment specifications. We replaced fine-grained point-based rubrics with a 4-level **E/S/N/U** ordinal scale: Exemplary / Satisfactory / Not yet / Unassessable. This policy was used in [CSE 143 Autumn 2020](https://courses.cs.washington.edu/courses/cse143/20au/about/#grading).

**How is progress communicated?** Although we can represent this data in a learning management system as 3/2/1/0, the conversion to an interval scale implies that differences between each rating are similar when in reality they may be quite different depending on what information the rubrics intend to evaluate at each level. This system is relatively easy to adapt to single-number learning management systems because we can enter the 3/2/1/0 rating for each assignment as the grade. Final grades are calculated by exporting the grades, entering them into a spreadsheet, and then applying the specifications-based grading policy. The contribution of specifications-based grading is to not assume a weighted average of 3/2/1/0 values is the ideal way to assign grades---not only because of the interval scale conversion, but also because final grades (for the many purposes they might serve) might be better determined using a count of E/S/N/U ratings. Robert Talbert's [written a lot more about this](https://rtalbert.org/tag/mastery-grading/).

## Multiple-rating grading

Multiple-rating grading takes the idea of E/S/N/U ratings but considers that large assignments may emphasize multiple, orthogonal dimensions of quality rather than just a single dimension of quality. Assignments are given multiple E/S/N/U ratings, one for each dimension of quality. In a programming assignment, we might assign E/S/N/U for each of the following dimensions.

- **Behavior**. Does the input and output functionality of the program meet the specification?
- **Concepts**. Does the code effectively and appropriately use the Python language or libraries?
- **Quality**. Does the code meet the code quality guidelines and documentation standards?
- **Testing**. Do the unit tests ensure the correctness of the code across relevant inputs?

This policy was used in [CSE 163 Spring 2021](https://courses.cs.washington.edu/courses/cse163/21sp/#grading).

**How is progress communicated?** This is much trickier to represent in a learning management system because they often assume assignments only have a single score. One approach would be to apply the interval scale conversion and sum the result so that a single score is generated between 0 and 12, but this raises many new issues around interpretation of grades as well as the fact that this conversion is a one-way operation---we can't recover the original E/S/N/U grades for some scores like 6 because there are many ways for a student to have a scored a total of 6 "points" in this scale. An average of the score is similarly problematic.

Ultimately, we'd like to be able to communicate these ratings separately. At the University of Washington, we use the Canvas learning management system, which provides three features that help us implement multiple-rating grading. Setting up the grading system requires combining three Canvas features.

1. [Assignment grading rubrics](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-add-a-rubric-to-an-assignment/ta-p/1058). Rubrics can be attached to an assignment, which allows instructors to assign scores on each dimension.
2. [Outcomes](https://community.canvaslms.com/t5/Canvas-Basics-Guide/What-are-Outcomes/ta-p/75). Outcomes define the method for aggregating rubric scores across multiple assignments. This is used to determine cutoffs for a student who's "mastered" a dimension.
3. [Learning mastery gradebook](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-use-the-Learning-Mastery-Gradebook-to-view-outcome/ta-p/775). This opt-in feature provides an alternative view of student progress based not on the single-number grade, but rather the rubric scores accumulated across the course.

The resulting learning mastery gradebook that students see is a dashboard organizing their progress on each dimension of quality. This dashboard is particularly helpful for providing students an at-a-glance view of what assignments they might need to revise or resubmit. In this example, we have a student who's received feedback on 3 assignments (Pokemon, Primer, Startup), and we're looking at how they're doing on **Behavior** and **Concepts** for each of the 3 assignments. The headings note whether or not the student has "mastered" or "not mastered" the dimension according to how we defined mastery in the Outcomes.

![Learning mastery gradebook](/assets/images/learning-mastery-gradebook.svg)

There are some limitations with this approach. For one, there are few options to customize the "mastered" versus "not mastered" headings. Canvas offers three calculation methods for determining mastery, but all three of them are meant for standards-based grading where students are reassessed multiple times on the same concept; mastery involves a minimum threshold on the number of satisfactory evaluations. Our specifications-based grading instead uses rubrics to measure dimensions of quality in different CS concepts; mastery involves satisfactory completion of all assignments. Furthermore, in Canvas, rubrics do not replace the single-number assignment grade: an assignment is not graded until is given a single-number grade. I work around this by treating the single-number grade as a binary flag for satisfactory submissions: 0 for work that is below satisfactory on any dimension, and 1 for work that is satisfactory across all dimensions.

Getting all of this multiple-rating data into Canvas is also tricky for programming assignments that may be graded on other platforms. UW CSE courses use a learning platform called Ed. Ed supports grading programming assignments using our multiple-rating E/S/N/U scale, but it doesn't have a direct integration to send the multiple-rating scores to Canvas or implement the binary flag idea that I use. So I wrote a script to send the entire class's [multiple-rating grade data from Ed to Canvas](https://gist.github.com/kevinlin1/f3bb1bab2bab2ce65ba947e6d5040a58).

## Module completion grading

Module completion grading is a variant of single-rating grading that organizes the grading policy around modules---collections of assignments or other work in the course. Rather than emphasizing each assignment's grade as an individual unit to be counted toward a student's final grade in the course, module completion grading emphasizes counting the modules completed to satisfaction. We still give grades for each assignment, but rather than use a 4-level E/S/N/U scale, I use a binary 1/0 scale. Receiving a 1 on all the work in a module signifies satisfactory completion.

This policy is used in my CSE 373 courses, the latest of which will be [CSE 373 Winter 2022](https://courses.cs.washington.edu/courses/cse373/22wi/#deliberate-practice).

**How is progress communicated?** The binary 1/0 scale is a good fit for single-number learning management systems, so it's relatively easy to adapt. Modules can be communicated using any medium: it could be posted as a document, discussed in class, included in the syllabus, or presented using [Canvas modules](https://community.canvaslms.com/t5/Canvas-Basics-Guide/What-are-Modules/ta-p/6). Canvas provides robust features for modules, including the ability to [add requirements](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-add-requirements-to-a-module/ta-p/1131) that students must complete in order to pass a module. I use module requirements to codify the score requirements for assignments in a module, and as student work is graded, the module immediately updates to reflect their progress through the course.

![Module completions](/assets/images/module-completions.svg)

What I like about this policy is that it abstracts-away all the details of the grading policy until later when the assignments are actually released. It allows you to easily incorporate work such as participation. Just include it in the module to communicate the importance of the work. In the past, I've had modules that included pre-class preparation work as part of the requirements for satisfactory completion of the module. Since my courses are on Ed, I wrote another script to send the entire class's [lesson completions from Ed to Canvas](https://gist.github.com/kevinlin1/9d233b3f9957201f619afb9d5b27a08e).
