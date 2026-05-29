# §3 Draft — Broader Landscape: LLMs in Physics and Math
## Target: 10–12 minutes

*Working draft for speaker revision. Delivery notes in [brackets].
This section's job is to show Hsu is not an isolated anomaly — and to give
the audience a framework for thinking about the range of evidence,
not a tour of every paper. Organize by structural pattern, not by paper.*

---

[No new slide needed to open. Carry the momentum directly out of §2.]

The question this section answers is simple: is the Hsu paper a data point, or is
it a trend?

To answer that, I want to introduce a framework — and then show you what fits into it.

---

### The framework: where in the research cycle does AI help?

A group of physicists and ML researchers at the Max Planck Institute for Quantum
Optics and ETH Zürich — Lu et al., a 2026 preprint — broke the theoretical
physics research workflow into stages. The taxonomy is useful and
I'll use it throughout:

[Slide: a simple vertical list or flow diagram]

> **Stage 1**: Literature review and problem identification  
> **Stage 2**: Hypothesis formulation and model building  
> **Stage 3**: Analytical derivation and computation  
> **Stage 4**: Simulation and computational experiment  
> **Stage 5**: Analysis and interpretation of results  
> **Stage 6**: Communication — writing up, peer review

Where do documented LLM contributions live on this list?

Most are in stages 1 and 3. Literature synthesis and calculation execution — the
two ends of the derivation sandwich. Stage 2 is where the Hsu paper is most
remarkable: the TS framework suggestion is hypothesis formulation. That is the
hardest stage, and it is where the one published physics case sits.

Keep this taxonomy in mind. What I'm about to show you fills in stage 3 with
real numbers, and stages 1 and 2 with evidence from a related field.

---

### Stage 3: Calculation execution

[New slide: "87.5 / 100"]

Pan et al. — published last year in *Communications Physics*, Cornell, Google Research,
Harvard, Google DeepMind — tested GPT-4 on Hartree-Fock mean-field theory.

If you work in condensed matter, you know what Hartree-Fock is. For the rest of the
room: it's the workhorse approximation method. It replaces a many-body interaction
with a mean field, separates the problem into a tractable analytic piece and a
numerical self-consistency equation. Doing it correctly for an arbitrary system
requires graduate-level knowledge. In practice, it takes years to learn to do
reliably. Over six thousand condensed matter arXiv papers reference it in their
abstracts in the past decade.

Pan et al. built what they call an HF template — a multi-step prompt structure that
decomposes the calculation into eleven sub-tasks, written in natural language, with
placeholders for the system-specific information. Each step's output was checked by
a human expert before becoming input to the next step.

They tested this on fifteen real papers from APS journals spanning a decade of
condensed matter research.

The result: GPT-4 scored **87.5 out of 100** across all rubric layers and all
fifteen papers. Mathematical rigor — the accuracy of the equations themselves —
consistently **above 95**. It correctly derived the final Hartree-Fock Hamiltonian
in **13 of 15** papers when intermediate steps were corrected along the way.

One more detail I find striking: as a byproduct, GPT-4 identified typographical errors
in published papers. It was computing intermediate steps the published papers didn't
show, and occasionally found the printed answer inconsistent with a correct derivation.

[Pause.]

This is not performance on a benchmark. This is execution of a core research tool
on real publications. And GPT-4's training cutoff was September 2021. The corpus
includes papers both before and after that date; performance was flat across the
cutoff. The model was not recognizing old problems — it was doing the derivations.

Now, notice what Pan et al. are and are not claiming. The framework — the HF template,
the decomposition into eleven sub-tasks, the judgment about which implicit conventions
to supply — was designed by expert condensed matter physicists. GPT-4 executes inside
the framework brilliantly. It did not design the framework.

The stage 3 capability is there. The stage 2 requirement — building the scaffold —
is still human.

---

### Stage 1: Literature synthesis and the limits of the unguided approach

The physics literature is not the only domain where this has been tested.

[New slide: brief header — "Multi-agent AI scientists, *Nature*, 2026"]

In the same week in May this year, *Nature* published two papers on multi-agent
AI systems applied to drug discovery. I'll take them briefly, because they
illustrate something important about stage 1 — literature synthesis — and its failure
modes.

The first is from FutureHouse: a system called Robin, applied to dry age-related
macular degeneration, the leading cause of blindness in the developed world. Robin
analyzed 551 papers in 30 minutes — a human equivalent of roughly 540 hours. It
proposed drug candidates ranked by a tournament among model instances, and handed
experimental execution to human researchers. The humans ran the experiments. Robin
received the raw data back and updated its hypotheses.

One of Robin's candidates — ripasudil, a ROCK inhibitor already approved for
glaucoma in Japan — produced a 1.89-fold increase in RPE cell phagocytosis activity.
An application to macular degeneration that had never previously been proposed. The
mechanism was in the literature: ROCK inhibition enhances phagocytosis; phagocytic
dysfunction is a feature of dAMD. Robin connected them. No human had.

The second is Co-Scientist, from Google: given the question of how a class of mobile
genetic elements carrying antibiotic resistance genes achieves broad host range across
bacterial species, Co-Scientist — given minimal background — proposed, within two
days, the same mechanism that a separate research group had been investigating for
approximately a decade and was simultaneously publishing.

Two days. A decade.

---

### What makes these systems work — and the number that matters

The reason Robin works is not that it uses a more powerful LLM. It is that it uses
a literature-grounded retrieval architecture: two specialized agents that verify
claims against real papers before they enter the reasoning pipeline.

Here is the number that makes this concrete.

When the literature agents were replaced by raw calls to o4-mini — one of the most
capable models currently available — **44.5% of the references in the drug candidate
reports were hallucinated**. Citations that do not exist.

With the full Robin architecture: **zero percent**.

I am not citing this number to criticize frontier LLMs. I am citing it because it
quantifies something the Hsu case showed qualitatively: an unguided, unverified LLM
operating at research level is producing fabricated content at a rate that would
make any physicist's results unreliable. The expert bottleneck — in Robin's case,
the literature retrieval agents; in Hsu's case, the physicist himself — is not a
nice-to-have. It is the difference between a tool that works and one that appears
to work.

---

### The characteristic failure pattern

Now let me return to the Lu et al. paper, because it contains the most important
analytical finding in any of these sources for understanding why the expert
bottleneck is structurally necessary.

When Lu et al. tested current LLMs on research-level physics problems — not textbook
problems, but the kinds of derivations that appear in real papers — they found a
consistent pattern. I want to read it exactly:

> *"Models correctly execute standard procedures — routine operator expansions,
> standard change-of-basis steps — but fail at the key non-standard step requiring
> genuine insight: discovering a novel proof technique, or recognizing a technically
> delicate prerequisite before the main argument can proceed."*

The failure is not random. It is not distributed uniformly across the calculation.
It clusters at the pivot point — the step that distinguishes a physicist's approach
from a textbook application. Everything before that step, and everything after it,
can often be executed correctly. The creative move that makes the whole derivation
possible is where the model fails.

This is interesting in two directions.

In one direction: it is consistent with the Hsu case, but from the opposite side.
GPT-5 succeeded in proposing the TS framework — which is exactly a non-standard step
requiring insight. That success happened in a *generative* context: GPT-5 was
suggesting what to try, not executing a derivation it had been handed. The
characteristic failure pattern is about execution of novel steps in an existing
derivation framework. The Hsu case is about proposal of a new framework entirely.
These are different cognitive demands, and the evidence for each is different.

In the other direction: it explains why the Pan et al. HF template works so well.
The HF template is specifically designed to eliminate the pivot point from GPT-4's
task. The human expert has already identified the non-standard conceptual step —
"use Wick's theorem here," "identify the order parameter structure there" — and
encoded it into the template structure. GPT-4 executes the standard procedures
around those pivots at near-expert level. That is what 87.5/100 measures.

---

### The Lu/Hsu tension

This brings me to a tension in the literature that is worth naming explicitly, because
it tells you where the field actually is.

Lu et al., writing in the same period as Hsu, conclude that current LLMs are
"inadequate for theoretical physics research" without specialized training and tooling.
Hsu, writing in the same period, published a peer-reviewed QFT paper in *Physics
Letters B* using general-purpose LLMs with no specialized training.

These are not contradictory. They are a description of a moving frontier with a
specific limiting factor.

Lu et al. are characterizing what happens when LLMs are deployed without expert
supervision — and their conclusion that this produces "large volumes of subtly
incorrect output" is entirely consistent with the 44.5% hallucination rate in the
Ghareeb paper and the Reeh-Schlieder episode in Hsu.

Hsu demonstrates what is possible with expert supervision and a structured workflow.

The resolution is the expert bottleneck. Hsu's deep familiarity with his 2014 paper
and with the TS formalism was what allowed him to recognize the GPT-5 suggestion
as novel and worth pursuing — and to catch the Reeh-Schlieder suggestion as
plausible but wrong. Without that expertise, the two suggestions are
indistinguishable in the output. Both are stated with confidence. Both involve real
concepts applied with apparent precision.

The Lu/Hsu pairing is more useful than either paper alone. Lu et al. tells you what
goes wrong without the expert. Hsu tells you what's possible with the expert. The
gap between those two cases is exactly what the expert bottleneck measures.

---

### Before we move on

I want to register one more observation before we leave this survey.

Three independent research groups — Hsu, Lu et al., and Pan et al. — working in
different institutions on different problems, arrived at the same structural
solution: multi-step workflows where an LLM generates a result, and either a human
expert or a separate model instance verifies it independently before the next step.
Hsu calls it Generate-Verify. Lu et al. call it the Deriver-Critic loop. Pan et al.
use sequential human correction.

Same principle. Different implementations. Convergent from independent directions.

In 2022, Lewkowycz et al. — the Minerva paper from Google — had already found a
simpler version of the same insight at the benchmark level. Generate multiple
independent solutions; select the most common answer. They called it majority voting.
Their framing: *"The truth is a Schelling point."* Correct answers cluster on a single
value; wrong answers distribute across many. The generate-and-verify instinct was
already visible in 2022, as a statistical property of correct computation. By 2025,
it had become a structured research methodology with a human expert closing the loop.

That convergence is itself a data point. It suggests these groups are discovering
something real about the structure of reliable LLM use in technical domains — not
because they talked to each other, but because the problem has a shape.

[Transition to §4:]

What I want to do now is give you a working model for evaluating all of this —
a physicist's map of what LLMs can and cannot do, and why the failures they
have are the failures that matter most.
