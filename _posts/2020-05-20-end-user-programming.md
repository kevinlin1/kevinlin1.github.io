---
layout: post
title: End-user programming
excerpt: >-
  When it's really not about the turtles all the way down.
---

**Abstraction** is one of the most important ideas in computer programming. By defining methods, programmers give names to computational ideas. Abstraction allows clients to use these computational ideas without understanding the implementation details. Another kind of abstraction, known as **data abstraction**, is about defining abstract data types (e.g. list) to separate the behaviors of a data type from its implementation details (e.g. resizing array, linked nodes).

However, beyond both of these perspectives, abstraction applies at multiple levels in a software product.

1. An **end-user** uses a software product to achieve change something about the world or learn something new. They interact with the computational environment by clicking buttons, entering input fields, speaking voice commands, gesturing, etc.
1. These actions (often called **events**) are passed to the **client** program. The client program includes all of the business logic for getting things done. But the client program depends on many lower levels of programming abstractions, such as lists, sets, maps, etc.
1. These programming abstractions are provided by the **implementer**. It's up to the implementer to provide a correct (and, ideally, efficient) implementation of the programming abstraction.

Between each level is an interface, a contract upheld by the adjacent level. Java interface serve as the bridge between clients and implementers by representing the idea of abstract data types. Implementers implemented these interfaces with classes such as `ArrayList` and `LinkedList`. A course on **data structures and algorithms** (CSE 373 for non-majors, CSE 332 for majors) will explore more of these implementation details.

Just as there is an interface (in Java, literally `interface`) between clients and implementers, there's also the **user interface** between users and clients. However, there is an increasingly large demand for **end-user programming**, which hasn't been a traditional focus of computer science. Rather than using a pre-packaged application written by a professional software engineer, there are many people who use programming as a tool to help them get things done.

Some examples of end-user programming include data analysis, web programming (CSE 154), and home automation. In reality, end-user programming is all around us: any system where we (as end-users) can define its behavior is an example of programming. Oftentimes, these don't even involve typing code into a computer. Spreadsheets react to changes whenever we enter new values. Voice commands allow us to specify actions in response to sensors. Gaming is about using peripherals or even our own body to execute plans in virtual environments.

Every system has its own set of rules and its own abstractions: different "methods" for interacting with the system and defining new behaviors. Part of what makes end-user programming (and all of our computing experiences) so different from the computer programming in this course is due to the mismatch between expectations about these abstractions. The programming in this course introduces just one (historically important) set of programming abstractions. It's not particularly better or necessarily more versatile than other abstractions.

One style of programming at the intersection of the end-user and client/implementer programming is **data programming** (CSE 163). Data programming expands on the programming abstractions that we learned in client/implementer programming by using our skills to harness computing to answer questions about a dataset. [John D. Cook describes how scientists use software as a tool.](https://www.johndcook.com/blog/2011/07/21/software-exoskeletons/)

> I work with scientists and programmers, often bridging the gaps between the two cultures. One point of tension is defining when a project is done. To a scientist, the software is done when they get what they want out of it, such as a table of numbers for a paper. Professional programmers give more thought to reproducibility, maintainability, and correctness. Scientists think programmers are anal retentive. Programmers think scientists are cowboys.
