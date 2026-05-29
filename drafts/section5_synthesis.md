# §5 Draft — Synthesis: Thesis and Trajectory
## Target: 8–10 minutes | Estimated actual: ~11–12 minutes

*Working draft for speaker revision. Delivery notes in [brackets].
§5 has two jobs: deliver the thesis and point at where physics is going.
The mathematics material in §5.1–5.3 appears again in §6, but in a
different register — §5 is the analytical argument; §6 is the rhetorical
landing. Don't recapitulate §4; build on it.*

*§5.6 (the first-person section) is a skeleton — the speaker must fill this in
with actual experience. The structure is provided; the content must be personal.*

---

### The adoption curve

[New slide or transition graphic: "Software → Mathematics → Theoretical Physics"]

There's a pattern in how AI capability has moved through rigorous formal domains.

Software engineering first. Not because it is the most formal, but because code
has the most immediate verification feedback: it either runs or it doesn't. By
2023, GitHub Copilot was shipping code daily in the codebases of practicing
engineers. By 2024, AI was solving real software bugs from public repositories
in competitive benchmarks — not toy problems.

Mathematics is next on the curve. Close enough to physics in formalism and rigor
to function as a leading indicator. Currently ahead of physics. The Castelvecchi
*Nature* feature from May of this year documents where it is.

And then: theoretical physics.

The argument is not that physics is the same as mathematics. It is that the distance
between mathematics and theoretical physics on this adoption curve is shorter than
the distance the curve has already covered. What is happening in mathematics in 2026
is not a distant future for physics; it is the near term, visible now.

---

### Mathematics in May 2026

[Slide: the Castelvecchi headline from *Nature*, or the Erdős problem number alone]

The Castelvecchi *Nature* feature describes what is happening in mathematics in real
time. A few things from that article that I want to put in front of this room.

Liam Price — no formal mathematics training, hasn't attended university, working from
his home in southwest England — solved Erdős problem number 1196 using ChatGPT. The
problem was posed by Paul Erdős in 1966. It had resisted specialists for sixty years.

The solution surprised mathematicians, and not just because it was reached by a
non-specialist. What surprised them was *how*. Prior attempts had translated the
problem into probability theory language. That was the natural move — experienced
number theorists, encountering this problem, rephrased it in the register they trusted.
ChatGPT solved it in the original formulation. Its solution implicitly established
the probability connection that human solvers had needed to introduce explicitly at
the start.

The AI found a path through the original terrain that humans had walked around,
precisely because human training told them the terrain was harder than the detour.

[Pause.]

Terence Tao, commenting on this result, identifies exactly this as what was surprising.
Those who had tried solving the problem began by rephrasing it in probability theory
language. GPT solved it in the number-theoretic original — and yet its solution
established the probability connection that human solvers had assumed they needed to
introduce first. The machine did not know the convention. It worked in the language
of the problem.

That result is published. Alexeev et al., arXiv, 2026.

---

### The trajectory and the indigestion problem

Castelvecchi reports a rare concrete trajectory for proof-length capability.

Current frontier models produce proofs of at most **three to four pages**. Internal
Google models are already reaching beyond that, targeting ten pages. One hundred
pages: "not within their capabilities right now, but we are working towards there."

[Delivery note: let the physics audience register that the Hsu *Physics Letters B*
paper is four pages. Current frontier proof-length capability is just reaching
the length of a publishable physics result.]

Luong at Google DeepMind has predicted that AI and mathematicians could jointly
win a Fields Medal by 2030. This is a four-year prediction from someone building
these systems.

And then there is the other side of this. Terence Tao has named a concern he calls
proof indigestion. Not "AI is writing proofs." Not "AI is getting results wrong."
The concern is: *we may soon have more verified results than the community can absorb
and understand.* Human referees are stretched thin evaluating human-written papers
already. The AI-generated ones coming into journal pipelines now make the problem
worse — and a referee cannot quickly distinguish a correct AI proof from a
plausible-but-wrong one without doing the work of verification.

This is the shadow side of the capability story, and it maps directly onto the
communicability requirement Lu et al. identify: if AI produces technically correct
but opaque derivations, human understanding lags behind verified truth. A physics
result that is verified but that no physicist can give a talk on, or answer questions
about, is not physics in any meaningful sense. Physics has always demanded more than
correctness — it demands understanding, intuition, the capacity to generalize.

---

### Efficiency is not insight

Before the steelman, one more distinction the *Nature* editorial names precisely:

> *"We don't yet know whether greater efficiency equates to greater insight."*

The efficiency gains are real. Robin analyzed 551 papers in 30 minutes; human
equivalent, roughly 540 hours. Co-Scientist reached in two days what a research
group had worked toward for a decade. These numbers are not in dispute.

But efficiency in science is not the same as quality of science. The history of
theoretical physics has a particular relationship with inefficiency. Feynman's path
integral came from trying to make sense of a notation in Dirac. BCS theory came from
an approach to nuclear physics that seemed unpromising. 't Hooft's renormalization
proof came from a student following a suggestion his supervisor thought would lead
nowhere. These are examples of the kind of exploration that an efficiency-optimized
system would have routed around — and that turned out to be the path.

There is also a field-level version of this concern. If multiple research groups use
the same AI system to generate hypotheses, the hypothesis space explored by the field
may narrow — many groups following the same AI-suggested directions, other directions
untouched. This is convergent search at the scale of a discipline. Physics has a long
history of results that required a human to first notice an apparently unpromising
direction was interesting. That judgment is not capturable in a structured task
specification.

---

### The steelman: why physics might be different

Before I give you the thesis, I want to take the strongest objections seriously —
because they are real, and because addressing them honestly is what makes the thesis
credible.

**Physics requires physical reality, not just formal consistency.**
A mathematical proof can be evaluated entirely within formal systems. A physical
result must connect to experiment and to the structure of the physical world. The
Chern number example from §4 makes this precise: the linear algebra is trivial,
but the physics is in the winding number's relationship to a measurable Hall
conductivity. Passing that gap — from the formalism to the physics — requires
knowing what the formalism is about. Whether LLMs grasp this in any meaningful
sense remains unclear.

**The hallucination risk is asymmetric.**
In mathematics, a wrong proof is eventually caught. The formal verification
ecosystem is increasingly capable of finding errors. In physics, a plausible-but-wrong
result can propagate through the literature for years before the experimental test
comes. The Reeh-Schlieder episode consumed significant expert effort from one of the
most capable QFT theorists working in this area. At scale, across many groups using
LLMs and publishing results, this becomes a serious problem for how the field
allocates attention. The asymmetry between "generates plausible physics" and
"generates correct physics" is structurally more dangerous in physics than in
mathematics.

**Physical intuition is not pattern matching on the existing literature.**
This is the hardest version of the steelman. Knowing which approximation to trust
in a new domain, knowing when a formally correct calculation is physically misleading,
knowing that a particular model is elegant in a way that suggests it captures
something real — these are skills that resist precise characterization even by
the physicists who have them. Lu et al.'s "research taste" and "approximation
judgment" remain the least evaluable capabilities. We don't know if LLMs have them
because we don't have a reliable test.

**The normative and epistemic limits.**
The sharpest version of the steelman comes from Botvinick and Gershman — not from
physicists, from cognitive scientists, writing in a 2025 PNAS paper about LLMs in
science. They identify two aspects of science that should remain irreducibly human —
not because AI cannot perform them, but because they should not be delegated even
if AI could.

The normative aspect: what problems shall we work on? Judgments of interestingness,
significance, and timeliness are tied to culturally and historically grounded
sensibilities that evolve over time. Science no longer approaches certain questions
the way it did fifty years ago — not because the evidence changed, but because the
values did. That value evolution is not derivable from the existing literature. An
AI trained on the past record cannot generate it; it can only reflect the values
already encoded in its training data.

The epistemic aspect: "Would it be satisfactory to have AI systems that successfully
model aspects of nature — as reflected in accurate predictions — but which do not
directly advance human knowledge concerning the underlying principles or mechanisms?
From an engineering standpoint, that might be fine. However, if it's basic science
we're talking about, we shouldn't let go of the core objective, which is not just
practical but epistemic."

Physics has always cared about the why. A verified result without an explanation
is engineering. The normative and epistemic arguments are different in kind from
the capability arguments — they are not claims about what AI can't do, but about
what shouldn't be delegated even when AI can do it.

**The honest conclusion of the steelman**: these differences are real. They are also
not obviously permanent. The same arguments were made about chess, formal proof,
code generation. In each case, the capability arrived earlier than the argument
predicted. But the normative and epistemic distinctions are more durable — and for
physicists specifically, they are where the question of what we value in our work
gets asked most sharply.

---

### The thesis

[Delivery note: pause before this. Say it once, cleanly. No slide needed — or
a slide with just the thesis sentence if the room is large.]

Here is what I take the evidence to show.

> *LLMs have crossed from tools into contributors at the calculation and conjecture
> levels of theoretical physics — still requiring expert oversight, but already
> appearing in published results — and mathematics is showing us, in real time,
> what happens when that oversight requirement starts to erode.*

That sentence has three parts and each one does work.

"Crossed from tools into contributors at the calculation and conjecture levels":
Pan et al. at 87.5/100 on condensed matter HF derivations. Hsu in *Physics Letters B*.
Those are contributions — not assistance, not autocomplete. They are at different
levels of the research workflow, but they are in the literature.

"Still requiring expert oversight, but already appearing in published results":
both halves of this are true simultaneously. The oversight is not optional —
the Reeh-Schlieder episode, the 44.5% hallucination rate, the characteristic failure
pattern. And the results are published and peer-reviewed. This is the present state.

"Mathematics is showing us, in real time, what happens when that oversight requirement
starts to erode": the Erdős case, the proof-indigestion dynamic, the Fields Medal
prediction. This is the near-term trajectory, visible now in a field close enough
to theoretical physics in rigor that physicists should treat it as a leading indicator.

---

### A first-person note

[Delivery note: this section must be revised with actual personal experience.
The structure below is a prompt, not a script. Say what is true.]

I want to say something briefly from my own experience, because it is evidence that
no published paper can give you — or at least none that I know of from someone
with my specific combination of backgrounds.

I have studied QFT and related areas seriously, including under Bryce DeWitt.
I also use these models daily — not to write papers, but to work through physics.
The experience is genuinely strange.

[Fill in from actual use: where the LLM helps most readily — probably: following
an argument, checking whether you've set up a derivation correctly, asking what
the physical picture is behind a formalism. Where it misleads — probably:
precisely the Type 2 and Type 3 failures from §4. The moment of discovering a
plausible-seeming output is wrong is distinctive. What makes you catch it?]

[The question worth sitting with for the audience: does your experience of catching
an LLM error require you to already know the answer? If so, what does that tell us
about who can use these tools effectively in physics research, and at what point in
their training?]

---

### What it means for this room

The physicist's role is not disappearing. But it is shifting — and the shift has
already begun, in labs and offices where LLMs are used and not disclosed, in the
gap between what the Hsu acknowledgements say and what his methodology paper shows.

The physicists who are thinking clearly about what these tools can and cannot do —
right now, in 2026, before the transition is complete — will be in a better position
to shape what it looks like than those who wait until it has already happened.

That is not a claim about AI. It is a claim about the history of physics.

[Transition to §6:]

I want to close by returning to where we started.
