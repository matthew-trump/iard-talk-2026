# Anticipated Q&A — Hsu's Paper
## For a relativistic QFT / covariant formalism audience

The audience will be expert in the physics but unfamiliar with the AI methodology.
Questions will come from two directions: probing the physics result on its own merits,
and probing the AI contribution skeptically through the physics lens.

You are not obligated to answer every question — deflecting to "I'd need to look at
the derivation more carefully" or "Hsu discusses this in the companion paper" is
entirely appropriate for a paper that isn't your own.

---

## Category 1: The physics — questions they can evaluate independently

---

### Q1. "What exactly was the obstacle to Lorentz covariance in nonlinear QM, and why does TS fix it?"

**This is the first question, nearly guaranteed.**

In standard QM, state evolution on an equal-time surface is frame-dependent, but this
doesn't matter because the dynamics are linear — you get the same S-matrix regardless
of foliation. In state-dependent nonlinear QM (ψ̇ = H(ψ)ψ), the Hamiltonian itself
depends on which state you're evolving, so the frame-dependence of the surface choice
enters the physics directly. The Tomonaga-Schwinger formalism defines covariant
evolution along arbitrary spacelike hypersurfaces and enforces consistency via the
integrability condition — it's Lorentz covariant by construction. In the linear case,
the TS integrability condition is automatically satisfied. In the nonlinear case,
satisfying it is the non-trivial constraint the paper addresses.

**Likely follow-up**: "What does the integrability condition look like explicitly for
a state-dependent H?" This is getting into the derivation itself. Deflect if you
haven't worked through it: "That's Hsu's calculation — I can point you to the paper."

---

### Q2. "Was TS actually the right tool, or could other covariant formalisms have worked?"

Path integrals on arbitrary backgrounds, algebraic QFT (Haag-Kastler), covariant
Hamiltonian methods — all are available. TS is particularly natural here because it
preserves the Hamiltonian structure while achieving covariance. Path integral
approaches would require specifying the measure for a state-dependent theory, which
introduces its own complications. Whether TS is uniquely correct or one of several
viable approaches is an open question you can honestly acknowledge.

---

### Q3. "Is the nonlinearity renormalizable, or is this purely a formal result?"

Weinberg-type nonlinear QM has known problems at loop level. The Kaplan-Rajendran
retarded model is designed to avoid specific no-go theorems. Renormalizability is a
separate question the covariance paper doesn't address.

**Deflect cleanly**: "The paper addresses the covariance question; renormalizability
is presumably open and would be a natural extension."

---

### Q4. "What happened with the Reeh-Schlieder suggestion — why was it wrong?"

**Worth being able to answer fully — it's the most interesting moment for a QFT audience.**

GPT-5 made two suggestions. The TS one was correct. The Reeh-Schlieder suggestion was
not. RS says that local operations on the vacuum can generate any state in the full
Hilbert space — it's a theorem about vacuum structure in algebraic QFT. The LLM
apparently connected this to the nonlinear QM problem, possibly because nonlinearity
can induce nonlocal correlations and RS is a nonlocality theorem. But RS lives in the
Wightman/AQFT framework with specific axioms that state-dependent nonlinear QM doesn't
satisfy. The cross-subfield connection was formally plausible but physically wrong.

Hsu recognized this immediately because he knows both fields. This is not a minor
detail — it's the structural argument for why expert oversight is not optional. Remove
the expert, and the Reeh-Schlieder suggestion would be indistinguishable in the output
from the TS suggestion.

---

## Category 2: The AI contribution — they'll probe its actual substance

---

### Q5. "What did GPT-5 actually say? Was it 'try TS' or something more specific?"

**The most pressing question. You should be able to answer this.**

The companion methodology paper (Hsu 2025, arXiv) contains the verbatim exchange.
The suggestion was substantive enough that Hsu judged it as identifying the main
research direction — not a one-line keyword hint. The companion paper apparently
shows GPT-5 sketching at least partial reasoning for why TS resolves the covariance
problem, not merely naming the formalism.

**Recommendation**: Reread that exchange before the talk. The audience will want to
know the form of the suggestion, not just that it happened.

---

### Q6. "Could a well-read postdoc have made the same suggestion after a 10-minute conversation?"

**The sharpest skeptical question and the hardest to answer honestly.**

Possibly. We don't know — the counterfactual wasn't run. What we do know is that Hsu,
who is himself an expert in both relativistic QFT and nonlinear QM, had not reached
this direction independently before turning to GPT-5. Whether another expert would
have immediately said "use TS" when asked "how do you make a state-dependent H
covariant" is genuinely uncertain.

The parallel worth invoking: in Co-Scientist, the AMR hypothesis took a decade for
domain experts to establish experimentally, and two days for the AI to propose. The
question isn't whether a human *could* reach it — it's whether they *did*, in this
specific instance, with this specific researcher.

---

### Q7. "Is this reproducible? If I give the same prompt to GPT-5 today, do I get the same suggestion?"

**Excellent question. The honest answer is probably no — not reliably.**

Binz et al. (PNAS, 2025) document that GPT-4 results from one study could not be
reproduced three months later after a model update; some benchmark scores decreased.
GPT-5 is a black box with no guaranteed version pinning. The Hsu result is not an
experiment that can be repeated with controlled conditions.

This is a genuine methodological concern for the field. Open-source models (which can
be pinned to a specific version) partially address it, but no physics LLM paper has
yet met that standard.

---

### Q8. "Why isn't GPT-5 a co-author?"

**The field hasn't settled this.** The norms are actively being worked out. Hsu
acknowledged AI use, but the PLB paper's acknowledgement described the AI's role as
more peripheral than the companion paper reveals — the companion paper was a separate
and subsequent disclosure. This gap between what was stated in the published paper and
what the companion paper revealed is itself a data point the community is grappling
with.

The most concrete reform proposal on the table: Marelli et al. (in Binz et al.)
recommend using the CRediT taxonomy to code AI contributions without granting
authorship, and publishing prompts as supplementary material.

---

## Category 3: Implications for their own work

---

### Q9. "Has anyone extended this? Is the TS approach to nonlinear QM now a research program?"

Know whether you can answer this before the talk. If you can't, say so directly — the
paper is recent enough that follow-on work may simply not exist yet.

---

### Q10. "What would this look like applied to [their specific subfield]?"

Someone will instantiate the question to quantum gravity, lattice gauge theory,
condensed matter, or whatever their own work is. You don't need to answer this
specifically — you can redirect: "That's exactly the question the community is starting
to ask" and point to the Lu et al. workflow taxonomy, which maps which stages of the
physics research workflow LLMs currently contribute to and where the gaps are.

---

## The question you most need to be ready for

---

### Q11. "So Hsu got lucky — the AI suggested two things, one was right and one was wrong, and he happened to have the expertise to know which. Is the lesson 'AI is useful' or 'AI is a random suggestion generator that occasionally hits'?"

**This is the steelman of the skeptical position and it is genuinely good.**

Your answer is the core thesis of the talk:

That's not luck — that's the architecture. The expert bottleneck is not a limitation
to be engineered away. It is the mechanism by which the system produces reliable
output. A suggestion generator that produces one correct hypothesis and one incorrect
hypothesis is useful *precisely and only if* the expert can distinguish them. Remove
the expert, and the output is not less useful — it becomes actively dangerous. The
fluency of a wrong LLM output is indistinguishable from the fluency of a correct one.

The quantitative version of this argument is in Robin (Ghareeb et al.): when the
expert architecture (literature-grounded agents) is replaced with raw LLM calls, 44.5%
of references in the output are fabricated — and 0% with the architecture in place.
The 44.5% is not an argument against using LLMs. It's an argument for why the expert
(or expert-designed system) is structural, not optional.

---

## Deflection phrases worth having ready

- "That's in the companion methodology paper — I can send you the arXiv link."
- "The paper addresses the covariance question; that's a natural extension."
- "The field is actively working out those norms."
- "The counterfactual wasn't run, which is one of the genuine open questions."
- "My argument doesn't require the result to generalize — it requires us to take
  this instance seriously as evidence that needs to be explained."
