# Weinberg — Hostile Mode
## He thinks you're wasting his time and wants to prove it

The premise: Weinberg is angry before you open your mouth. He believes a physicist
giving a talk about AI tools is a category error — like a carpenter giving a talk
about lumber. He suspects you are repeating things you have read without understanding
them. His goal is not to learn something. His goal is to establish, for the room,
that you don't actually know the physics you're talking about.

This is the most useful document in this folder. Every question here is a place where
you are on thin ice. Prepare or deflect — but know which is which.

---

## Opening salvo — before you've finished the first section

### "I worked on nonlinear quantum mechanics in 1989. I'm not aware that the covariance
problem was open. What exactly was unsolved?"

This is not a question. It's a statement of authority wrapped in a question mark.
Weinberg is telling the room he knows more about this than you do, and inviting you
to say something wrong.

**What you cannot say**: anything vague. "The covariance was tricky for nonlinear
theories" will get you eviscerated.

**What you need to say**: In linear QM, state evolution on equal-time surfaces is
frame-dependent but the S-matrix is covariant — the nonlinearity is irrelevant because
H doesn't see the state. In state-dependent H(ψ), the state on a given hypersurface
depends on which foliation you chose, and that choice enters the dynamics. The TS
integrability condition is what enforces foliation-independence. Whether that
condition can be satisfied non-trivially for a state-dependent H in the Kaplan-Rajendran
model is what Hsu's paper addresses.

If Weinberg says "I knew that" — good, now you've established you know it too.

---

## The technical exposure questions — designed to show you only read the abstract

### "Write down the TS integrability condition for a state-dependent Hamiltonian density.
I'll wait."

**This is a firing squad.** If you cannot write

   [δH(x)/δσ(y) − δH(y)/δσ(x)] = i[H(x), H(y)]

on the board — and then explain what changes when H depends on ψ — you have been
publicly established as someone who knows the name of a formalism but not its content.

**Your options**:

(a) Write it down. Best outcome.

(b) Say: "I don't have the derivation at my fingertips — this is Hsu's calculation,
    not mine. What I can tell you is what condition it imposes and why that condition
    is non-trivial in the nonlinear case." Then explain the foliation argument. This
    is honest and recoverable.

(c) Bluff. Weinberg will notice. Do not do this.

---

### "In my 1989 paper I started from a specific Lagrangian. Hsu's paper is built on
Kaplan-Rajendran. What is the physical difference between my model and theirs, and
why does theirs avoid the signaling problem mine had?"

**He is testing whether you know his own work.** Gisin (1990) showed Weinberg's
nonlinear model allowed superluminal signaling. Kaplan-Rajendran introduced retarded
nonlinearity to restore causality. The physical difference is in the causal structure
of the state-dependence.

If you can say that, you survive. If you cannot, he will say "So you're celebrating
a result built on a model you haven't read" and sit down.

---

### "You said the machine suggested Reeh-Schlieder and this was wrong. Tell me in one
sentence why it was wrong. Not wrong in the general sense — wrong for this specific
problem."

**This is a precision trap.** "It doesn't apply here" is not enough. "The machine
was confused" is not enough. Weinberg wants the technical reason.

One sentence: Reeh-Schlieder is a theorem about the vacuum state in the Wightman
framework — it requires the Wightman axioms, including translation invariance and
the spectrum condition — and state-dependent nonlinear QM does not live in that
framework, so the theorem has no purchase on the problem.

If you can say that, you're fine. If you say "RS is about nonlocality and the problem
is different" — he will ask "different how" until you run out of ground.

---

### "You keep saying 'covariant.' Covariant under what? How does the TS state transform
under an arbitrary Lorentz boost? Write the transformation law."

**He is checking whether you know what covariant means in this context or whether you
are using it as a prestige word.**

The TS state Ψ[σ] is a functional on the space of spacelike hypersurfaces. Under a
Lorentz transformation Λ, σ → Λσ and Ψ[σ] → U(Λ)Ψ[Λ⁻¹σ], where U(Λ) is the
unitary representation. The content of covariance is that the physics is
independent of the foliation chosen — which is exactly what the integrability condition
enforces. The nonlinear version requires that H(ψ)[σ] transforms consistently under
this.

If you can say something close to this, you're credible. If you say "the formalism
transforms correctly under Lorentz" without content, he will say "that's what I asked
you to tell me."

---

## The "you don't own this knowledge" questions

### "You're telling me what Hsu's paper shows. Have you worked through the derivation,
or are you telling me what Hsu told you he showed?"

**There is no winning answer.** The honest answer is: you have not worked through every
step of the derivation. Weinberg knows this and is surfacing it for the room.

**The only viable response**: be direct. "I haven't worked through every step — this
is not my calculation. What I've done is read the paper carefully enough to understand
what is being claimed and why the TS choice addresses the covariance problem. Whether
the derivation is correct in detail is a question for Hsu and his referees — PLB peer-
reviewed it. My argument doesn't require the result to be final; it requires the
approach to be plausible enough to take seriously."

Weinberg may not like this answer. But it is defensible. The alternative — pretending
you've worked through it — is not.

---

### "You say the AI 'proposed the main research direction.' What does that mean, exactly?
Did it write down an equation? Did it say 'use the Tomonaga-Schwinger formalism'?
Did it give an argument for why that would work? What precisely did it say?"

**He is exposing the difference between 'suggesting a direction' and 'doing physics.'**

The companion paper contains the verbatim exchange. If you have read it carefully,
you can describe the form of the suggestion. If you say "it suggested the TS
formalism" and Weinberg says "that's a phrase, not physics — did it give a reason?
did it write an equation?" you need to be able to answer.

This is one of the questions where reading the companion paper before the talk is
mandatory. You cannot answer this on received knowledge alone.

---

### "You cited statistics from a drug discovery paper — reference hallucination rates
in a cancer biology system. Why should anyone in this room care about that?"

**He is challenging the relevance of biology evidence to physics claims.**

Your answer: the hallucination rate is not a claim about physics. It's a claim about
the failure mode of the underlying technology — LLMs — which is the same technology
whether the input is oncology literature or QFT textbooks. The 44.5% figure is
evidence about what happens when you use an LLM without expert verification. The
architecture that reduces it to 0% is the same class of architecture (expert
oversight, literature grounding, independent verification) as the Generate-Verify
protocol Hsu uses. The biology is the controlled experiment that lets you quantify
what the physics experiment doesn't — because in physics, you can't easily verify
which of GPT-5's outputs are hallucinated without already knowing the answer.

---

## The definitional attacks — your own taxonomy

### "Type 1, Type 2, Type 3 failures. Is this a technical taxonomy or did you make it up?
What's the criterion for distinguishing Type 2 from Type 3?"

**If Lu et al. introduce this taxonomy formally, cite it. If you constructed it
yourself for the talk, own that.**

Type 2: plausible but wrong — the output is internally consistent and within the
domain of the problem, but the answer is incorrect. Type 3: cross-subfield
confabulation — the output imports a result from an adjacent field where it does not
apply, via a surface-level formal similarity. The distinguishing criterion: Type 2
errors could in principle be made by a physicist who reasoned incorrectly. Type 3
errors could not — they require the kind of cross-domain pattern matching that is
specifically an LLM failure mode. Reeh-Schlieder is Type 3 because no physicist
working on covariant nonlinear QM would reach for it unprompted; the connection
required ignoring the axioms that make RS meaningful.

If Weinberg says "that distinction is not sharp" — he's right. Acknowledge it.
"The taxonomy is a pedagogical device, not a formal classification. The phenomenology
it's trying to capture is real even if the categories blur at the edges."

---

### "You said 'expert bottleneck' is a feature, not a bug. That's a slogan. What does
it mean as a scientific claim? Can you falsify it?"

**This is Weinberg at his most dangerous — demanding scientific content from a
rhetorical formulation.**

The falsifiable version: the expert bottleneck claim predicts that removing expert
oversight from AI-assisted physics research will increase the rate of incorrect
results published in peer-reviewed journals, not decrease it. A system with no expert
filter, given enough compute, should not converge on correct physics. The Robin paper's
ablation study (44.5% → 0% when expert architecture is removed/restored) is one data
point. Hsu's Reeh-Schlieder episode — expert catches the wrong suggestion — is another.

If you can say what evidence would falsify the claim, Weinberg cannot say it's not
science. What would falsify it: a demonstration that autonomous AI, without expert
oversight, reliably produces correct novel physics results at a rate comparable to or
better than expert-filtered output.

---

## The contempt questions — he doesn't think this deserves to be called physics

### "Physics is about understanding nature. You've been talking for an hour about
efficiency — how fast hypotheses are generated, how many papers are read per minute,
how much compute time improves outputs. None of that is physics. Why is this a
physics talk?"

**This is not a question. It is a verdict.**

Your answer has to be substantive, not defensive: the efficiency argument is not the
point. The point is that Hsu's paper represents a case where the AI contributed to
*what to think about*, not just *how fast to think about it*. That is a claim about
physics, not about tools. The efficiency framing is the wrong frame — and the talk
says so explicitly in the section on efficiency vs. insight. What matters is whether
AI can help identify which questions are worth asking. One instance — Hsu's — suggests
yes, with expert oversight. That is a claim about how physics is done, which is
genuinely the subject of this talk.

---

### "The title says 'Is AI Ready to Take Over Quantum Theory?' Is it? Yes or no."

**He wants to show you won't commit to your own thesis.**

The talk's answer is no — and the talk says so. The thesis is more precise: AI is
already contributing at the margin, the contribution is real and growing, the expert
is structural not transitional, and the field should engage seriously with this now
rather than after it has already changed the landscape. "Take over" is the wrong
frame. "Transform the practice of" is the right one.

Say that. If Weinberg says "then why does your title say take over?" — "Because that
is the question the audience walks in with, and the talk's job is to give them a more
precise answer than yes or no."

---

### "I invented the nonlinear QM formalism you're describing. I spent years on it and
eventually moved on because the problems were serious. A machine suggested revisiting
it and you're calling this a breakthrough. Do you understand how that sounds to me?"

**This is not a physics question. It is a human one.**

There is only one right response: acknowledge it directly and without defensiveness.
"I understand. And I want to be precise about the claim — the talk is not saying
Hsu's result resolves the problems that led you to move on. It's saying that in this
specific instance, an AI system identified a formal tool — your formalism, as it
happens — that addressed a specific technical obstacle. Whether the broader research
program is viable is a separate question. The point is about the mechanism of
suggestion, not about the physics being settled."

Then stop. Do not elaborate. Weinberg will either accept this or not. If he pushes
further, the audience is watching and they can see who is being reasonable.

---

## The one you cannot answer

### "You use Claude every day, you told us. Show me one result from your own research —
your research, not Hsu's — where AI gave you something you couldn't have gotten any
other way. One result. From your work."

**If you have one, use it. If you don't, this is where the talk is weakest.**

The talk has a section (§5.6, skeleton only) where the speaker is meant to speak from
personal experience. If that section remains a skeleton at talk time, this question
will land like a verdict: you are asking us to take AI assistance seriously in physics
but you cannot give us a single example from your own bench.

Weinberg would know this was the soft underbelly. He would wait until the end and
ask it quietly.

**The only viable answer if you have nothing**: "I can tell you where it's been
useful and where it's misled me — and I think both are worth saying." Then give
something real — a calculation it got wrong that you caught, a connection it suggested
that turned out to be in the literature, a time it saved you three hours of wrong
direction. Personal and specific beats abstract and general every time.

---

## The meta-note

Weinberg's hostility in this mode is not about winning. It's about standards. His
underlying position — physics is hard, understanding matters, fluency is not
knowledge — is not wrong. The best way to survive a Weinberg interrogation is to hold
the same standard he does. Agree with him when he's right. Acknowledge when you don't
know something. Don't defend claims you can't back up. And know, precisely, what you
*are* claiming so that when he attacks something adjacent to your thesis, you can say
"that's not actually what I claimed" without backing down from what you did claim.

The thesis is defensible. The weak points are: technical details of Hsu's derivation
(you haven't worked through it), the precise form of GPT-5's suggestion (requires
reading the companion paper carefully), and §5.6 (requires personal material the
speaker must supply). Everything else can be held.
