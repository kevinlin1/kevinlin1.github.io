---
layout: post
title: Contraction Hierarchies
excerpt: >-
  Efficient Real-World Route Searching
---

[![Contraction Hierarchies Header](/contraction-hierarchies/header.png)](/contraction-hierarchies/)

> In this assignment, students implement a real-world route searching algorithm for HuskyMaps, a derivative of the street mapping application [Bear Maps][] (Nifty Assignment 2018). The assignment applies several topics commonly taught in CS2, including priority queues, graphs, shortest paths algorithms, binary trees, tree traversals, testing, and debugging large programs. After building HuskyMaps in a previous homework, this homework challenges students to improve upon the relatively simple A\* route search algorithm by implementing [contraction hierarchies][], a 2008 algorithm for efficient routing based on the idea that many shortest paths queries share the same major roadways. This can be done in 3 phases: (1) compute an importance heuristic for each vertex; (2) add new shortcut edges by contracting each vertex in the order given by the importance heuristic; and (3) precompute the shortest paths on the augmented graph from each vertex to increasingly important roadways. Afterwards, a source-to-destination route search query can be answered by finding the common most-important roadways (midpoints) and reconstructing the best path from source to midpoint to destination. Reconstructing the path is an application of inorder tree traversal since each shortcut edge contains two smaller edges, both of which can also be shortcut edges. Each part of this assignment can be scaffolded. Unit tests on a small, manually-computable graph provide immediate, formative feedback to students as they develop their implementation. Randomized route search queries serve as a stress test for the correctness and efficiency of their implementation, which they can compare against their earlier A\* search algorithm implementation.

[Bear Maps]: http://nifty.stanford.edu/2018/hug-bear-maps.html
[contraction hierarchies]: http://algo2.iti.kit.edu/schultes/hwy/contract.pdf

- [Assignment Landing Page](/contraction-hierarchies/)
- [Contraction Hierarchies briefly explained][] (Stefan Funke 2017)

[Contraction Hierarchies briefly explained]: https://www.fmi.uni-stuttgart.de/files/alg/teaching/s15/alg/CH.pdf
