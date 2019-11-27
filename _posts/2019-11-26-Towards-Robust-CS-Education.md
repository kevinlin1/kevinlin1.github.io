---
layout: post
title: Towards Robust CS Education
excerpt: >-
  Equitable CS education in higher-ed: a 2-year retrospective on Teaching to Groups.
---

*Part two of [Teaching to Groups]({% link _posts/2018-02-04-Teaching-to-Groups.md %}).*

I used to think undergraduate teaching assistants (TAs) were the most amazing part of a CS course. I admired my TAs, and I owe to them my interest in teaching computer science. I mostly still think this way. But, over time, I've grown increasingly critical of what I call **inherited pedagogy**: when a teacher chooses their pedagogy based on how their teachers taught them. These practices reinforce the status quo, and we know that the status quo often enables diversity and achievement gaps in CS education. How can we design a technical CS education that is accessible to all undergraduates?

If we want to teach CS equitably in higher education, if we want to close the diversity and achievement gaps, then we need to begin with a common understanding of the goals of CS education.

> [Computer science is the study of computers and all the phenomena surrounding them][] ([Newell, Perlis, Simon, 1967][])

[Computer science is the study of computers and all the phenomena surrounding them]: https://computinged.wordpress.com/2016/02/01/computer-science-is-the-study-of-computers-and-all-the-phenomena-surrounding-them/
[Newell, Perlis, Simon, 1967]: https://science.sciencemag.org/content/157/3795/1373.3

The study of computer science includes the study of data representation (data structures), data transformation (algorithms), abstractions over these processes and structures, and the effects of these ideas on humans and society.

Broadly speaking, effective teaching at any level necessarily requires an equity perspective on education. Teaching is not merely about the transfer of information from one mind to another, but rather about creating access to relevant, actionable critical thinking skills that ultimately lead to individual empowerment ([Freire, 1968][]). In other words, the purpose of a course is not the course in and of itself, but rather its realized student outcomes. The difference between an effective or ineffective teacher cannot simply be determined by their [student evaluations][], which capture a wide variety of psychological phenomena mostly unrelated to the goal of educational equity. Equitable CS education requires optimizing pedagogy to enable a more diverse set of students to meet higher educational outcomes, not just increasing their [feeling of learning][].

[Freire, 1968]: https://patitsas.github.io/2016/01/28/On-Paulo-Freire-and-seeing-computing-as-literacy/
[student evaluations]: https://www.stat.berkeley.edu/~stark/Preprints/setNotes19.pdf
[feeling of learning]: https://www.pnas.org/content/116/39/19251

## Productive Failure

> [Productive Failure][] (PF) is a learning design that entails the design of conditions for learners to persist in generating and exploring representations and solution methods (RSMs) for solving complex, novel problems. Though such a process may initially lead to failure to generate canonical RSMs, it has a hidden efficacy that is germane for learning provided an appropriate form of instructional intervention follows that can consolidate and assemble student-generated RSMs into canonical RSMs. (Kapur)

[productive failure]: https://www.manukapur.com/productive-failure/

What is the critical thinking skillset specific to CS education? One framing for CS education is to view it as a problem of obtaining canonical mental representations and solution methods (RSMs). In this view, "programming is not merely about language syntax and semantics, but more fundamentally about the iterative process of refining mental representations of computational problems and solutions and expressing those representations as code" ([Loksa et al., 2016][]). As computing experts, we have acquired robust RSMs that enable us to analyze, select, adapt, and apply a wide variety of programming and problem-solving plans to solve a range of computing-framed problems.

[Loksa et al., 2016]: https://dl.acm.org/citation.cfm?id=2858252

However, acquiring canonical mental representations is [anything but a straightforward task for novices][debugging failure].

> Experiences of failure are frequently so negative that students shut down (Holt, 1964), lose agency (Weiner, 1985), and develop low self-efficacy (Bandura, 1982) and learned helplessness (Abramson, Seligman, & Teasdale, 1978). Surrendering too quickly to obstacles is particularly unfortunate, given experimental evidence that initially "getting it wrong" ultimately breeds deep and sustained learning (Kapur, 2008).

[debugging failure]: https://edrl.berkeley.edu/projects/debugging-failure/

Productive failure suggests a framework for teaching CS skills by means of iterative refinement of RSMs.

1. **Priming**. Present a problem that is beyond students' current problem-solving capacities ([Zone of Proximal Development][]). Prior knowledge is activated even though students are unable to solve the problem.
2. **Consolidation**. Students learn from comparison between their partial or incomplete RSMs and the canonical RSMs. [Subgoal labeling][] and targeted, explicit instruction can draw attention to key features of the problem. Learning happens when feedback is timely, is specific on what thinking was incorrect, and provides a path for improvement. ([Wieman, 2018][])
3. **Recalibration**. Provide an isomorphic problem and return to step 1.

[Zone of Proximal Development]: https://en.wikipedia.org/wiki/Zone_of_proximal_development
[Subgoal labeling]: https://dl.acm.org/citation.cfm?id=2361291
[Wieman, 2018]: https://depts.washington.edu/amath/slides/20180426-Wieman.pdf

Within the context of productive failure, teachers are responsible for designing structures for student interaction, facilitating group discussions, building intrinsic motivation, and providing. Critically, teachers play an important role in [framing classroom climate for student learning and retention][classroom climate] (Barker et al., 2014). Teachers, as the dominant force for classroom socialization, set the norms for accepted communication in the classroom.

[classroom climate]: https://dl.acm.org/citation.cfm?id=2538959

In undergraduate CS classrooms, a hierarchy of value for student responses is established through the way in which teachers respond to student suggestions. For example, when an incorrect answer is suggested, the teacher will sometimes dismiss it nicely *without giving the incorrect suggestion more than one second of consideration*. Other times, they may discuss why it's incorrect *without giving it spatial consideration on the board*. These are just two of several dimensions by which teachers are biased towards correct answers to the detriment of incorrect answers. But there's an even more fundamental problem with this example: by funneling student ideas into the dichotomy of either correct or incorrect, student responses are immediately judged on those merits, obscuring the underlying mental RSMs responsible for producing the answer. (Lin, unpublished)

If robust CS education requires iteratively refining students' mental RSMs, then it is the teacher's responsibility to design supportive classroom communication climates that encourage mutual collaboration, development, and introspection of incomplete mental RSMs, not answers.

## Pedagogical Development

However, teachers don't improve overnight. Four stages of psychosocial pedagogical development are outlined in *How Professors Develop as Teachers* ([Kugel, 1993][]):

> Typically, when they begin their teaching careers, professors focus their concern primarily on their own role in the classroom (stage 1: self). When they have mastered this role, at least to their own satisfaction, the focus of their concern shifts, first to their understanding of the subject matter they teach (stage 2: subject) and then to their students' ability to absorb what they have been taught (stage 3: student). With this last shift comes a more general shift of focus from teaching to learning, that begins, in stage 3, with a focus on helping their students become more absorbent (stage 3: student as receptive). Concern then typically shifts to helping students learn to use what they have been taught (stage 4: student as active) and then to helping them to learn on their own (stage 5: student as independent).

[Kugel, 1993]: https://www.mach.kit.edu/download/HowProfessorsDevelop.pdf

In the most extreme interpretation, this model implies that "what comes later must be better" (Kugel, 1993). Indeed, STEM education research in the past 20+ years have championed evidence-based teaching practices for active learning with the goal of improving student outcomes. But framing the problem as simply advancing through linear stages dehumanizes the teacher in the process, as "the work that is done within a stage is important and cannot always be hurried" (Kugel, 1993).

As in *Pedagogy of the Oppressed* ([Freire, 1968][]), the purpose of a course is not to serve the teacher's "own satisfaction", but rather about "helping [the student] learn on their own" in order to become more self-determining human beings. Teachers work with students to develop greater self-awareness about the world around them. As students develop a more complete sense of self based on their various experiences in the spaces surrounding them (affirming or denying aspects of CS identity, for example), so too does the teacher develop.
