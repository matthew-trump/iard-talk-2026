# §2 Draft — A Case Study: The Hsu Paper
## Target: 12–15 minutes

*This is a working draft for speaker revision. The voice is close but not final —
adjust phrasing, emphasis, and technical depth to match your delivery style.
Delivery notes appear in [brackets].*

---

### Opening move

I want to start with a specific paper.

*Physics Letters B*, volume 872, 2026. Author: Stephen Hsu, professor of theoretical
physics at Michigan State. Title: "Relativistic covariance and nonlinear quantum
mechanics: Tomonaga-Schwinger analysis." Published after standard peer review. Four
pages. No asterisks, no caveats in the abstract. It looks, from the outside, like a
normal theoretical physics paper.

The Acknowledgements read, in full: *"The author used AI models GPT-5, Gemini 2.5 Pro,
and Qwen-Max in the preparation of this manuscript, to check results, format latex,
and explore related work."*

[Pause.]

That acknowledgement is accurate. It is also, I would argue, significantly incomplete.
And the gap between what the acknowledgement says and what actually happened is, in
a small way, the whole subject of this talk.

---

### The physics

Before I tell you what happened, let me tell you what the paper is about — because
the physics matters.

The question is an old one in quantum foundations: can you modify quantum mechanics
to be nonlinear? Linear superposition is exact as far as we know experimentally, but
theorists have long asked whether small nonlinear corrections are possible in
principle — modifications where the Hamiltonian depends not just on the state vector
but on expectation values, or on the global wave functional. Weinberg wrote down
a careful class of such theories in 1989. Polchinski showed in 1991 that even gentle
nonlinearity causes problems — in particular, it allows superluminal signaling via
entangled pairs. That's a fatal objection in a relativistic theory.

Hsu had worked on related problems. In a 2014 paper with Ho, he showed that
instantaneous entanglement generation appears under certain nonlinear evolutions in
the non-relativistic case. But the full relativistic treatment — the question of
whether nonlinear QM can survive contact with special relativity at the QFT level —
had not been settled with the right tools.

The right tools, it turns out, are the Tomonaga-Schwinger formalism. You may know it
from axiomatic QFT. The idea is to define quantum evolution not with respect to a
preferred time coordinate but with respect to arbitrary spacelike hypersurfaces —
so the evolution operator maps states from one spacelike slice to another. For a
covariant theory, the physics cannot depend on which foliation you choose. That
independence condition — that you get the same answer regardless of how you slice
spacetime — is the TS integrability condition.

What Hsu shows is that state-dependent nonlinear modifications to QFT generically
fail this condition. The key mechanism: state-dependent evolution doesn't preserve
microcausality — the commutativity of spacelike-separated operators — once you
propagate forward from an initial slice. Three specific models are analyzed: Weinberg's
local form, a nonlocal generalization, and a more recent retarded model by Kaplan and
Rajendran. All three fail. The conclusion is a no-go theorem: under TS integrability
with microcausality, admissible deterministic state-dependent modifications collapse
to the linear case.

That's the result. It's a genuine contribution to the foundations of QFT. The referee
evidently thought so — asked for a non-trivial extension not in the original
submission, which Hsu provided.

---

### How it actually happened

Now here is what the acknowledgement doesn't tell you.

Hsu published a companion paper in December 2025, titled "Theoretical Physics with
Generative AI." It includes verbatim transcripts of his exchanges with GPT-5. I want
to walk through what happened, because the sequence matters.

Hsu was probing GPT-5's understanding of his own 2014 paper. A reasonable thing to
do — use your own prior work as a test of the model's grasp of specialized content.
He asked GPT-5 to compare nonlinearity in non-relativistic QM with what happens when
you impose the full QFT structure, where the nonlinearity involves the entire wave
functional across potentially infinite spacelike-separated modes.

GPT-5 gave a technically correct answer. And then it volunteered something Hsu had
not asked for. I'll read it exactly as it appears in the transcript:

> *"If you want, I can sketch the Tomonaga-Schwinger version of this — evolution by
> spacelike hypersurfaces — to show explicitly why a hypersurface-local generator that
> depends nonlinearly on the global state cannot remain foliation-independent without
> collapsing back to linear dynamics."*

Hsu said yes.

GPT-5 then generated the TS setup, derived the integrability condition including
the Fréchet derivative cross-terms that state-dependence requires, and wrote down
the key operator constraint. Hsu's assessment in the companion paper:

> *"This exchange is remarkable because GPT-5 proposes a novel research direction."*

The phrase "de novo" appears in the methodology paper's abstract. The research
direction — apply the TS formalism to constrain nonlinear QM — was not in any prior
paper that Hsu or I can find. GPT-5 suggested it unprompted.

The equations from that exchange form, in Hsu's words, "the core of the resulting
paper."

[Pause. Let this land.]

I want to be careful about what I'm claiming here, and I'll be more precise about
that shortly. But take a moment to appreciate what just happened: a published,
peer-reviewed result in a legitimate physics journal, in an area of active theoretical
interest, where the originating idea — the conceptual move that made the paper
possible — was proposed not by the human physicist, but by a language model.

---

### The workflow

Now let me tell you how Hsu actually worked, because the methodology is as important
as the result.

Hsu did not take GPT-5's output at face value. He used what he calls a
Generate-Verify protocol. One model instance generates a research step or
calculation. A separate model instance — given no context about what the first one
produced — checks it for errors. The Verifier prompt is minimal but direct:
*"You are a world class theoretical physicist. Check the following for errors.
Review each equation and reasoning step. Identify all problems and summarize your
findings."*

Hsu ran multiple models: GPT-5 and Gemini 2.5 Pro and Qwen-Max as primary generators
and verifiers; DeepSeek V3.1 and Grok-4 as final checks.

His analogy for what this is like:

> *"Using LLMs as noisy Verifiers of a research step is not very different, in my
> experience, from going down the hall to explain the new idea to a colleague. Even
> an expert colleague will not render a completely reliable opinion; however the
> resulting discussion is useful to discover problems and to calibrate conviction levels."*

I find this analogy precise. The colleague analogy isn't flattering to the LLMs — it
acknowledges they're noisy, unreliable, sometimes wrong. But it correctly identifies
the function: verification through independent engagement, not through formal proof.

One asymmetry that matters: **convergent positive Verifier responses are a good signal
for correctness. Lack of convergence is a reliable signal that something is wrong.**
The asymmetry is useful. When multiple independent model instances agree that a step
is correct, that's weak evidence for correctness. When they can't agree, that's strong
evidence to slow down.

---

### Where the AI failed

This is as important as the success.

During the research, multiple LLMs made a consistent suggestion: use results from
axiomatic QFT — specifically the Reeh-Schlieder theorem and the "split property" —
to prove directly that the TS integrability conditions must be violated in the
presence of nonlinear terms.

These suggestions were wrong.

Hsu:

> *"I expended a significant amount of effort to determine this, given that my
> background is not in axiomatic field theory."*

Let me be precise about what kind of error this was. The models were not confusing
the Reeh-Schlieder theorem with something else. They correctly identified the theorem,
correctly knew it was about operator algebras in relativistic QFT, and incorrectly
concluded it was applicable to the problem at hand. They drew a plausible connection
between two distant parts of the literature — axiomatic QFT and nonlinear QM — and
the connection was wrong.

Hsu's diagnosis:

> *"Model expertise extends across the entire literature of our subject, and hence
> they are fully capable of introducing plausible-sounding applications of techniques
> from distant subfields. These are often the most difficult confabulations to detect!"*

Notice the structure of this failure: it is systematically enabled by the same thing
that made GPT-5's TS suggestion possible. Broad exposure to the literature enables
both genuine cross-domain insight and plausible cross-domain confabulation. The model
doesn't know which is which. That's not a limitation that goes away with more
training data — it may get worse.

The Verifier methodology helped here. Multiple Verifier instances couldn't converge
on whether the Reeh-Schlieder approach was correct — and that failure to converge was
the signal. But resolving the question still required Hsu to work through axiomatic
QFT in enough depth to understand the theorem's limitations for himself.

This is the expert bottleneck in action, and I'll return to it in §4.

---

### Peer review

One more piece of the story.

The paper went through peer review. The referee — not knowing or at least not
commenting on the AI involvement — asked for the analysis to be extended to the
Kaplan-Rajendran retarded nonlinearity model. This is a more recent proposal, not
in the original submission, and the retarded structure makes the causal analysis
more delicate.

GPT-5 generated the correct calculation. The key issue is causality: the retarded
kernel and commutator terms have support on overlapping past light cones — J-minus
of x and J-minus of y — and the argument is that even retarded causal dependence
fails TS integrability because spacelike-separated points share a nonempty causal
past. Other models initially got the causal structure wrong but converged to GPT-5's
result when used as Verifiers.

I mention this because it shows the AI contribution persisting through the revision
phase, not just in the initial ideation. The referee asked a genuine technical
question. The AI helped answer it.

---

### What to claim, and what not to claim

Let me now be precise about what this paper does and does not establish, because
the tendency in both directions — to oversell and to dismiss — is real.

**What the Hsu paper establishes**:

A published, peer-reviewed result in a reputable physics journal. The main research
direction — use the TS formalism to constrain nonlinear QM — was proposed de novo by
GPT-5, unprompted, in the course of a conversation. The key equations were generated
in that exchange and form the core of the paper. The Generate-Verify workflow is
described in detail and is in principle replicable. LLM cross-subfield confabulation
caused significant wasted effort. Expert human oversight was essential throughout.

**What the Hsu paper does not establish**:

That GPT-5 understands physics in the way a physicist does. That this is replicable
without deep expert oversight. That a non-expert could have done what Hsu did. That
it demonstrates autonomous physics research. That this is a typical result rather
than an exceptional one.

Hsu's own summary is the right one to end on:

> *"Research with an LLM might be compared to collaboration with a brilliant but
> unreliable human genius who is capable of deep insights but also of errors both
> simple and profound."*

That phrase — brilliant but unreliable — is not false modesty. It is a precise
description of what the evidence shows.

---

### The disclosure gap

One last observation before we move on.

The Acknowledgements say GPT-5 was used to "check results, format latex, and explore
related work." The companion paper says the originating conjecture of the paper came
from a GPT-5 exchange. These are both true. They describe different things.

Are current norms for disclosing AI contributions in physics publications adequate?
If the conceptual move that made a paper possible came from a language model —
even with full human verification and full human responsibility — what does the
acknowledgement section owe the reader?

Hsu takes full responsibility. He does not attribute co-authorship to GPT-5.
I think that's correct. But the gap between "used to check results and format latex"
and "proposed the main research direction" is a gap the community will have to
address as these cases multiply. Right now, we have one published case willing to
describe in detail what happened. There are almost certainly others who aren't saying.

[Transition to §3:]
The question is whether the Hsu paper is a data point or a trend. To answer that, I
need to show you what else is happening — and in particular, what's happening in a
domain that moves faster than theoretical physics and is close enough in rigor to
function as a leading indicator.
