---
layout: post
title: Learning from errors
excerpt: >-
  Self-regulation and metacognition in algorithm design.
---

How do we start solving a programming problem?

Some programmers prefer to jump in and write code immediately so that they can get to identifying and debugging the program sooner rather than later. This style of exploratory coding is helpful for learning more about the characteristics of the problem, with the often implicit assumption that the final program will look very different from the initial prototype. By building an initial prototype, programmers learn more about the complexities of the problem so that they can then integrate lessons learned towards designing a better program. Old ideas (and code) are frequently discarded to make space for new ideas in this *bricolage* or trial-and-error problem solving approach.

In computer science especially, problem understanding is the first step towards problem solving. While bricolage can help when problems are not well understood, many of the educational programming problems that students solve in introductory programming courses are relatively well understood. Educational programming problems are often developed using backward design: keeping a particular set of learning objectives in mind, the course staff wrote a complete program, removed its implementation, and only then drafted the specification. The goal of educational programming problems is not to teach or evaluate students' general problem exploration skills, but rather specific learning objectives. As a result, a little planning goes a long way.

One remaining challenge in solving educational programming problems is that there's still a gap between the problem solutions that we already know and the slightly different problem in front of us. This requires us to focus a bit on problem understanding, but not enough to demand programming like in the bricolage approach. We can apply the first four steps of the [Design Recipe](https://htdp.org/2020-8-1/Book/part_preface.html#%28counter._%28figure._fig~3athe-design-recipe%29%29) to gain a deeper understanding of the problem.

1. **From Problem Analysis to Data Definitions**. What kind of information is involved, and how is the data structured?
1. **Signature, Purpose Statement, Header**. What is the purpose of the function, and what exactly does it compute?
1. **Functional Examples**. What are some example inputs, and what should the function do with those inputs?
1. **Function Template**. What similar problem solutions and problem templates have we used in the past?

Throughout this process of learning about the problem, new information and examples can complicate the design.

> Examples play a central role at almost every stage. For the chosen data representation in step 1, writing down examples proves how real-world information is encoded as data and how data is interpreted as information. Step 3 says that a problem-solver must work through concrete scenarios to gain an understanding of what the desired function is expected to compute for specific examples.

How do we deal with complexity when an example doesn't work with the existing design? How should the design be changed to accommodate it? Sometimes, it's necessary to increase the **solution complexity** when an existing design can't handle the **problem complexity**. For example, a problem that we realize actually needs to consider every position as a possible starting point needs to have a solution that also considers that possibility.

But, oftentimes, solution complexity increases because code is already written against a design that doesn't handle the problem complexity. This practice accumulates something known in the study of software engineering as **technical debt**. Technical debt is "paid off" when programmers redesign the program through **code refactoring**.
