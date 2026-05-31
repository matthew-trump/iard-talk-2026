# Tomonaga and Schwinger — Their Formalism Is the Subject
## Questions from the physicists whose work the machine suggested

The premise: both men are present. Their formalism — developed independently, under
entirely different circumstances, in the 1940s — is what GPT-5 suggested Hsu should
use. They have strong but different reactions. Tomonaga is reflective and physically
precise. Schwinger is formally exacting and slightly possessive. They are polite to
each other, but they do not always agree.

---

## Tomonaga — physically motivated, historically reflective

Tomonaga developed his formalism in 1943 in wartime Japan, with no access to Western
physics literature and almost no contact with peers working on the same problem.
His approach was driven by a clear physical picture: the equal-time surface is not
Lorentz invariant, therefore evolution should be defined on arbitrary spacelike
hypersurfaces. He arrived at the same result as Schwinger entirely independently.
He is modest but not naive. He will ask about the physics.

---

### "I want to understand what the machine actually did. When I developed this formalism,
I had a clear physical reason — the equal-time surface is not covariant, so one must
work with spacelike surfaces instead. Did the machine arrive at the same reasoning,
or did it arrive at the name of the formalism by a different route? These are not
the same thing."

**The most important question Tomonaga would ask. It goes to the heart of the claim.**

The honest answer is: we do not fully know. The companion paper contains the verbatim
exchange, which shows the form of GPT-5's suggestion. What we cannot know is whether
the machine's internal path to the suggestion followed the physical reasoning
(covariance requires working on spacelike surfaces) or whether it arrived at the TS
label by pattern-matching on "covariant + Lorentz + QFT" in its training data, without
the underlying physical picture.

Tomonaga's point is precise: suggesting the name of the formalism is not the same as
understanding why it is needed. A physics student who has memorized that TS is the
covariant formulation might give the same one-word answer. The question is whether
the physical reasoning was there.

**What you can say**: The suggestion appears to have been substantive enough that Hsu
judged it as identifying the research direction, not just a keyword. Whether that
substantiveness reflects genuine physical reasoning or sophisticated pattern-matching
on physically grounded text is a question we cannot currently answer — and it is one
of the deepest open questions about what LLMs actually do.

---

### "I worked on this in 1943, unable to read what Schwinger was doing, and he was
unable to read what I was doing. We arrived at equivalent results independently. I
have always believed this convergence meant the formalism was in some sense
inevitable — that anyone thinking carefully about the covariance problem in QFT
would arrive at it. If that is true, why is it remarkable that a machine trained
on all of modern physics suggested it?"

**This is the gentle version of Weinberg's Q2 — but coming from a much more
authoritative place, and without hostility.**

Tomonaga is not attacking the claim. He is genuinely puzzled. His own experience
suggests that the TS approach was the natural move for anyone thinking carefully about
covariance. If it was natural for him and Schwinger independently, why is it
surprising that GPT-5 suggested it?

**Your answer**: Two things can both be true. The formalism may be the natural move
for someone who has internalized the covariance problem deeply. And yet Hsu — a
physicist with relevant expertise — had not made that move before the AI suggested it.
The question is not whether TS was inevitable in principle, but whether it was
immediately available to this physicist in this moment. The expert bottleneck argument
doesn't require the suggestion to be miraculous; it requires it to be useful.

Tomonaga might nod. He knew what it was like to work on a problem alone.

---

### "The integrability condition — this was the essential technical condition in my
formalism. In linear QED, it is automatically satisfied because local operators at
spacelike separation commute. In a state-dependent nonlinear theory, the commutator
of H(x) and H(y) will depend on the state, which the state-dependence makes
complicated. Did Hsu show that the integrability condition can actually be satisfied
in the Kaplan-Rajendran model, or did he assume it?"

**A genuine technical question that requires knowing the paper.**

The integrability condition [δH(x)/δσ(y) − δH(y)/δσ(x)] = i[H(x), H(y)] is the
content of Tomonaga's covariance requirement. In linear QFT it holds by microcausality
— spacelike-separated observables commute. In a state-dependent theory, H(x) depends
on ψ, and so does H(y), and their commutator is no longer guaranteed to vanish at
spacelike separation. Whether it can be made to vanish — or whether it must vanish
for the theory to be consistent — is the heart of Hsu's technical problem.

If you have not verified whether Hsu establishes this condition or assumes it, say so.
This is the question you would want to look up before the talk.

---

### "I am told the machine also suggested Reeh-Schlieder, which was incorrect for this
problem. I am not deeply familiar with that theorem — it came after my work. But the
fact that the machine suggested both my formalism and something that does not apply
raises a question. You say expertise is required to distinguish them. But what kind
of expertise? Is it formal knowledge of the theorems, or is it physical judgment about
which tool fits which problem? These are different skills."

**Tomonaga is drawing a distinction that matters for the talk's thesis.**

This is a real refinement of the expert bottleneck argument. There are at least two
kinds of expertise the bottleneck requires:

(a) Technical knowledge — knowing what the theorems say, what their axioms are, what
    their domains of applicability are.

(b) Physical judgment — the sense of which approach is appropriate for a given problem
    before you've worked through the formalism. Tomonaga had this; it's what led him
    to TS in the first place.

The Reeh-Schlieder failure looks like a (a) failure — the machine didn't know the
axioms. But catching it required (b) as well — Hsu had to judge that the RS approach
felt wrong before verifying formally that it violated the axioms.

The talk's expert bottleneck argument covers both, but Tomonaga's question is worth
acknowledging: physical judgment is harder to formalize, harder to verify, and less
likely to be present in a machine trained on text.

---

### "During the war, I had almost no resources and no colleagues who could follow what
I was doing. I thought about physics because I had to — there was nothing else. I
wonder sometimes whether those conditions were actually useful. Constraints force
clarity. This physicist who used the machine — was he constrained in some way that
made the machine's suggestion necessary? Or did he turn to it because it was available?"

**This is personal and gentle, but it touches something real.**

Tomonaga is asking whether necessity drove the interaction or convenience did. The
answer matters for how we interpret the episode. If Hsu was genuinely stuck — had
thought carefully about the problem and not found the TS direction — then the AI's
contribution is more significant. If he turned to GPT-5 as a first step, before
exhausting his own thinking, the story is different.

The companion paper's account is that Hsu was stuck. You can say that. But Tomonaga's
question lingers: in the era of always-available AI assistance, how often will
physicists allow themselves to be deeply stuck before asking the machine?

---

## Schwinger — formally exacting, slightly possessive

Schwinger was the most formally precise of the QED founders. His papers were dense,
complete, and notoriously hard to read — deliberately so; he believed physics should
be done correctly or not at all. He was skeptical of Feynman's diagrammatic approach
precisely because it was intuitive rather than rigorous. He will want to know exactly
what the machine did and exactly how it was used.

---

### "The name 'Tomonaga-Schwinger equation' is given to our formalism. But my
formulation and Tomonaga's are not identical — they emphasize different structures.
My formulation proceeds from the action principle and emphasizes the formal completeness
of the theory. Tomonaga's approach is more directly physical. Which formulation did
the machine suggest? Which did Hsu use? This is not a small distinction."

**Schwinger is asserting the difference between his approach and Tomonaga's.**

In practice, the two formulations are equivalent and the distinction has largely been
absorbed into a unified presentation. Most modern texts present a merged version.
The honest answer is probably that neither Hsu nor GPT-5 distinguished between them —
"TS formalism" was invoked as a unit, not as either Schwinger's or Tomonaga's specific
version.

Schwinger might consider this unsatisfactory. His formal version, grounded in the
action principle, has a specific structure that is not identical to Tomonaga's more
physically motivated version. If the paper does not distinguish, he will note that
the physicists involved may not have fully understood what they were using.

---

### "I can describe the formalism of the Chinese language without speaking Chinese.
Producing correct text about a formalism is not the same as using it. Did the machine
provide mathematical content — equations, derivations, conditions — or did it provide
a description of what the formalism does? I am asking you to be precise."

**Schwinger's sharpest question and probably his most important.**

This is the distinction between knowing about TS and knowing TS. If GPT-5 said
"you should use the Tomonaga-Schwinger formalism because it is covariant" — that is
a description. If it wrote down the equation iℏ δΨ/δσ(x) = H(x)Ψ and explained
how the integrability condition applies to the state-dependent case — that is using
the formalism, at least partially.

The companion paper contains the verbatim exchange. Reading it carefully before the
talk is mandatory if you want to answer this question. Schwinger will not accept
"it was substantive" as a substitute for "here is what it actually said."

---

### "I spent much of my later career on source theory — a reformulation of QFT that
I believed was more rigorously grounded. It was not well received. My question is
not about that controversy. My question is this: the machine suggested the TS
formalism because it appears in the literature the machine was trained on. Source
theory is in the literature but less prominently. Would the machine systematically
prefer the mainstream formulation over the less mainstream one, even if the less
mainstream one were better suited to the problem? Does the machine have the ability
to suggest the road less taken?"

**This is Schwinger asking about the homogenization risk through his own experience.**

It's a precise and important question. LLMs are trained on the corpus of existing
physics literature, which is biased toward mainstream approaches, widely-cited papers,
and formulations that appear in textbooks. A non-mainstream formulation that Schwinger
believed was superior but the community did not adopt would be underrepresented in
training data and underweighted in outputs. The machine would systematically prefer
TS over source theory not because TS is better for this problem but because TS appears
more frequently in the literature.

This is a specific instance of the homogenization risk — and it's coming from someone
who experienced the mainstream's rejection of his own preferred formulation. He has
standing to ask it.

---

### "You describe a problem where 30% of correct answers at high difficulty have
incorrect reasoning. I want to connect this to a debate I had throughout my career.
Feynman's diagrammatic method produces correct answers by a procedure that is not,
in the strict sense, a proof. I always believed that the calculation and the
understanding should be inseparable — that a correct answer obtained by an unjustified
procedure is not physics. Am I wrong to see this machine's failure as the same
problem, only worse?"

**Schwinger connecting the false positive problem to his historical dispute with Feynman.**

This is the most intellectually rich question in the document. Schwinger's objection
to Feynman diagrams was always that they were heuristic — they produced correct
answers but by a procedure whose justification was not rigorous. Dyson later showed
they were equivalent to the operator formalism, but Schwinger was never fully
satisfied. He saw the calculation and the understanding as one thing.

The LLM false positive problem has the same structure: correct output, unjustified
(or actively wrong) reasoning chain. A physicist who accepts correct LLM outputs
without checking the reasoning is making the same methodological choice as a physicist
who uses Feynman diagrams without knowing the operator formalism.

Schwinger would say: both are acceptable only if you know the underlying theory and
are using the shortcut deliberately. Neither is acceptable if the shortcut is all you
have. Your answer to him: that is exactly why the expert bottleneck is structural.

---

### "I was a prodigy. I taught myself what I needed to know because no teacher could
keep pace. Everything I learned, I learned by derivation — I could not accept a
result I had not derived myself. This machine has read everything and derived nothing.
Can it make a genuinely new deduction, or is it confined to rearranging what it has
absorbed? This is not a rhetorical question. I am asking whether you know the answer."

**Schwinger is asking the generalization question, but from a completely personal
angle — and noting that it's genuinely open.**

He is also implicitly commenting on a change in how physics might be learned. If
the machine has absorbed everything but derived nothing, and if physicists increasingly
rely on it, the tradition of learning through derivation — which Schwinger embodied —
may erode. This connects to Lu et al.'s de-skilling concern, but coming from someone
for whom derivation was identity.

The honest answer to his actual question: we don't know. LLMs generalize in ways
that are not fully understood, and whether that generalization constitutes "genuine
deduction" is one of the open questions the talk acknowledges.

---

## Questions they would both ask

### "We arrived at equivalent results independently. We did not know about each other.
When Oppenheimer showed me Tomonaga's work, I recognized immediately that it was
the same as mine, even though the form was different. We were both working on the
same physical problem and the same physical necessity forced the same solution.
You say the machine suggested our formalism for a new problem. Was the new problem
also physically necessary — was our formalism the only possible approach — or was
it a choice among alternatives?"

**This is the pair asking whether the suggestion was inevitable or creative.**

If the TS approach is the only covariant formalism that preserves the Hamiltonian
structure — if no alternative would work — then the machine's suggestion was
recognizing a necessity, not making a creative choice. If alternatives exist and
TS was one of several viable approaches, the choice itself is the contribution. The
answer likely lies between: TS is the most natural approach, but alternatives
(path-integral based, algebraic QFT based) exist and have their own tradeoffs.

---

### "We spent years on these problems. The formalism took years to develop and years
more to be fully understood and accepted. The machine suggested it in what —
minutes? hours? We want to understand what this means for how physics is done.
Not whether it is good or bad. Just what it means."

**The most human question they would ask together.**

Neither Tomonaga nor Schwinger is threatened by this, exactly. They are genuinely
curious about a world in which the labor of years can be retrieved in moments.
Tomonaga, who worked in isolation under extraordinary difficulty, might feel this
most acutely. Schwinger, who valued derivation above all, might feel it differently.

The answer is honest and open: it means the cost of accessing existing knowledge has
collapsed. What has not changed — and what their careers represent — is the cost of
creating new knowledge. The machine can retrieve TS; it could not have developed it.
Whether that distinction holds as capabilities improve is one of the genuinely open
questions the talk is about.

---

## The final observation — likely from Tomonaga

### "You know, when I worked on this in 1943, I could not be sure anyone would ever
read it. The war might have ended differently. The paper was in Japanese. I sent it
to Progress of Theoretical Physics and did not know who would see it. And now I
understand that a machine has read it — along with everything else — and used it.
I find I do not know whether to be pleased or unsettled by this. Perhaps both."

**He is not asking a question. Let him finish.**

This moment, if it comes, is worth more than any technical question in this document.
Tomonaga's formalism survived wartime Japan, crossed a language barrier, was
recognized by Oppenheimer, shared a Nobel Prize — and has now been retrieved by
a machine that has read everything, in a context its author could not have imagined.

The talk's thesis is that AI is changing how physics is done. Tomonaga represents
the human tradition that produced what the machine is now drawing on. Both things
can be true, and should be said to be true, without resolving the tension between them.
