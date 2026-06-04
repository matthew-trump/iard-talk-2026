# Weinberg-Style Questions on Hsu's Paper
## The hardest room

A thought experiment: what would Weinberg ask?

The specific difficulty: Weinberg (1989, Annals of Physics) originated the nonlinear
QM framework Hsu is working in. He would walk into this talk with more authority over
the physics than almost anyone in the room. He would not be impressed by novelty
claims. He would ask the question that reveals whether the result means anything.

---

## Q1. "You're aware that nonlinear QM generically allows superluminal signaling. Does the TS formulation resolve that, or just move it around?"

**This is probably question one, and it's lethal if you can't answer it.**

Gisin (1990) showed that Weinberg's own 1989 nonlinear QM formalism allowed faster-
than-light signaling via entangled states — you can use the state-dependence of H to
transmit information nonlocally. This is the deepest consistency problem for nonlinear
QM, and it's been known for 35 years. Weinberg was aware of it. The Kaplan-Rajendran
retarded model is specifically designed to avoid it by making the nonlinearity retarded
(causal). But the question is whether the TS covariant formulation, as Hsu develops
it, inherits this fix or needs to re-establish causality separately.

**You probably cannot answer this in full.** What you can say: the signaling problem
is what motivated Kaplan-Rajendran's specific model choice, and Hsu's covariance result
applies to that class of models. Whether TS formulation adds new signaling channels or
forecloses them is a question for the paper and its follow-on work.

**Why Weinberg would ask it**: because if the covariant formulation reintroduces
superluminal signaling that the retarded model was designed to avoid, the whole
construction is physically inconsistent. Covariance without causality is not progress.

---

## Q2. "The TS formalism is in my textbook. What exactly did the machine contribute that a competent graduate student couldn't have contributed?"

**The most direct challenge to the novelty claim — and it's fair.**

Weinberg's *Quantum Theory of Fields*, Volume 1, Chapter 8 contains a careful
pedagogical treatment of the Tomonaga-Schwinger equation and the integrability
condition. This is not obscure material. TS is standard relativistic QFT. The
question is whether GPT-5 made a connection that required genuine synthesis, or
whether it retrieved a standard technique and suggested it, which is something a
graduate student assigned to the problem might also do.

**The honest answer**: We don't know the counterfactual. Hsu — who is himself an
expert — had not made this connection. Whether a well-assigned graduate student would
have made it in an afternoon or in a year is genuinely unclear. The companion paper
contains the verbatim exchange, which shows the form and depth of GPT-5's suggestion.
That's the evidence. The novelty claim rests on Hsu's own judgment that he was stuck
before the suggestion and could proceed after it.

**What you cannot say**: that TS was an obscure or surprising choice. It wasn't. The
claim is about the specific application to state-dependent nonlinear QM, not about TS
itself.

---

## Q3. "The machine suggested Reeh-Schlieder and was wrong. It suggested TS and was right. On what basis do you distinguish 'the AI contributed a research direction' from 'the AI produced two guesses and the physicist picked the right one'?"

**This is the most philosophically acute question Weinberg would ask — and it has no clean answer.**

The structure of the episode: one correct suggestion, one incorrect suggestion, an
expert who could distinguish them. From the outside, this is consistent with two
interpretations:

(a) The AI identified a genuine connection between covariant formalism and the
    nonlinear QM covariance problem — a connection that required understanding both
    fields. The Reeh-Schlieder error was a separate failure.

(b) The AI pattern-matched on keywords from the prompt — 'covariant,' 'Lorentz,'
    'field theory' → TS; 'nonlocal,' 'QFT,' 'vacuum' → Reeh-Schlieder — and produced
    two plausible-sounding suggestions. One happened to be correct. The physicist
    selected it.

Weinberg would note that interpretation (b) is consistent with everything we observe,
and that interpretation (a) requires a claim about the AI's internal process that we
cannot verify. This is a genuinely hard epistemological problem. The Reeh-Schlieder
failure is actually evidence *for* interpretation (b): the machine connected
'nonlocal' to RS without apparently understanding that RS requires the Wightman axioms,
which the model doesn't satisfy. That's keyword matching, not physics.

**Your best answer**: You can't rule out (b). The argument from the talk's perspective
is that interpretation (b) is *still useful* — a suggestion generator that produces
physically relevant candidates, even by pattern matching, is useful if and only if the
expert can filter them. The question of whether the machine "understood" is separate
from whether the output was productive. But you should acknowledge that Weinberg's
challenge is correct: we don't have access to the machine's internal process, and the
external evidence is consistent with both readings.

---

## Q4. "What does this predict? Has anyone tested nonlinear QM since my 1989 papers, and does this covariant formulation change what's testable?"

**Weinberg was a phenomenologist at heart. He always asked this.**

His 1989 papers on nonlinear QM were motivated by the question: can we test the
linearity of QM experimentally? The answer at the time was that precision spectroscopy
of atoms and ions could set bounds. (Bollinger et al. 1989 set bounds of order 10⁻²⁷
on the nonlinearity parameter shortly after Weinberg's papers.) Weinberg may have
left the program partly because the experimental bounds became very tight and the
theoretical consistency issues (signaling) were serious.

The question is: does Hsu's covariant formulation open new experimental avenues, or
is it a formal result that doesn't change what's observable? If it's purely formal,
Weinberg would consider it a theoretical exercise, not physics in the full sense.

**You cannot answer this fully.** Deflect honestly: "The paper addresses the formal
covariance question. Whether it changes the experimental program for testing nonlinear
QM is a question I'd want to look at more carefully before claiming an answer."

---

## Q5. "You're telling me a physicist needed a machine to suggest the Tomonaga-Schwinger equation. What does that tell us about how we're training physicists?"

**This is the question with the sharpest edge — and it's not really about AI.**

Weinberg cared deeply about physics education and the culture of the field. He wrote
textbooks precisely because he thought the pedagogical tradition was important. If a
physicist working on a covariance problem in QFT didn't immediately reach for TS, that
might say something about the state of QFT education as much as it says something
about AI.

**This is a trap.** Do not defend Hsu's physics education. The right response:

The interesting thing is not that Hsu didn't immediately reach for TS — experts get
stuck on their own framing all the time, and the narrow focus that makes someone an
expert in one area is exactly what causes them to miss obvious moves from adjacent
areas. That's Lichtman's chess-opening point: human training causes detours. The
question is whether this is a failure of physics education or a structural feature of
how expertise works. Probably the latter.

---

## Q6. "If many groups now use the same machine to identify covariant formulations of their nonlinear models, and the machine makes the same suggestion to all of them, what has happened to the diversity of research directions in the field?"

**This is the question Weinberg would ask if he were thinking about the field, not just the paper.**

He was historically aware that physics progresses through a diversity of approaches —
many wrong ones, some right — and that the wrong ones are often not recognized as
wrong until much later. If a single AI system is suggesting research directions to
many groups simultaneously, and the system has systematic biases (toward techniques
well-represented in its training data, toward formally elegant approaches, toward
published positive results), the field's search space narrows in a correlated way.

This is the homogenization risk from the talk's §4/§5. It maps directly onto
Weinberg's sense of how physics actually makes progress — not by everyone following
the same program, but by a plurality of bets.

**Your answer**: This is the talk's most important concern about the long run. For
a single paper, it's not the issue. For a field, it could be. The worry is not
that AI suggests wrong directions — experts catch those. The worry is that AI
systematically deprioritizes directions it can't suggest, which are precisely the
directions most likely to require genuinely new ideas.

---

## Q7. "Can this approach help with the real problem?"

**The hardest question, and the one Weinberg might save for last.**

By "the real problem," Weinberg would mean the measurement problem, or the meaning
of the quantum state, or whatever he considered the genuine open question in
foundations — the one he wrote about in the 2017 *New York Review of Books* piece
("The Trouble with Quantum Mechanics"). He was not satisfied with the Copenhagen
interpretation and remained genuinely puzzled by the foundations late in his career.

The question is whether AI assistance with formal calculations and cross-subfield
synthesis can help with problems where we don't even know what the right formulation
is — where the question itself needs to be invented, not just the answer. Hsu's
paper is an application of an existing formalism to a well-posed problem. The hardest
problems in physics foundations are not well-posed. Can AI help there?

**Your honest answer**: Probably not in its current form. The Botvinick/Gershman
argument from Binz et al. is directly relevant: AI trained on the existing record
cannot generate the question-evolution that comes from changes in human understanding
and values. Weinberg's "trouble with QM" is the kind of problem where we might need
a new concept, not a better application of an old one. LLMs are strong at the latter.
Whether they can contribute to the former is genuinely unknown and genuinely important.

---

## Notes on Weinberg's style

- He asked the question that implied a criticism without stating it as one.
  ("You're aware that..." is more devastating than "But what about...")
- He did not accept "that's an interesting question" as an answer.
- He was willing to be wrong and to say so. He would respect an honest "I don't know."
- He disliked evasion more than error.
- He distinguished between what a result *shows* and what a result *suggests* —
  and was not satisfied with the latter being presented as the former.
- If you didn't know the answer, the right move was to say so directly, then say
  what you *do* know and where the boundary is. Bluffing was worse than ignorance.

**The one thing he would respect**: that the talk is honest about what Hsu's result
shows and doesn't overstate the AI contribution. The claim in the talk is carefully
scoped — one instance, one research direction, expert oversight throughout. If you
hold that line under pressure, Weinberg-style questioning is answerable.

[June 3, 2026]
Keum and Warey, "Bracketing Inference with Uncertainty Quantification: A Reliability Pipeline for Neural Aerodynamic Surrogates" https://doi.org/10.21203/rs.3.rs-9775673/v1 on Data-driven surrogates for computational fluid dynamics (CFD) https://www.researchsquare.com/article/rs-9775673/v1