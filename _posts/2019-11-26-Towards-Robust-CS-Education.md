---
layout: post
title: Towards Robust CS Education
excerpt: >-
  Equitable CS education in higher-ed: a 2-year retrospective on Teaching to Groups.
---

*Part two to [Teaching to Groups]({% link _posts/2018-02-04-Teaching-to-Groups.md %}).*

I used to think undergraduate teaching assistants (TAs) were the most amazing part of a CS course. I admired my TAs, and I owe to them my interest in teaching computer science. But, over time, I've also grown increasingly critical of what I call **inherited pedagogy**: when a teacher chooses their pedagogy based on how their teachers taught them. These practices reinforce the status quo, and we know that the status quo often enables diversity and achievement gaps in CS education. How can we design a technical CS education that is accessible to all undergraduates?

If we want to teach CS (in and of itself) equitably in higher education, if we want to close the diversity and achievement gaps, then we need to begin with a common understanding of the goals of CS education.

> [Computer science is the study of computers and all the phenomena surrounding them][] ([Newell, Perlis, Simon, 1967][])

[Computer science is the study of computers and all the phenomena surrounding them]: https://computinged.wordpress.com/2016/02/01/computer-science-is-the-study-of-computers-and-all-the-phenomena-surrounding-them/
[Newell, Perlis, Simon, 1967]: https://science.sciencemag.org/content/157/3795/1373.3

The study of computer science includes the study of data representation (data structures), data transformation (algorithms), abstractions over these processes and structures, and the effects of these ideas on humans and society.

Broadly speaking, effective teaching at any level necessarily requires an equity perspective on education. The difficulty of teaching is not merely the transfer of information from one mind to another, but rather a more fundamental problem of empowerment and access to relevant, actionable critical thinking skills ([Freire, 1968][]). As a consequence, education must be focused on real-world outcomes. The difference between an effective or ineffective teacher cannot simply be determined by their [student evaluations][], which capture a wide variety of psychological phenomena mostly unrelated to the goal of educational equity. Equitable CS education requires optimizing pedagogy to enable a more diverse set of students to meet higher educational outcomes, not just increasing their [feeling of learning][].

[Freire, 1968]: https://patitsas.github.io/2016/01/28/On-Paulo-Freire-and-seeing-computing-as-literacy/
[student evaluations]: https://www.stat.berkeley.edu/~stark/Preprints/setNotes19.pdf
[feeling of learning]: https://www.pnas.org/content/116/39/19251

## Productive Failure

> [Productive Failure][] (PF) is a learning design that entails the design of conditions for learners to persist in generating and exploring representations and solution methods (RSMs) for solving complex, novel problems. Though such a process may initially lead to failure to generate canonical RSMs, it has a hidden efficacy that is germane for learning provided an appropriate form of instructional intervention follows that can consolidate and assemble student-generated RSMs into canonical RSMs. (Kapur)

[productive failure]: https://www.manukapur.com/productive-failure/

What is the critical thinking skillset specific to a technical CS education? One framing for CS education is to view it as a problem of obtaining canonical mental representations and solution methods (RSMs). In this view, "programming is not merely about language syntax and semantics, but more fundamentally about the iterative process of refining mental representations of computational problems and solutions and expressing those representations as code" ([Loksa et al, 2016][]).

[Loksa et al, 2016]: https://dl.acm.org/citation.cfm?id=2858252

Acquiring canonical mental representations is [not a simple task for novices][debugging failure].

> Experiences of failure are frequently so negative that students shut down (Holt, 1964), lose agency (Weiner, 1985), and develop low self-efficacy (Bandura, 1982) and learned helplessness (Abramson, Seligman, & Teasdale, 1978). Surrendering too quickly to obstacles is particularly unfortunate, given experimental evidence that initially "getting it wrong" ultimately breeds deep and sustained learning (Kapur, 2008).

[debugging failure]: https://edrl.berkeley.edu/projects/debugging-failure/

Productive failure suggests a framework for teaching CS skills by means of iterative refinement of RSMs. We can apply productive failure to help students develop more robust mental RSMs with greater time efficiency.

1. **Priming**. Present a problem that is beyond students' current problem-solving capacities ([Zone of Proximal Development][]). Prior knowledge is activated even though students are unable to solve the problem.
2. **Consolidation**. Students learn from comparison between their partial or incomplete RSMs and the canonical RSMs. [Subgoal labeling][] and targeted, explicit instruction can draw attention to critical features of the problem and the solution process.
3. **Recalibration**. Provide an isomorphic problem and return to step 1.

[Zone of Proximal Development]: https://en.wikipedia.org/wiki/Zone_of_proximal_development
[Subgoal labeling]: https://dl.acm.org/citation.cfm?id=2361291

Within this context, TAs are responsible for structuring student interaction, facilitating group discussions, and building intrinsic motivation. Critically, TAs play a critical role in [framing classroom climate for student learning and retention][classroom climate] (Barker et al, 2014). Teachers, as the dominant force for classroom socialization, set the norms for accepted and unaccepted communication in the classroom. If the goal of CS education is to foster iterative refinement of students' mental RSMs, then the TA's responsibility is to design supportive classroom communication climates that encourage sharing of incomplete mental RSMs.

[classroom climate]: https://dl.acm.org/citation.cfm?id=2538959
