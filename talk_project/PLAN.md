# PLAN.md — Talk Outline
## "100 Years Since the Schrödinger Equation: Is AI Ready to Take Over Quantum Theory?"

*Evolving outline. Sections marked [STUB] need content; sections marked [POPULATED] have
working material. Update after each session.*

---

## Status

| Section | Title | Status | Draft | Est. time |
|---------|-------|--------|-------|-----------|
| §1 | Introduction: Two Timelines | POPULATED | drafts/section1_two_timelines.md | ~7 min |
| §2 | A Case Study: The Hsu Paper | POPULATED | drafts/section2_hsu_case_study.md | ~14–15 min |
| §3 | Broader Landscape: LLMs in Physics and Math | POPULATED | drafts/section3_broader_landscape.md | ~9–10 min |
| §4 | What LLMs Can and Cannot Do | POPULATED | drafts/section4_can_and_cannot.md | ~11 min |
| §5 | Synthesis: Thesis and Trajectory | POPULATED | drafts/section5_synthesis.md | ~11–12 min |
| §6 | Conclusion | POPULATED | drafts/section6_conclusion.md | ~5 min |

**Estimated total: ~57–59 minutes.** At the top of the 45–60 min range.
§2 is the load-bearing section. §4 and §5 are both at the long end of their targets
and are the natural trim points if the talk needs to shorten.

**Cross-section consistency review (2026-05-29):**
- §4 is tightest against its time budget. "Efficiency is not insight" was moved to §5
  where it fits the synthesis arc better.
- §5 and §6 both treat Castelvecchi/Erdős. §6 version compressed to a callback;
  §5 is the full analytical treatment. Speaker: do not re-expand §6 in delivery.
- The Reeh-Schlieder Hsu quote (*"model expertise extends across the entire
  literature..."*) appears in both §2 and §4. Intentional — §4 is the taxonomy
  section and it earns a second appearance as the Type 3 definition. Speaker:
  frame it as a callback, not a repeat ("as Hsu put it in §2...").
- "Physicist's role shifting" appears in §5 (forward-looking) and §6 (grounded in
  Hsu/Pan et al. time use). Different registers — keep both.
- §5.6 (first-person section) is a skeleton requiring speaker content. If this
  section runs short or long it will affect total time most.

---

## §1. Introduction: Two Timelines [POPULATED]

**Purpose**: Orient the audience historically and establish the talk's frame. The
parallel between the 1913–1926 QM arc and the 2017–2026 LLM arc is not decorative —
it primes the audience to take pace of change seriously, without requiring any claim
about AI significance. The §6 conclusion closes this frame; §1 must open it cleanly.

**Time budget**: 5–8 minutes. This section establishes tone; do not let it run long.

### 1.1 The Centennial Anchor

The title of this talk specifies 100 years. Let it be precise: on January 27, 1926,
Erwin Schrödinger submitted "Quantisierung als Eigenwertproblem (Erste Mitteilung)"
— Quantization as an Eigenvalue Problem, Part One — to *Annalen der Physik*. It is
one of four papers he would publish in the same journal that year. By December of 1926,
Max Born had added the probabilistic interpretation. The complete theoretical structure
of quantum mechanics — wave equation, operator algebra, probabilistic rule — had been
assembled in under two years.

We are 100 years from that moment. The question on the title slide is not rhetorical.

**Delivery note**: Open with the title question — say it aloud — then say "Let me tell
you about two timelines." Put up a two-column slide and walk both columns.

### 1.2 Timeline One: The Birth of Quantum Mechanics (1913–1926)

The arc from Bohr's atom to the Schrödinger equation spans 13 years. It does not feel
fast until you look at where the acceleration happens.

**1913 — The Bohr atom**
Niels Bohr, "On the Constitution of Atoms and Molecules" (*Philosophical Magazine*,
two papers). Quantization postulated: electrons occupy discrete orbits. No derivation,
no mechanism. It works for hydrogen. Physicists know something has changed; they do not
know what.

**1916 — Sommerfeld's refinements**
Arnold Sommerfeld, "Zur Quantentheorie der Spektrallinien" (*Annalen der Physik*).
Elliptical orbits, relativistic corrections, fine structure. The old quantum theory
is extended; its foundations remain unexplained.

**1922 — Stern-Gerlach**
Walther Gerlach and Otto Stern, "Der experimentelle Nachweis der Richtungsquantelung
im Magnetfeld" (*Zeitschrift für Physik*). Directional quantization demonstrated
experimentally. Something is happening to angular momentum that classical physics
cannot touch.

**1923 — Compton; de Broglie**
Arthur Compton, "A quantum theory of the scattering of X-rays by light elements"
(*Physical Review*). X-rays scatter from electrons as particles: photons have momentum.
Louis de Broglie, in the *Comptes Rendus*: matter has wave properties. Both moves are
outrageous and correct.

**1924 — de Broglie's thesis**
*Recherches sur la théorie des quanta* (Paris, 1924). Wave-particle duality argued as
a general principle. Einstein reads it and calls it significant. Most physicists wait.

**July 1925 — Heisenberg's Umdeutung paper**
"Über quantentheoretische Umdeutung kinematischer und mechanischer Beziehungen"
(*Zeitschrift für Physik*). The pivot point. Heisenberg abandons classical trajectories
entirely — position and momentum are not continuous variables, they are tables of
transition amplitudes. Matrix mechanics, though Heisenberg does not call it that.
Born and Jordan recognize it as matrix algebra within weeks.

**November 1925 — The Dreimännerarbeit**
Born, Heisenberg, and Jordan, "Zur Quantenmechanik. II" (*Zeitschrift für Physik*).
Matrix mechanics in complete form. The commutation relation [q,p] = iħ appears.
This is quantum mechanics — mathematically complete, physically bewildering.

**January 27, 1926 — Schrödinger submits Erste Mitteilung**
The wave equation. Derived from a variational principle applied to de Broglie waves.
Schrödinger will publish four papers in *Annalen der Physik* that year, including a
proof that wave mechanics and matrix mechanics are mathematically equivalent —
two routes to the same theory.

**June 1926 — Born's probability rule**
"Quantenmechanik der Stoßvorgänge" (*Zeitschrift für Physik*, two papers). The
wavefunction is not a physical wave; its squared modulus is a probability density.
This is the interpretation that allows quantum mechanics to make predictions. It will
win Born the Nobel Prize in 1954.

**1928 — Bohr's complementarity**
"The Quantum Postulate and the Recent Development of Atomic Theory" (*Nature*).
The philosophical framework. Wave and particle are complementary, not contradictory.
The Copenhagen interpretation begins to consolidate.

**The compression to notice**: From Heisenberg's Umdeutung paper (July 1925) to
Born's probability rule (June 1926) is *11 months*. In those 11 months: matrix
mechanics, the Dreimännerarbeit, the Schrödinger equation (four papers), the proof
of equivalence, and the Born rule. The entire theoretical apparatus of quantum
mechanics, assembled in less than a year. The physicists doing this were in constant
correspondence; some visited each other's institutes. The field moved faster than
anyone predicted, including the people making it move.

### 1.3 Timeline Two: The Development of LLMs (2017–2026)

**2017 — The foundational paper**
Vaswani et al., "Attention Is All You Need" (Google Brain / Google Research). The
transformer architecture. Attention mechanisms allow models to relate distant tokens
without recurrence. A technical contribution — not obviously revolutionary at the time.

**2019–2020 — Scaling**
GPT-2 (OpenAI, 2019): language generation at scale; at first partially withheld over
misuse concerns. GPT-3 (OpenAI, 2020): 175 billion parameters; few-shot learning
emerges — the model performs tasks it was not trained on, with only a few examples.
Scaling laws are identified: capability improves predictably with compute and data.

**November 2022 — The public inflection point**
ChatGPT. Not a research paper — a product. The broader world encounters the capability
directly. Physicists in the audience: recall where you were when you first used it and
what you asked it about your subfield.

Two weeks after launch: Gerardo Adesso (Nottingham) publishes the first paper
"entirely generated with outputs from ChatGPT" — a physics-themed gamification
experiment with no scientific content, explicit about its limitations. His 2022
conclusion: ChatGPT "is not at the level of autonomously making and developing
original scientific contributions." This is the baseline.

**2023–2024 — Professional-level performance; a named prediction**
GPT-4 (March 2023): multimodal; scores at or above the 90th percentile on bar exams,
GRE, USMLE. Reasoning models (o1 class, 2024): extended chain-of-thought; capable of
sustained multi-step derivation. Graduate-level physics benchmarks saturating.

Also in 2023: Terence Tao (Fields Medal, UCLA) wrote: *"The 2023-level AI can already
generate promising leads to a working mathematician. When integrated with tools such
as formal proof verifiers, internet search, and symbolic math packages, I expect,
say, 2026-level AI will be a trustworthy co-author."* (Quoted in Binz et al., PNAS
2025.) The talk is being given in 2026. The rest of the evidence in this talk is the
test of whether Tao was right — and on what terms.

**2025 — Frontier models enter the lab**
GPT-5, Gemini 2.5 Pro, Qwen-Max, and others. These are the models Stephen Hsu uses
in the Generate-Verify workflow described in §2. A quantum field theory result —
published in *Physics Letters B* — where the main research direction was proposed by
GPT-5, unprompted, during a Q&A about the author's 2014 paper.

**May 2026 — The mathematics leading indicator**
Castelvecchi, *Nature* 653 (May 19, 2026): "How AI is transforming mathematics."
General-purpose LLMs contributing to solved problems in number theory. A Fields Medal
by 2030 predicted by a senior Google DeepMind researcher. Proof-length capabilities
scaling toward 10 pages, then 100. This is happening in mathematics now; it is where
theoretical physics is heading.

**The compression to notice**: From "Attention Is All You Need" (2017) to a published
QFT result with LLM-generated conjecture (2025) is *8 years* — shorter than the
13-year span from Bohr to Schrödinger. From ChatGPT (November 2022) to that same
published result is *3 years*. The explosive phase — the Umdeutung-to-Born-rule 
equivalent — may be the three years we are currently living through.

### 1.4 What the Parallel Claims, and What It Does Not

This needs to be said once, clearly, before the audience pushes back silently.

**What the parallel claims**:
Both timelines represent episodes of compressed, discontinuous capability development
driven by a foundational architectural insight (Heisenberg's abandonment of classical
trajectories; the attention mechanism). Both surprised even their practitioners at
the speed of what followed. In both cases, the capability arrived faster than predicted
from the apparent plateau immediately before it.

**What the parallel does not claim**:
- That LLMs describe anything about physical reality (QM describes nature; LLMs do not)
- That the comparison has predictive force about *what* will happen, only about *pace*
- That the significance of LLMs to physics will equal the significance of QM
- That the analogy is anything other than a heuristic for taking pace seriously

The honest framing: the QM parallel is motivational, not explanatory. Its function is
to make this audience — physicists who know how fast 1925–1926 actually moved — take
the pace of LLM development seriously, without requiring any claim about AI that goes
beyond the documented evidence.

### 1.5 The Talk's Evidence Base

Everything that follows is drawn from published or preprint sources:

- One peer-reviewed physics paper: Hsu (2026), *Physics Letters B*
- One published empirical study: Pan et al. (2025), *Communications Physics*
- One position paper from leading physicists and ML researchers: Lu et al. (2026)
- One *Nature* news feature on the mathematics leading indicator: Castelvecchi (2026)

The case study in §2 is the anchor. The broader landscape in §3 shows it is not
isolated. §4 characterizes what LLMs can and cannot do. §5 synthesizes these into
a thesis. §6 answers the title question directly.

**Framing sentence to close §1** (spoken, no slide):
> *We are 100 years from the moment the wave equation was written. The question
> I want to explore today is whether we are also inside a comparably compressed
> moment — and what that would mean for how we do theoretical physics.*

---

## §2. A Case Study: The Hsu Paper [POPULATED]

**Purpose**: Anchor the talk in a concrete, peer-reviewed, published result. The Hsu case
is the best single piece of evidence currently available that LLMs can make a non-trivial
contribution to frontier theoretical physics research. Handle it carefully: neither oversell
nor understate.

### 2.1 The Publication

Hsu, Stephen D.H. "Relativistic covariance and nonlinear quantum mechanics:
Tomonaga-Schwinger analysis." *Phys. Lett. B* 872 (2026) 140053.
arXiv:2511.15935. Accepted after standard peer review.

**The physics problem**: The paper asks whether nonlinear (state-dependent) modifications
to quantum field theory can be made compatible with relativistic covariance. The question
matters because the linearity of quantum mechanics is exact as far as we know, but the
foundations community has long explored whether nonlinear corrections are possible in
principle. Previous work (Gisin 1990, Polchinski 1991, Ho–Hsu 2014) had shown problems
with nonlinear QM in non-relativistic settings.

**The approach**: Hsu uses the Tomonaga-Schwinger (TS) formulation of QFT — a covariant
framework in which evolution is defined on arbitrary spacelike hypersurfaces rather than
on a single time coordinate — to derive precise integrability conditions for
foliation independence under state-dependent evolution.

**The result**: State-dependent nonlinear modifications to QFT generically fail the TS
integrability conditions. The key mechanism: state-dependent evolution does not preserve
operator commutation relations (microcausality) over time, even if microcausality is imposed
on an initial Cauchy slice. Three specific nonlinear models are analyzed and all fail:
  - Weinberg local expectation-value form (Weinberg 1989)
  - Weinberg nonlocal mean-field generalization
  - Kaplan-Rajendran retarded (past-light-cone) model (2022)

The conclusion: under TS integrability with microcausality, admissible deterministic
state-dependent modifications collapse to the linear case.

**Context for the audience**: The result is a no-go theorem at the frontier of quantum
foundations. It is not a solved problem dressed up as new — the TS framework had not
previously been applied to this question with the Fréchet derivative terms that
state-dependence requires. The referee asked for the KR model extension, which was
not in the original submission, confirming the paper entered genuine peer review.

**Prior work connection**: Hsu had co-authored a 2014 paper (Ho and Hsu, "Locality and
Nonlinear Quantum Mechanics," *Int. J. Mod. Phys. A* 29, 1450088) that showed
instantaneous entanglement generation under nonlinear evolution in the non-relativistic
case. The 2025 paper upgrades this to the full relativistic QFT setting using the TS
formalism — and that upgrade is where the AI contribution enters.

### 2.2 What the Published Acknowledgements Say

The Acknowledgements in the published Phys. Lett. B paper read:

> "The author used AI models GPT-5, Gemini 2.5 Pro, and Qwen-Max in the preparation
> of this manuscript, to check results, format latex, and explore related work. The author
> has checked all aspects of the paper and assumes full responsibility for its content."

This is accurate but understates the AI contribution. The companion methodology paper
provides a fuller account.

### 2.3 The Companion Paper: How It Actually Worked

Hsu, S.D.H. "Theoretical Physics with Generative AI." Preprint, December 1, 2025.
Available: https://drive.google.com/file/d/16sxJuwsHoi-fvTFbri9Bu8B9bqA6lr1H/view

This paper describes the workflow in detail and includes verbatim prompt-response
exchanges with GPT-5. It is aimed at both AI researchers and theoretical physicists.

### 2.4 The Key Exchange: Where the Idea Came From

Hsu was testing GPT-5's understanding of his 2014 paper on nonlinear QM — a natural way
to probe a model's grasp of specialized prior work. He asked:

> *"Compare and contrast studies of nonlinearity in non-relativistic QM with treatments
> that incorporate what is known from quantum field theory — that the nonlinearity must
> involve the entire wave functional which describes a (potentially infinite) number of
> spacelike separated modes."*

GPT-5 gave a technically correct response, and then volunteered:

> *"If you want, I can sketch the Tomonaga–Schwinger version of this (evolution by
> spacelike hypersurfaces) to show explicitly why a hypersurface-local generator that
> depends nonlinearly on the global state cannot remain foliation-independent without
> collapsing back to linear dynamics."*

Hsu said yes. GPT-5 then generated the TS setup, the integrability condition including
the Fréchet derivative cross-terms, and the key operator constraint — equations that
"form the core of the resulting paper."

Hsu's own assessment: *"This exchange is remarkable because GPT-5 proposes a novel
research direction."*

**Note for the talk**: This is the clearest known case in the published literature of a
frontier physics research direction being proposed de novo by an LLM. The phrase "de novo"
appears in the abstract of the methodology paper. The research direction was not in any
prior paper; GPT-5 suggested it without prompting, in the course of responding to a
question about a related topic.

### 2.5 The Workflow: Generate–Verify Protocol

Hsu did not treat GPT-5 output as reliable. He used a structured workflow:

- **Generate step**: One model instance proposes a research step or calculation.
- **Verify step**: A separate model instance independently checks it. A minimal
  Verifier prompt: *"You are a world class theoretical physicist. Check the following
  for errors. Review each equation and reasoning step. Identify all problems and
  summarize your findings."*
- More specific Verifier steps are possible: targeted questions, pointers to relevant
  papers.

Models used: GPT-5, Gemini 2.5 Pro, and Qwen-Max as primary; DeepSeek V3.1 and
Grok-4 as final checks.

Hsu's analogy: *"Using LLMs as noisy Verifiers of a research step is not very different,
in my experience, from going down the hall to explain the new idea to a colleague. Even
an expert colleague will not render a completely reliable opinion; however the resulting
discussion is useful to discover problems and to calibrate conviction levels."*

Key observation: **convergent positive Verifier responses are a good (not perfect)
signal for correctness; lack of convergence signals a problematic step.** This
asymmetry is important and usable.

Reference point: The same Generate–Verify approach had been used by AI teams to solve
IMO problems at gold-medal level. The Hsu paper extends it to frontier physics research.

### 2.6 Where the AI Failed: The Reeh-Schlieder Episode

This is as important as the success story.

During the research, multiple LLMs suggested using results from axiomatic quantum field
theory — specifically the Reeh-Schlieder theorem and the "split property" — to prove that
the TS integrability conditions must be violated in the presence of nonlinear terms.

**These suggestions were wrong.**

Hsu: *"I expended a significant amount of effort to determine this, given that my
background is not in axiomatic field theory."*

Why this matters:

1. The error was cross-subfield: the models drew on genuine knowledge from a distant
   part of the literature (axiomatic QFT) and suggested it applied to a different problem.
   This is not a simple factual hallucination — it required understanding enough of both
   areas to construct a plausible-sounding but incorrect connection.

2. Hsu's diagnosis: *"model expertise extends across the entire literature of our subject,
   and hence they are fully capable of introducing plausible-sounding applications of
   techniques from distant subfields. These are often the most difficult confabulations
   to detect!"*

3. The Verifier methodology helped: multiple Verifier steps failed to converge on this
   question, which was a signal that something was wrong. This is the asymmetry in action.

4. Resolution required the researcher's own deepened understanding — Hsu worked through
   the Reeh-Schlieder theorem well enough to understand its limitations himself.

**Key observation for the thesis**: The failure mode is not random noise. It is
systematically related to LLM strengths: broad exposure to the literature enables
broad confabulation across it. Expert human oversight is not merely desirable — it is
structurally necessary to catch exactly the failures that non-experts cannot catch.

### 2.7 Peer Review: The KR Extension

The paper underwent standard peer review at *Physics Letters B*. The referee requested
analysis of the Kaplan-Rajendran (KR) retarded nonlinearity model using the new TS
conditions — a non-trivial extension not in the original submission.

GPT-5 generated the correct calculation. The calculation required careful treatment of
causal structure: the retarded kernel and commutator terms have support on overlapping
past light cones J⁻(x) ∩ J⁻(y), and the key insight is that even retarded (causal)
dependence fails the TS integrability conditions because spacelike-separated points
share a nonempty causal past. Other models initially failed to handle the causal
structure correctly but converged to GPT-5's result when used as Verifiers.

**For the talk**: The referee extension is useful because it shows LLM contribution
persisting through the revision phase — not just ideation, but technical response to
expert criticism.

### 2.8 Summary of the Hsu Case: What to Claim and What Not to Claim

**What can be claimed**:
- A published, peer-reviewed paper in a reputable physics journal with a stated
  AI contribution to a novel technical result
- The main research direction (use of TS formalism for this problem) was proposed
  by GPT-5 unprompted
- The key equations were generated by GPT-5 in the course of that exchange and
  form the core of the published paper
- The Generate-Verify workflow is a replicable, described methodology
- LLM cross-subfield confabulation caused significant wasted effort (Reeh-Schlieder)
- Expert human oversight by the author was essential throughout

**What cannot be claimed**:
- That GPT-5 "understands" physics in the way a physicist does
- That this is replicable without expert oversight
- That it represents what non-expert researchers could do
- That the result could have emerged from single-shot LLM use
- That this proves LLMs can do physics autonomously

**The honest framing** (Hsu's own words):
> *"Research with an LLM might be compared to collaboration with a brilliant but
> unreliable human genius who is capable of deep insights but also of errors both
> simple and profound."*

### 2.9 Disclosure Questions (for Thesis)

The Acknowledgements understate the AI contribution relative to what the methodology
paper reveals. This raises a question for the talk: are current norms for disclosing
AI contributions in physics publications adequate? If the originating conjecture came
from a language model, what does authorship mean? Hsu takes full responsibility and
does not attribute co-authorship to the AI — but the norms around this are unsettled.
This connects to broader questions about the epistemology of physics under AI-assisted
research. [→ THESIS §C]

---

## §3. Broader Landscape: LLMs in Physics and Math [POPULATED]

**Purpose**: Show the Hsu paper is not an isolated anomaly. Document the range of
current activity. Organize around structural patterns rather than a list of papers.

### 3.1 The Lu et al. Paper: A Framework

Lu et al. "Can Theoretical Physics Research Benefit from Language Agents?"
arXiv:2506.06214v2. Max-Planck-Institut für Quantenoptik / MCQST / ETH Zürich /
MPI for Intelligent Systems. Originally submitted June 2025; revised March 2026.

**Citation**: arXiv:2506.06214v2. Preprint — not yet published in a journal.
The *Nature* editorial's "Lu, C. et al. *Nature* 651, 914–919 (2026)" was verified
(doi: 10.1038/s41586-026-10265-5) and is a *different paper entirely*: "Towards
end-to-end automation of AI research" (The AI Scientist, by Chris Lu, Cong Lu et al.,
March 2026). Cite our Lu et al. paper as a preprint only.

**What this paper is**: A preprint position paper — a structured argument about what
LLMs currently can and cannot do in theoretical physics, written by a collaboration
including serious physicists (Cirac group at MPQ, central to quantum many-body and
quantum information) and serious ML researchers (Schölkopf, a leading figure in
machine learning). Published only on arXiv; cite accordingly.

**Central position**:
> *"LLM agents, when appropriately adapted and integrated with domain-specialized
> training and tooling, could potentially serve as a promising technology for
> accelerating discovery in theoretical physics — provided their current limitations
> in rigorous reasoning, physical grounding, and reliability are systematically
> addressed through targeted interdisciplinary research."*

Note the hedging: "when appropriately adapted," "could potentially," "provided their
current limitations are addressed." Lu et al. is more cautious than Hsu. This
produces an interesting tension in the literature (see §3.5).

**The central claim about what makes physics hard for LLMs**:
Current models "show competence in mathematical reasoning and code generation" but
have "critical gaps in physical intuition, constraint satisfaction, and reliable
reasoning that cannot be addressed through prompting alone." Physics requires
connecting mathematical abstractions to physical reality — and that connection is not
captured in the formalism alone.

### 3.2 The Physics Research Workflow Taxonomy

Lu et al. map a typical theoretical physics research workflow into stages:

1. **Literature review and problem identification**
2. **Hypothesis formulation and model building**
3. **Analytical derivation and computation**
4. **Simulation and computational experiment**
5. **Analysis and interpretation of results**
6. *(iterate)* 
7. **Communication**

This is a useful framework for the talk: it lets the audience locate where LLM
contributions have been demonstrated and where they remain aspirational. Most
documented LLM contributions are in stages (1) and (3); stage (2) is where Hsu's
case is most remarkable; stages (4) and (5) have some ML precedent but limited
LLM application; stage (7) raises new questions about authorship and communication.

### 3.3 Skill Analysis: Where LLMs Stand Right Now

Lu et al. identify several distinct skill types, ordered roughly from more to less
reliable in current LLMs.

**Mathematical and symbolic reasoning**:
Despite saturation on legacy benchmarks (MATH, MMLU), "errors are frequently
observed in algebra and calculus." The core problem is next-token prediction: in
long derivations, small errors compound. Unit consistency is particularly fragile
(mixing SI and natural units). Path integral calculations are problematic. This is
not the same as benchmark performance — a model that scores well on textbook
problems may still make cascading errors in a novel derivation.

**Conceptual framework and formula retrieval**:
LLMs can generate "textbook-style explanations" but "this apparent understanding
can be superficially derived from statistical correlations rather than causal models
of physical laws." The failure shows up in subtle inaccuracies and unstated
assumptions — for instance, applying perturbation theory without stating the
conditions for its validity.

**A key example for the audience** — the Chern number problem: Diagonalizing
a 2×2 matrix is trivial linear algebra. In topological condensed matter physics,
the same 2×2 matrix is the Bloch Hamiltonian H(k) = d(k)·σ of a Chern insulator.
Finding eigenvalues ±|d(k)| is mathematically simple. But the *physics* lies in
how the winding of d(k) in momentum space determines the Chern number — a topological
invariant that dictates quantized Hall conductivity. An LLM that can do the linear
algebra may entirely miss the physical content. This is the gap between symbolic
competence and physical understanding.

**Physical consistency and constraint satisfaction**:
LLMs can generate solutions that are "mathematically plausible but physically violate
fundamental laws if not carefully guided." They may fail to enforce conservation laws,
symmetry constraints, or problem-specific boundary conditions. When faced with
ambiguous problem statements — where a physicist would ask for clarification or try
limiting cases — "LLMs tend to randomly pick one path without justification."

A concrete failure mode: in modeling system-bath interactions, an LLM might place
system spins and bath spins on the same lattice sites — physically nonsensical, but
not detectable from the algebra alone.

**Making justified approximations**:
Progress in theoretical physics "often hinges on making well-justified approximations."
LLMs may apply standard textbook approximations (ideal gas law, harmonic oscillator)
without checking whether they hold for the specific problem. They may apply
perturbation theory without stating the validity condition |λ⟨ψ_m^(0)|V|ψ_n^(0)⟩|
≪ |E_m^(0) − E_n^(0)|. Identifying the right approximation scheme is a form of
physical judgment that is not encoded in formal rules.

**Research "taste" and elegance**:
This is the subtlest skill. Consider calculating ⟨x̂⟩_n for a particle in a symmetric
potential. A brute-force approach integrates ∫x|ψ_n(x)|²dx using explicit Hermite
polynomials. An elegant approach notes: x is odd, |ψ_n|² is even, integral of
(odd × even) over a symmetric interval is zero by symmetry. The answer is immediate.
Current LLMs "may sometimes opt for overly complex or brute-force approaches if not
guided." The deeper concern: genuine physical elegance is about recognizing which
structures are load-bearing, which is a form of insight that may not reduce to
pattern matching across training data.

**Code generation**:
This is the most reliable skill. LLMs can generate NumPy/SciPy code for Monte Carlo
simulations, molecular dynamics, exact diagonalization. They can help maintain and
modernize legacy Fortran code. But physics-aware code generation requires
understanding Hilbert space structure, symmetries, and numerical algorithms —
not just the Python syntax. Missing fermionic anticommutation rules or failing to
enforce Gauss's law in a lattice gauge theory implementation produces code that
runs but computes something other than the intended physics.

### 3.4 The Characteristic Failure Pattern at Research Level

This is the most important finding in Lu et al. for the talk's thesis.

Existing physics benchmarks measure "test-taking capability" — exam-style problems
with single definitive answers. Lu et al. argue we need benchmarks analogous to
SWE-Bench (software engineering), covering the full research cycle. Early attempts
at research-level replication reveal:

> *"Models correctly execute standard procedures (e.g., routine operator expansions)
> but fail at the key non-standard step requiring genuine insight — discovering a
> novel proof technique or recognizing a technically delicate prerequisite before the
> main argument can proceed."*

This failure pattern has a specific structure: LLMs are good at the routine parts
and fail at the pivot point — the step that distinguishes a good physicist's
approach from a textbook application. This matches Hsu's observation from the
other direction: the LLM succeeded at a non-standard step (proposing the TS
framework) but that was a generative suggestion, not a derivation from scratch.

### 3.5 The Deriver-Critic Loop and Tool Use

Lu et al. independently arrive at the same structural solution as Hsu's
Generate-Verify protocol, which they call the **deriver-critic loop**:

> *"One agent generates derivations while another critiques them — either
> autonomously or with a human expert validating the critic's annotations.
> Crucially, critic agents should operate without access to intermediate
> generation artifacts to ensure independent verification."*

They also emphasize **tool use**: LLMs should call Mathematica, SymPy, or
numerical libraries rather than trying to do complex computations in-context.
The pattern: use Mathematica to test algebraic constructions, verify candidates
against constraints, iteratively converge toward a short verifiable algorithm —
then extract the analytical understanding that generalizes.

This is convergent evidence from independent researchers that structured
multi-agent verification is the key methodological innovation.

### 3.6 The Lu/Hsu Tension: Where the Field Stands

Lu et al. argue LLMs are currently "inadequate" for theoretical physics research
and require specialized training and tooling to be useful. Hsu, writing in the
same period, published a peer-reviewed QFT paper using general-purpose LLMs
with no specialized training.

This tension is not a contradiction — it is a description of a moving frontier:
- Lu et al. are identifying the *systematic* limitations of current LLMs when
  deployed without expert supervision
- Hsu demonstrates what is possible *with* expert supervision and structured workflow

The resolution is the expert bottleneck: Hsu's deep familiarity with his own 2014
paper and with the TS formalism was what allowed him to recognize the GPT-5 suggestion
as correct and worth pursuing, and to catch the Reeh-Schlieder failure. Without that
expertise, GPT-5's suggestion would have been indistinguishable from a plausible
hallucination.

Lu et al.'s conclusion that "non-expert use is likely to lead to large volumes of
subtly incorrect output" is entirely consistent with Hsu's success under expert
oversight. The Lu/Hsu pairing is thus more useful than either paper alone.

### 3.7 The De-Skilling Question

Lu et al. raise the concern that "depending too heavily on LLMs for tasks like
mathematical derivations, programming, or data interpretation could risk degrading
these essential skills among physicists, especially those in training. Deep intuition
often arises from performing detailed calculations firsthand."

They immediately invoke the Mathematica analogy: "the history of scientific computing
shows both warnings and reassurances: tools like Mathematica initially raised
de-skilling concerns but ultimately enabled mathematicians to focus on higher-level
work by automating repetitive calculations."

**For the talk**: this framing is valuable and honest. The de-skilling concern is real;
the Mathematica precedent is instructive without being deterministic. A physicist who
learned field theory by doing long calculations will relate to the concern. The honest
response is: we don't know how this resolves, and the answer may depend on how the
tools are integrated into physics pedagogy and research practice.

### 3.8 The Communicability Requirement

Lu et al. make a point that connects to the "proof indigestion" concern from NOTES.md:

> *"Agents should mirror how theoretical physics groups operate: presenting results
> at varying levels of detail, highlighting why certain approaches work, and enabling
> supervisors to probe assumptions — so that discoveries can be understood, critiqued,
> and built upon. If agents merely produce piles of derivations without conveying the
> discovery process and key insights, humans are reduced to mechanical checking rather
> than scientific understanding."*

This is the physics analog of Tao's "proof indigestion" — the risk that verified
results outrun human capacity to understand them. An AI that can produce technically
correct but opaque derivations creates a new kind of epistemic problem: not whether
the result is true, but whether we understand *why* it is true. Physics has always
cared about the why. [→ THESIS §C, §5]

### 3.9 Future Directions Flagged by Lu et al.

**The AlphaGo Move 37 class of problems**: For discovery in physics, Lu et al. identify
a promising problem class — problems where the search space is combinatorially large
but candidate solutions can be verified in polynomial time:
- Discovering quantum error-correcting codes satisfying Knill-Laflamme conditions
- Finding Hamiltonians with exact symmetries or dualities
- Classifying symmetry-protected topological phases
- Identifying integrable structures

In these settings, AI enumerates candidates at scale while humans or automated
checkers verify. The result is "certificate-backed discovery where every claimed
result is independently validated." This is both more achievable and more clearly
structured than the open-ended conjecture generation in Hsu's case.

**Fine-tuned physics LLMs**: Lu et al. call for physics-specific training datasets,
reward signals that capture "physical reasoning quality" not just pass/fail on
benchmark problems, and verification frameworks encoding fundamental principles.
This is a research agenda, not a near-term capability. The current generation of
LLMs that Hsu used were general-purpose, suggesting the gap may be narrower than
Lu et al. imply.

### 3.10 Other Sources: How They Fit

**Pan et al. (2025)** — "Quantum many-body physics calculations with large language
models," *Communications Physics* 8:49 (2025). doi:10.1038/s42005-025-01956-y.
Cornell / Google Research / Harvard / Google DeepMind. Submitted September 2024;
accepted January 2025.

This is the **empirical study** in the group — actual numbers from actual physics
calculations, in contrast to Hsu (case study) and Lu et al. (position paper).

*The task*: Hartree-Fock (HF) mean-field theory, the workhorse approximation
method of condensed matter physics. Over 6,456 cond-mat arXiv papers use HF in
their abstracts in the last decade. The HF method replaces many-body interactions
with "mean fields" proportional to an order parameter, separating the problem into
an analytic derivation of the HF Hamiltonian H_HF and a computational self-
consistency equation. Deriving H_HF for a given system requires graduate-level
knowledge and, in practice, "years of study to do reliably." The five-step analytic
procedure: (1) set up system Hamiltonian, (2) Fourier transform, (3) apply Wick's
theorem to decompose into mean fields, (4) simplify the quadratic Hamiltonian,
(5) identify order parameter structures.

*The method*: An **HF template** — a multi-step prompt template with placeholders
for problem-specific information, decomposed into 11 sub-tasks (T1–T11). Each
sub-task prompt is constructed like instructions to a beginning graduate student:
natural language, specific steps, examples. Critically, each step's output is
evaluated and corrected by a human expert before becoming the input to the next
step. The template was evaluated on a corpus of 15 recent APS-journal papers
spanning a decade of condensed matter research.

*The headline results*:
- Average score of **87.5/100** across all rubric layers and all papers
- GPT-4 correctly derived the final H_HF in **13 of 15 papers** (with human
  correction of intermediate steps)
- Performance was **uniformly high across all five calculation steps** — not just
  the early or easy ones; system Hamiltonian setup scored as well as the Wick's
  theorem decomposition and the order-parameter simplification
- For Rigor (mathematical accuracy): consistently **above 95** — "quite capable
  of carrying out the calculations correctly"
- As a byproduct: GPT-4 identified **typos in published research papers**
  in the corpus — it was computing intermediate steps the papers didn't show,
  and occasionally found the published answer inconsistent with correct derivation

*The generalization question*: GPT-4's training cutoff was September 2021. The
corpus includes papers both before and after that date. Performance was flat across
the cutoff — the training-data-overlap did not affect scores. More specifically,
intermediate calculation steps were not written out in the source papers — GPT-4
had to derive them. This argues against pure memorization and for genuine
mathematical generalization.

*The information extraction task*: Pan et al. also tested whether GPT-4 could fill
in the template placeholders directly from paper excerpts and abstracts, eliminating
the human setup step. The nuanced result:
- High scores extracting **system-specific information** (what the physical system is,
  what symmetries it has)
- High scores extracting **explicit notation** (symbols and conventions stated in the paper)
- Poor scores on **implicit notation** — field conventions that every practitioner
  knows but that no paper writes down: the standard Fourier transform definition,
  second-quantized operator conventions, the usual way to handle fermionic statistics
- With one-shot prompting (a single example of an excerpt and its correct extraction),
  performance on one template task jumped from 44 ± 8 to 80 ± 6

Most ambitiously: from just an abstract and 10 guided questions, GPT-4 could
sometimes infer the system-specific information and correctly carry out the full
HF derivation, demonstrating that "the vision of giving a synopsis of a calculation
in natural language to an LLM to carry out a Hartree-Fock calculation is within reach."

*How Pan et al. fits the framework from §3*:

In the Lu et al. taxonomy of physics research stages, Pan et al. sit squarely in
**stage (3): analytical derivation and computation**. This is not conjecture
generation (Hsu) or literature synthesis — it is executing a well-defined
multi-step calculation framework on novel instances. The Lu et al. "characteristic
failure pattern" (succeed at routine steps, fail at the non-standard insight step)
does *not* apply here, because the non-standard insight — how to decompose the HF
problem — is baked into the HF template by the human researchers. The model is
operating inside a framework, not generating the framework.

This is not a limitation of the paper; it is its honest claim. Pan et al. are
demonstrating that the **calculational execution layer** of theoretical physics is
largely within reach of current LLMs when the task is appropriately structured.

*The key contrast with Hsu*: The GPT-5/Hsu result is about research direction —
proposing a novel framework (use TS formalism for this problem). The Pan et al.
result is about research execution — applying an established framework (HF) to new
instances. Both are genuine contributions, but they live at different levels of the
research workflow. Neither paper is more important; they describe different modes
of LLM contribution.

*The correction workflow*: Pan et al. use **sequential human correction** —
each step is checked before the next step runs. This differs from Hsu's
Generate-Verify (parallel independent instances) and Lu et al.'s deriver-critic loop
(critic operates without access to generation artifacts). All three converge on the
same principle: structured human oversight between steps is necessary. The
operational difference is that Pan et al.'s method requires an expert to be in the
loop at every step, which is more labor-intensive but also more reliable for
well-defined tasks.

*The implicit-notation gap*: The finding that GPT-4 struggles with implicit
conventions — field knowledge that's real but unwritten — is the most important
limitation in the paper. It is precisely the knowledge that separates a physicist
who knows condensed matter from one who doesn't. This connects to Lu et al.'s
observation about physical context-dependence and to Hsu's point that non-expert
use leads to subtle incorrect output: what the expert supplies, besides oversight,
is fluency in the implicit register of a subfield.

*For the talk*: Pan et al. is the clearest quantitative evidence that LLMs can
perform at **expert level** on a specific, well-defined class of research-level
physics calculations. The 87.5 score and the above-95 Rigor score are quotable.
The discovered-typos finding is a vivid detail. The limitation — implicit notation,
field conventions, the scaffolding requirement — is equally important and keeps
the claim honest.

**Wang et al. (2024)** — "Examining the potential and pitfalls of ChatGPT in science
and engineering problem-solving." *Frontiers in Education* 8:1330486. Karen D. Wang,
Eric Burkholder, Carl Wieman, Shima Salehi, Nick Haber. Stanford / Auburn University.
Published January 2024. Note: Carl Wieman is a Nobel laureate in physics (2001) and
the foremost figure in physics education research.

*What the paper tests*: GPT-4 solving 40 problems from a calculus-based introductory
engineering physics course — statics, kinematics, momentum, energy, fluids. NOT
research-level physics. Problems span a two-dimensional framework: (1) abstract vs.
real-world context; (2) well-specified (all data given) vs. under-specified (data
must be assumed or estimated). All 40 problems are real-world context; they vary
on data specificity.

*The key result*:

| Problem type | N | Correct | Accuracy |
|---|---|---|---|
| Well-specified | 16 | 10 | **62.5%** |
| Under-specified | 24 | 2 | **8.3%** |

The gap is statistically significant (Fisher's exact test, p < 0.001). This is the
most direct quantitative evidence for the execution/judgment distinction (→ §4.6):
when all data is provided and the task is structured, GPT-4 performs reasonably;
when real-world judgment is required about what to assume, it nearly collapses.

*Three failure modes*:

(1) **Failure to construct accurate physical world models** (14/28 incorrect solutions):
ChatGPT correctly identifies the relevant physics (e.g., torques for the dresser
tipover problem) but misrepresents the physical situation (e.g., cannot correctly
identify the pivot point). For the Millennium Tower problem, it correctly computed
the building's weight but failed to account for the concrete slab and pile weights —
it never formed an accurate geometric model of the system. This failure is about
physical representation, not physics knowledge.

(2) **Failure to make reasonable assumptions about missing data** (8/28): Given a
floating duck problem, ChatGPT assumes the duck's density is 950 kg/m³ — a value
inconsistent with the problem's own stated constraint that 20% of the duck is
submerged in saltwater (which implies ~260 kg/m³). It cannot work backward from
observable physical behavior to infer correct parameter values. For a merry-go-round
problem, it estimated an initial speed far exceeding US Consumer Product Commission
safe limits for playground equipment — it computed a number without checking it
against real-world constraints.

(3) **Calculation errors** (6/28): Arithmetic and trigonometry errors, as in the
literature more broadly.

*An idiosyncratic case*: For the horsepower conversion problem (well-specified,
all data given), ChatGPT reached the correct answer while completely ignoring the
given data — instead using its training-data definition of horsepower. This raises
a structural question: when does the model prioritize its parametric knowledge over
provided context? Relevant to the implicit-notation problem in Pan et al.

*Chain-of-thought prompting*: "Solve step-by-step" recovered 3 of 28 previously
failed problems. Helped with physical modeling and assumption-making but had no
effect on calculation errors.

*Connection to Pan et al.*: This paper explains why the HF template works. Pan et al.'s
87.5% accuracy is achievable precisely because the HF template converts what would
be under-specified research problems (how do I apply Hartree-Fock to this paper?)
into a sequence of well-specified subtasks (given this Hamiltonian, apply Wick's
theorem to these terms). Wang et al.'s 62.5%/8.3% cliff shows what GPT-4 performance
looks like without that conversion. The expert who designs the HF template is doing
exactly what Wang et al.'s failure modes demand: constructing the accurate physical
model and specifying all required data before handing the problem to the LLM.

*For the talk*: The 62.5%/8.3% numbers are quotable and vivid. The connection to Pan
et al. and the execution/judgment distinction is the key point. The physical-world-
modeling failure is a distinct failure mode worth naming alongside the Type 1/2/3
taxonomy — it's not confabulation or calculation error; it's incorrect representation
of the physical situation.

**Wu and Tegmark (2018)** — "Toward an AI Physicist for Unsupervised Learning."
arXiv:1810.10525. Tailin Wu and Max Tegmark, MIT Dept. of Physics / Center for
Brains, Minds & Machines (2018, revised 2019).

**What it is — and what it is not**: This is not an LLM paper. It is a neural-net-based
ML system designed to learn physical laws from unlabeled trajectory data using four
strategies explicitly borrowed from physics culture: divide-and-conquer, Occam's razor,
unification, and lifelong learning. The "toy AI Physicist" is tested on environments
where balls move through combinations of gravity, electromagnetism, and harmonic motion.

The paper's goal is stated with unusual modesty: "The goal of this paper is to take a
very modest but useful step in that direction... does not even remotely approach the
ambition level of problem solving by human physicists." This disclaimer is itself a
data point: in 2018, the honest assessment of ML-in-physics was that it addressed toy
problems only. By 2025–2026, the conversation had shifted to peer-reviewed QFT results
(Hsu) and 87.5/100 on condensed matter calculations (Pan et al.).

**What it does and how**: The AI Physicist observes only coordinate sequences (ball
positions), with no domain labels. It simultaneously (1) discovers which regions of
space obey different laws, and (2) infers the equations of motion in each region —
without being told the laws or the boundaries. After learning, it uses minimum-
description-length (MDL) optimization to "snap" neural net parameters into simple
symbolic formulas: if a parameter is ≈1.4999917, the system checks whether 3/2 gives
equally good fit with lower description length. The result: it often recovers equations
exactly, including Newton's law (finding gravity weakens like r⁻² rather than r^1.9999),
Hooke's law, and the Lorentz force law.

**Key results**: Compared to a standard feedforward neural net:
- Median MSE improvement: ~10⁹× (billion-fold)
- Classification accuracy (unsupervised domain discovery): 100% (vs. 67.56% baseline)
- Fraction of "mystery worlds" solved exactly: 90–92.5%
- Rational/integer parameters recovered exactly in most cases

**The four strategies and their physics grounding**:
- *Divide-and-conquer*: Physics always asks "in what domain does this law hold?" —
  as Galileo ignored everything except the swinging lamp's period
- *Occam's razor*: Physics prefers simple theories; MDL formalizes this preference
  computationally
- *Unification*: Maxwell unified electricity and magnetism; Newton's gravitation unifies
  planetary dynamics across different planets. The AI Physicist attempts this automatically
- *Lifelong learning*: Accumulated theory hub enables fast learning in new environments —
  analogous to how experienced scientists solve new problems faster by building on prior work

**The successor — AI Feynman**: Reference [58] in the paper is Udrescu & Tegmark (2019),
"AI Feynman: A physics-inspired method for symbolic regression." This is Tegmark's next
project: symbolic regression applied to the Feynman lecture dataset, recovering known
physical formulas from input-output data. The lineage from Wu/Tegmark (theory learning
from trajectories) → AI Feynman (symbolic regression from data) → current LLM-in-physics
is the arc from "ML that learns physics" to "LLM that does physics."

**Why it matters for the talk — the interpretability contrast**:

Wu/Tegmark and the LLM papers (Hsu, Pan et al.) share a goal — AI doing theoretical
physics — but represent opposite philosophies about what "doing physics" means:

| | Wu/Tegmark (2018) | Hsu / Pan et al. (2025) |
|--|--|--|
| Goal | Interpretable symbolic formulas | Correct derivations in natural language |
| Method | Physics-inspired inductive biases (MDL, unification) | General-purpose LLM + expert scaffolding |
| Output | Equations the physicist can read and generalize | Steps the physicist must verify |
| Intelligibility | Explicit design goal ("intelligible intelligence") | Not guaranteed |
| Domain | Toy unsupervised physics from data | Real research problems with expert input |

The Wu/Tegmark tradition values what Lu et al. call the "communicability requirement"
(§3.8) — not just getting the right equation, but understanding *why* it is the right
equation. The LLM approach, at least in Hsu's workflow, produces derivations that must
be verified step by step, with no guarantee that the reasoning is interpretable even
when correct.

**For the talk**: Wu/Tegmark belongs in §1.3 as the 2018 data point on the ML-in-physics
timeline — before LLMs, before transformers dominated the field. It shows that "AI in
physics" is not a new question, and that it was being asked with explicit commitments to
parsimony and interpretability that the LLM era has partially set aside. The "intelligible
intelligence" goal connects directly to Botvinick & Gershman's epistemic argument (§5.4):
that physics without human understanding is not physics. Wu/Tegmark designed their system
so the output *would* be understandable. The question raised by the LLM papers is whether
that constraint is still achievable — or even still the right constraint to impose.

**Lewkowycz et al. (2022)** — "Solving Quantitative Reasoning Problems with Language
Models." *NeurIPS 2022*. Google Research. (Lewkowycz, Andreassen, Dohan, Dyer,
Michalewski, Ramasesh, Slone, Anil, Schlag, Gutman-Solo, Wu, Neyshabur, Gur-Ari,
Misra.)

**What this is**: The Minerva paper — PaLM pretrained models (8B, 62B, 540B parameters)
finetuned on 38.5B tokens of mathematical web content and arXiv papers. This is the
2022 frontier: specialized math-and-science finetuning of a large foundation model.
Its value for the talk is as the historical baseline — what was possible four years
before Hsu.

**The OCWCourses dataset**: 272 problems from MIT OpenCourseWare across undergraduate
STEM courses, including special relativity. This is the only physics-specific
undergraduate benchmark in the paper. Minerva 540B scores **17.6%** without voting,
**30.8%** with majority voting (maj1@k).

**Other benchmarks**:
- MATH (Hendrycks et al.): 33.6% without voting → 50.3% with maj1@256
- MMLU-STEM: 63.9% without voting → 75.0% with voting
- Polish National Matura (Math): 57% (62B) → 65% (540B); the 2021 national average was 57%

These numbers are the 2022 state of the art. The current frontier (Pan et al.: 87.5%
on real condensed matter papers; Wang et al.: 62.5% on well-specified intro physics)
represents the distance traveled in four years.

**The majority voting insight**: Lewkowycz et al. introduce maj1@k — select the most
common answer across k independent samples. "The truth is a Schelling point": correct
answers cluster naturally because there is typically one correct value, while wrong
answers are distributed across many incorrect values. Performance saturates around
k=64 for MATH. This is the benchmark-domain antecedent of Hsu's Generate-Verify
and Lu et al.'s Deriver-Critic: multiple independent generations are a verification
signal even without a human in the loop.

**The false positive problem** (critical for §4): 8% of MATH solutions with correct
final answers had incorrect chain-of-thought reasoning. At the hardest difficulty
level, the false positive rate reached **30%** — solutions that look correct and
reach the right answer by wrong reasoning. Lewkowycz et al. flag this as a
"potential source of concern" because it means the final answer alone is not a
reliable quality signal. For physics: a derivation that reaches the right equation
via faulty intermediate steps is published as a correct result but cannot be used to
understand the physics. This is the Lewkowycz-level version of what Hsu encountered
with the Reeh-Schlieder episode — correct-seeming output that required deep expert
engagement to diagnose.

**Failure mode taxonomy** (Table 4, 8B vs. 62B comparison):
- Incorrect reasoning: 82 cases
- Incorrect calculation: 70 cases
- Misunderstands question: 22 cases
- Uses incorrect fact: 16 cases
- Solution too short: 4 cases
- Hallucinated math objects: 4 cases

The dominant failure modes (incorrect reasoning, incorrect calculation) are both
checkable in principle — but at the 30% false positive rate on hard problems, checking
every step correctly requires effort comparable to solving the problem independently.

**For the talk — the 2022 baseline**: The Lewkowycz paper belongs in §1.3 as a
concrete point on the LLM timeline (2022: Minerva reaches 17.6% on OCWCourses
undergrad STEM; 2024–2025: Pan et al. reaches 87.5% on real condensed matter papers)
and in §5.2 as illustration of the pace of improvement. It is not a landmark result
in itself — it is the starting point for the curve that the Hsu, Pan et al., and
Castelvecchi results describe. The false positive problem is a genuine contribution
to §4.2: it is not enough for the final answer to be right.

**Adesso (2023)** — "Towards The Ultimate Brain: Exploring Scientific Discovery with
ChatGPT AI." *AI Magazine* 44, 328 (2023). arXiv:2308.12400. Gerardo Adesso,
University of Nottingham. Written two weeks after ChatGPT's public release (November
2022); uses GPT-3.5.

What the paper does: Adesso runs ChatGPT in a gamification environment where it
plays a text adventure game to benchmark hypothetical "physical theories." The
"result" is a fictional GPT4 theory (invented before OpenAI's GPT-4 existed) that
combines Generalized Probabilistic Theory with language capabilities. The paper
itself is almost entirely AI-generated. The author is explicit: "These experiments
are conducted within a virtual gamification environment and should not be regarded
as possessing any scientific foundation beyond showcasing the progress of AI."

What the paper is honest about: ChatGPT "occasionally generate[s] references or
information that may not be accurate or factual." The appendix reports that the
original version required revisions "to remove any hallucinations or hyperbolae,
such as unfounded claims of self-awareness." The author's 2022 conclusion: ChatGPT
"is not at the level of autonomously making and developing original scientific
contributions."

**Value for the talk — calibration only**: The Adesso paper is a data point for
the state of the art in November 2022. A physicist using the best available LLM
for "physics research" produced a gamification experiment with no actual scientific
content. Three years later, Hsu produced a peer-reviewed QFT paper in *Physics
Letters B* where the main research direction was LLM-generated. This is the
three-year arc of §1.3 made concrete. The contrast — not the paper itself — is
what belongs in the talk.

**Ghareeb et al. (2026) and Gottweis et al. (2026)** — Multi-agent AI scientists in
*Nature*. Both cited in the *Nature* editorial "Why AI cannot do good science without
humans" (21 May 2026, *Nature* 653, 650).

*Ghareeb et al. (FutureHouse, Robin)*: Ghareeb, A.E. et al. "A multi-agent system
for automating scientific discovery." *Nature* doi:10.1038/s41586-026-10652-y (2026).
FutureHouse / Fordham University / University of Oxford.

**What Robin is**: Three specialized agents — Crow (concise literature search via
PaperQA2), Falcon (deep literature evaluation), and Finch (scientific data analysis in
Jupyter notebooks) — integrated into a continuous loop. Given a disease, Robin
identifies relevant in vitro assays, proposes drug candidates ranked by an LLM
tournament, hands experimental execution to humans, receives raw data back, analyzes
it autonomously, and generates updated hypotheses. This is explicitly a "lab-in-the-loop"
system: Robin handles the intellectual steps, humans run the experiments.

**The scientific result — not just efficiency**: Robin was applied to dry age-related
macular degeneration (dAMD), the leading cause of blindness in the developed world.
Key findings confirmed in vitro:

- **Ripasudil** (a ROCK inhibitor approved for glaucoma in Japan): Robin proposed this
  for dAMD via phagocytosis enhancement of retinal pigment epithelium — an application
  *never previously proposed*. Confirmed: 1.89-fold increase in RPE cell phagocytosis
  (1.75-fold in independent human analysis). Approved drug, known safety profile.
- **KL001** (a circadian clock modulator): proposed by Robin based on circadian control
  of RPE phagocytosis. Confirmed as a hit. "To our knowledge no one has previously
  proposed KL001 as an enhancer of phagocytosis." A genuinely novel finding — structural
  parallel to Hsu's novel research direction.
- **ABCA1 upregulation**: Finch's RNA-seq analysis found 3-fold upregulation (p=2.13×10⁻⁸³)
  of ABCA1, a lipid efflux pump, in treated cells — a possible novel mechanistic target
  that "might have otherwise remained unexplored."

**The 200-fold speedup — with actual numbers**:
- Robin analyzed 551 papers in 30 minutes; human equivalent: ~540 hours
- Total cognitive labor per discovery cycle: 872–937 human hours → under 2 hours
- Cost per Robin run: $10.76 (45 Crow calls + 30 Falcon calls)

**The "combinatorial synthesis" framing**: Robin's authors describe what it does as
"combinatorial synthesis" — identifying non-obvious connections between disparate fields
that human experts overlook due to knowledge compartmentalization. The ripasudil insight
existed in the literature (ROCK inhibition enhances phagocytosis; phagocytic dysfunction
is present in dAMD) but had never been connected to dAMD therapeutics. Robin connected
them. This is the productive version of what Lu et al. call cross-subfield connection —
the same mechanism that enables LLM confabulation (Hsu's Reeh-Schlieder episode) also
enables genuine cross-domain synthesis when the literature grounding is reliable. The
difference is verifiability.

**The Deep Research control — validates the architecture**:
As a direct comparison, the same drug generation prompt was given to OpenAI's Deep
Research (a general-purpose multi-step research agent). Deep Research generated 17
unique candidates. **None were hits** in the RPE phagocytosis assay. Deep Research
did not suggest ROCK inhibition as a mechanism. This is a controlled within-paper
comparison demonstrating that the literature-grounded architecture (Crow/Falcon) adds
genuine value beyond what a generic powerful LLM agent produces.

**Hallucination rate — quantified**:
When the Crow/Falcon literature agents were ablated and replaced with raw o4-mini
calls, **44.5 ± 6.4% of references in drug candidate reports were hallucinated**.
With the full Robin architecture (Crow + Falcon): **0% hallucinated references**.
This is the sharpest quantitative evidence in the reviewed literature for both (a) the
severity of the hallucination problem in scientific LLM use, and (b) how literature-
grounded retrieval agents can practically eliminate it. For physics: this failure mode
is not hypothetical — it is measurable, and the mitigation exists.

**Finch data analysis performance**:
On BixBench (170 expert-generated bioinformatics/statistics question-answer pairs):
- Finch (with agent harness): 22.8 ± 1.7%
- Claude Sonnet 3.7 alone: 1.6 ± 1.2%
- Finch on single-step statistics tasks: 47.9% vs. 15.3% on multi-step bioinformatics

The statistics/bioinformatics gap maps onto Wang et al.'s well-specified vs.
under-specified cliff: single-step computations on clean tabular data (well-specified)
vs. multi-step pipelines requiring parameterization decisions (under-specified).

**For the talk**: Ghareeb et al. is the most concrete available demonstration of what
the 200-fold efficiency number actually means — not an abstraction but a specific drug
(ripasudil) now being studied for a disease (dAMD) it was never previously considered
for. The 44.5% hallucination rate for raw o4-mini belongs in §4.2 as a quantitative
anchor for the hallucination problem. The combinatorial synthesis framing belongs
in §4.1 alongside Hsu's cross-subfield navigation — same mechanism, different context.

*Gottweis et al. (Google, Co-Scientist)*: Asked to find repurposable drugs for
leukaemia and drug targets for liver fibrosis. The more striking result: asked to
develop a hypothesis explaining why many bacterial species share a particular suite
of antibiotic-resistance genes — a puzzle that the scientists on the team had been
investigating for approximately **a decade** without publishing. Co-Scientist arrived
at the same hypothesis **within days**.

This case parallels Hsu structurally: an AI system arriving at a result that
expert humans had been working toward. The difference is the type of contribution
(hypothesis replication rather than novel conjecture) and the field (experimental
biology rather than theoretical physics). Both the Hsu and Co-Scientist cases involve
expert-framed problems — the humans defined the question. Neither represents fully
autonomous research direction.

*The editorial's institutional position*: The *Nature* editorial board concludes
directly: "AI scientists can and should empower human researchers. They cannot and
should not replace them." And: "we don't yet know whether greater efficiency equates
to greater insight." This is not a researcher's opinion — it is the editorial stance
of the journal publishing these papers. The convergence with the talk's thesis is
notable and quotable.

*Relevance for the talk*: (1) Cross-domain confirmation that the Generate-Verify
structure is independently converging in different fields; (2) the 200-fold speedup
is a striking efficiency number; (3) the Co-Scientist/decade parallel is a vivid
illustration of what the expert bottleneck looks like in a non-physics context;
(4) the editorial's "efficiency ≠ insight" distinction is usable in §4.

**Castelvecchi (2026)** — *Nature* piece on AI transforming mathematics. Critical for
the "mathematics as leading indicator" thesis from NOTES.md: what is happening in
mathematics now is what is coming to physics. Connects §3 to §1's historical framing
and §5's trajectory argument. [Already in sources/to_review.]

### 3.11 Co-Scientist: Hypothesis Generation at Research Frontier (Gottweis et al., 2026)

Gottweis, J. et al. "Accelerating scientific discovery with Co-Scientist." *Nature*
doi:10.1038/s41586-026-10644-y (2026). Google Cloud AI Research / Google DeepMind /
Google Research / Stanford / Imperial College London.

**What Co-Scientist is**: A multi-agent AI system built on Google's Gemini, designed
as a "structured scientific thinking engine." Not a chatbot or a literature assistant —
a system of specialized agents that cooperate to generate and refine research hypotheses:
Generation, Reflection, Ranking, Evolution, Proximity, and Meta-review agents.

The core mechanism is a **"generate, debate, evolve" paradigm**: agents generate
candidate hypotheses, engage in internal self-play debate to evaluate them, rank
hypotheses through a tournament, and then evolve the top candidates through iterative
refinement. Crucially, hypothesis quality improves monotonically with compute time —
more thinking time produces better hypotheses, with no saturation observed. This is
test-time compute scaling applied to scientific reasoning.

**Scientist-in-the-loop by design**: Co-Scientist is explicitly "purpose-built for a
'scientist-in-the-loop' collaborative paradigm." Scientists specify research goals in
natural language, can inject initial hypotheses, give feedback via chat, and
prioritize outputs. Experimental validation is handed off to human wet-lab scientists.
"All three validations involved expert-in-the-loop." This is not a design constraint
being worked around — it is the stated architecture.

**The three validation cases**:

*Drug repurposing for AML (acute myeloid leukemia)*: Co-Scientist searched 2,300
approved drugs across 34 cancer types, generated ranked repurposing candidates reviewed
by oncologists, and suggested 5 candidates for wet-lab validation. Three showed cell
viability inhibition. Binimetinib: IC50 as low as 2 nM in AML cell lines, significantly
higher in non-AML control — demonstrating selective cytotoxicity at clinically relevant
concentrations. KIRA6 (IRE1α inhibitor): 18-fold IC50 separation between the most
sensitive AML line (KG-1a, 10 nM) and the non-AML control (TK6, 180 nM). Co-Scientist
also proposed synergistic drug combinations for AML with predominantly synergistic
results confirmed in vitro.

*Liver fibrosis*: Proposed novel epigenetic targets; two of three tested exhibited
significant anti-fibrotic activity in human hepatic organoids. One (Vorinostat) is
FDA-approved for cancer — a drug repurposing opportunity generated by cross-domain
connection.

*Antimicrobial resistance — the structurally parallel case*: Co-Scientist was asked
to explain how capsid-forming phage-inducible chromosomal islands (cf-PICIs) — mobile
elements carrying antibiotic resistance genes — achieve broad host range across bacterial
species. It was given "only minimal background information." In **two days**, Co-Scientist
independently proposed that cf-PICIs interact with diverse phage tails to expand their
host range. This precisely matched the primary finding of an independent experimental
study that had been working on the same question and published simultaneously as a
co-timed report. The researchers had been investigating this for approximately a decade.

**This is the structural parallel to the Hsu case**: expert-defined problem → AI
system given minimal framing → hypothesis generated that matches what domain experts
had concluded through years of investigation. The differences: (1) the domain is
experimental molecular biology, not theoretical physics; (2) Co-Scientist is an
autonomous multi-agent system, while Hsu's workflow centers on a human physicist
directing LLM queries; (3) Co-Scientist replicated an existing (unpublished) result,
while Hsu's GPT-5 proposed a genuinely novel research direction. The parallel is in
the *type* of contribution — hypothesis generation — and in the speed relative to
expert timelines.

**Evaluation**: Across 203 research goals (predominantly biomedical, also including
mathematics and physics goals), Co-Scientist demonstrated monotonic improvement in
hypothesis quality with compute time. On 15 expert-curated challenging goals, it
outperformed Gemini 2.0 Pro, Gemini 2.0 Flash Thinking, OpenAI o1, OpenAI o3-mini,
and DeepSeek R1 by expert preference ranking (average rank 2.36 out of 4, where 1 is
most preferred; novelty 3.64/5; impact 3.09/5). The system also improved upon expert
"best guess" solutions when given those as starting points.

**The architecture compared to prior frameworks**:

| Framework | Structure | Human role |
|-----------|-----------|------------|
| Hsu (Generate-Verify) | Two LLM instances; one generates, one checks | Human physicist structures task, catches errors, judges novelty |
| Lu et al. (Deriver-Critic) | Critic checks without access to generation artifacts | Expert physicist directs, evaluates |
| Pan et al. (Sequential correction) | Human expert checks each step | Expert corrects between every step |
| Co-Scientist | Multi-agent internal debate and tournament; agents generate, critique, rank, evolve | Scientist specifies goal, provides feedback, validates and experiments |

Co-Scientist is the most autonomous of the four — internal debate replaces much of
the step-by-step human review. But the scientist-in-the-loop remains essential for
goal specification, prioritization, and experimental validation. The principle is the
same; the automation is deeper.

**Limitations stated by the authors** (important for the talk's honesty):
- Knowledge constrained by **open-access literature** — no access to paywalled content
  or negative/failed experimental results. Systematic bias toward published positive findings.
- **Propagation risk**: relies on source literature quality; can amplify erroneous or
  irreproducible findings already in the literature.
- **Homogenization risk**: "risk of diminishing critical thinking or homogenizing
  research directions" — if many researchers use the same AI system to generate
  hypotheses, the space of hypotheses explored may narrow.
- Inherits LLM limitations: "imperfect factuality and the potential for hallucinations."
- Wet-lab validations are preliminary — not replacements for full preclinical/clinical trials.

**The homogenization risk for physics**: This limitation does not appear in the Hsu
or Lu et al. papers, but it is real and deserves a place in the talk. If multiple
research groups use the same AI system to suggest what problems to pursue, the effect
is not amplified serendipity but convergent search — many groups following the same
AI-suggested directions, leaving other directions unexplored. This is the inverse of
the productive inefficiency argument (§4.8): not only do individual researchers lose
the benefit of their own wandering, but the field loses the diversity that comes from
researchers wandering in different directions.

**Where Co-Scientist fits in the Lu et al. taxonomy**: Primarily stage (2) — hypothesis
formulation and model building. Unlike Pan et al. (stage 3: analytical derivation),
Co-Scientist is doing the earlier and harder step: deciding what to try. The AMR case
is squarely in stage (2): given a phenomenon (broad host range of cf-PICIs), propose
the mechanism. The drug repurposing case spans stages (1) and (2): synthesize literature,
then form testable hypotheses.

**For the talk**: Co-Scientist is the clearest available example of a multi-agent AI
system succeeding at the hypothesis generation stage — the stage Lu et al. identify
as most difficult and Hsu illustrates at smaller scale. It provides cross-domain
confirmation that the expert bottleneck (scientist in the loop) persists even in the
most automated currently-demonstrated system. The AMR two-days-vs.-decade comparison
is vivid and quotable. The homogenization risk is a genuinely new concern not captured
by the three core papers.

### 3.12 The Normative and Epistemic Dimensions (Binz et al., 2025)

Binz, M. et al. "How should the advancement of large language models affect the
practice of science?" *PNAS* 122(5), e2401227121 (2025). Max Planck Institute for
Biological Cybernetics / Helmholtz Center / TU Munich / UC Santa Barbara / Harvard /
Google DeepMind / University of Washington / Indiana University and others.
Published January 27, 2025.

**What this paper is**: A structured debate — four distinct groups of scientists
presenting positions and responding to each other. Not consensus; the groups
disagree substantially. The value for the talk is in the range of positions the
scientific community was already staking out in 2025, before the Hsu and Co-Scientist
results landed.

**Tao's 2023 prediction (quoted in Binz et al.)**:
> *"The 2023-level AI can already generate [...] promising leads to a working
> mathematician [...]. When integrated with tools such as formal proof verifiers,
> internet search, and symbolic math packages, I expect, say, 2026-level AI [...]
> will be a trustworthy co-author."*

This was Terence Tao writing in 2023. The talk is being given in 2026 — the year
Tao named. The Hsu paper, the Pan et al. results, and the Castelvecchi *Nature*
feature are the evidence base for evaluating whether the prediction is being borne
out. The talk should explicitly address this: Tao's "trustworthy co-author" framing
implies expert oversight (a co-author you trust is still one you check); it does not
imply autonomous research. On that reading, Hsu's workflow precisely matches.

**The four perspectives and what each contributes**:

*Schulz et al. — "More Like a Human Collaborator than a Software Tool"*:
LLMs are not traditional software; thinking of them as knowledgeable research
assistants better captures both their capabilities and their failure modes. Already
established practices of scientific integrity apply. Main contribution to the talk:
the collaborator framing, which Hsu's workflow exemplifies and which the THESIS.md
working thesis ("contributors") picks up. Also: the reproducibility problem (see §4).

*Bender et al. — "Science Is a Social Process That Cannot Be Autocompleted"*:
The harshest view. LLMs are "models of word form distributions — not models of the
information that people might get from reading that text." Three concerns that survive
scrutiny for the talk:
(1) **The cognitive vulnerability argument**: "We are ill-positioned to effectively
evaluate LLM output because we can't help but make sense of it." Human linguistic
processing is "instinctual and reflexive" — fluent text is processed as meaningful
even when it isn't. This is a structural reason why Type 2 and Type 3 failures
(§4.2) are difficult to catch: it's not just that the errors are plausible, it's
that the fluency itself disarms critical reading. Expert detection is harder than
it sounds.
(2) **Epistemic diversity**: "Widespread use of one or a few LLMs could undercut
epistemic diversity in science. When asked to provide a hypothesis, experiment, or
mode of explanation, LLMs may repeatedly offer similar solutions, instead of
leveraging the parallel creativity of an entire science community." This is the
same homogenization concern Gottweis et al. flag, from a different angle —
here focused on hypothesis diversity across the field, not just within a lab.
(3) **Writing is thinking**: The claim that LLMs can "relieve scientists of the
drudgery of writing" rests on a "false dichotomy between communication and
investigation... [that] ignores the role of writing in the process of formulating,
organizing, and refining ideas." If the physicist outsources the writing, they may
also be outsourcing part of the reasoning. This connects to Lu et al.'s
communicability requirement (§3.8) but at the level of individual cognition,
not field-level knowledge transmission.

*Marelli et al. — "A Matter of Principles, Not Just Regulations"*:
Transparency, accountability, fairness. The practical contribution: disclose which
LLMs were used and how; publish prompts as supplementary material; use the CRediT
taxonomy to code AI contribution without granting authorship. For the talk: the
disclosure norm gap illustrated by §2.9 (Hsu's acknowledgements understate the AI
contribution) is exactly what Marelli et al. are calling for reform on.

*Botvinick & Gershman — "AI Can Help, But Science Is for People"*:
The most analytically sharp perspective for the talk. Two aspects of science
that should remain irreducibly human:

**The normative aspect**: What problems shall we work on? Judgments of
"interestingness, significance, and timeliness are inherently tied to culturally
and historically grounded sensibilities and mores" that evolve over time. Science
no longer approaches homosexuality as a disorder; growing restrictions on animal
experimentation; new attention to historically neglected climate regions. These
shifts are not derivable from prior literature — they emerge from changes in human
values. An AI trained on past literature cannot generate value evolution. "People
should stay in the driver's seat, determining the direction of travel for science."

**The epistemic aspect**: "Would it be satisfactory to have AI systems that
successfully model aspects of nature — as reflected, for example, in accurate
predictions — but which do not directly advance human knowledge concerning the
underlying principles or mechanisms? From an engineering standpoint that might be
fine. However, if it's basic science we're talking about, we shouldn't let go of
the core objective, which is not just practical but epistemic. We cannot cede
understanding to artificial systems."

The **"subjective limit"** they name: humans have a "point of view" — knowledge
that is meaningful to us (epistemic) and values that are meaningful to us (normative).
Machines may have aligned versions of these, but alignment is yoked to our subjective
views. The epistemic aspect maps directly onto Tao's proof indigestion concern (§5.3):
a verified result that no human can explain is not science in Botvinick/Gershman's
sense, regardless of its formal correctness. The normative aspect maps onto the
homogenization risk (§3.11, §4.8): if AI steers problem selection, science loses the
value evolution that has made it self-correcting.

**The Galactica episode** (referenced by both Bender et al. and the introduction):
Meta released Galactica (2022), a science-specific LLM trained on scientific
literature and promoted as able to "summarize academic papers, solve math problems,
generate Wiki articles, write scientific code, annotate molecules and proteins."
It was taken offline after three days due to intense criticism for fabricating
information — including "fake papers (sometimes attributing them to real authors),
and wiki articles about the history of bears in space." For the talk: this is the
negative anchor — the Hsu paper is not the first attempt to use LLMs in science,
and the previous high-profile attempt failed visibly. The contrast is instructive
about what the expert bottleneck makes possible.

**For the talk**: Binz et al. provides the normative/epistemic framework (Botvinick
& Gershman) that gives the expert bottleneck philosophical grounding: it's not just
that experts catch errors (practical) — it's that expert judgment about what problems
matter and what counts as understanding cannot be delegated (principled). The cognitive
vulnerability argument (Bender et al.) strengthens the case for why expert oversight
is structurally necessary, not just desirable. The Tao 2023 prediction sets up a live
test the talk's evidence base answers.

---

## §4. What LLMs Can and Cannot Do [POPULATED]

**Purpose**: Give the audience a usable conceptual frame for evaluating LLM
contributions to physics. Not a technical tutorial — a physicist's working model.
This section draws directly on evidence from §2 and §3; it synthesizes rather than
introduces new material.

### 4.1 What the Evidence Shows LLMs Can Do

The three core papers give a concrete picture of demonstrated capability:

**Calculation execution at near-expert level** (Pan et al.): GPT-4 executing
Hartree-Fock mean-field theory — a standard but graduate-level analytic method —
scored 87.5/100 across 15 real condensed matter papers, with Rigor (mathematical
accuracy) consistently above 95. It found typos in published papers. It generalized
to papers outside its training window. This is not benchmark performance on toy
problems; it is execution of a core research tool on real publications. The ceiling
on this capability, within a well-structured template, is close to human expert.

**Conjecture generation at the research frontier** (Hsu): GPT-5 proposed, de novo
and unprompted, the use of the Tomonaga-Schwinger formalism to investigate
foliation independence under state-dependent QM evolution — a research direction
not present in any prior paper. The resulting equations became the core of a
published, peer-reviewed result in *Physics Letters B*. This is not summarizing
known results; it is proposing a novel conceptual move.

**Cross-subfield literature navigation**: LLMs have processed the entire arXiv.
They can draw connections across subfields at a speed no human can match. This is
the capability underlying both the Pan et al. information extraction results and
the Reeh-Schlieder suggestion in Hsu — the same mechanism that enables genuine
cross-domain synthesis also enables plausible cross-domain confabulation.

**Sequential multi-step reasoning within a structured framework**: Both Hsu and
Pan et al. demonstrate sustained correct reasoning over multi-step derivations —
not just one-shot inference. This is the capability that most surprised earlier
observers of LLMs.

### 4.2 A Taxonomy of LLM Failures in Physics

The failures documented across the three papers are not random — they have
structure. A physicist needs a map, not a list.

**Type 1 — Calculation errors** (easiest to catch):
Index mistakes, sign errors in momentum shifts, inconsistent unit conventions
(mixing SI and natural units). Lu et al. note these despite strong benchmark
performance. Pan et al. give partial credit for a sign error in a magnetic field
momentum shift. These are detectable by checking the output against physical
constraints — energy conservation, dimensional analysis, symmetry.

**Type 2 — Plausible-but-wrong conceptual steps** (harder):
The LLM produces a reasoning step that sounds correct and is internally consistent
but is factually wrong. In Lu et al.'s framing, this is applying a formula without
checking its validity conditions — perturbation theory without stating that
|λ⟨ψ_m|V|ψ_n⟩| ≪ |E_m − E_n|. The output looks like physics. It requires
knowledge of the content, not just the form, to detect.

**Type 3 — Cross-subfield confabulation** (hardest to catch):
The LLM draws on genuine knowledge from a distant part of the literature to
construct a plausible-sounding but incorrect argument in the problem at hand.
The Reeh-Schlieder episode in Hsu is the clearest example: the model correctly
understood the theorem, correctly knew it was relevant to operator algebras in QFT,
and incorrectly suggested it could be used to prove the TS integrability conditions
must be violated. Detecting this required Hsu to study axiomatic QFT in enough
depth to understand the theorem's limitations.

Hsu's diagnosis is exact: *"model expertise extends across the entire literature
of our subject, and hence they are fully capable of introducing plausible-sounding
applications of techniques from distant subfields. These are often the most
difficult confabulations to detect."*

The taxonomy matters because the mitigation strategies are different:
- Type 1: automated checking, dimensional analysis, symmetry verification
- Type 2: structured prompts that force explicit statement of validity conditions;
  expert review
- Type 3: requires deep human expertise in both the source and target subfield —
  this is structurally the hardest to automate

**The false positive problem** (Lewkowycz et al., 2022): A related structural issue
that cuts across all three types. At the hardest difficulty level on the MATH
benchmark, **30% of correct final answers** were accompanied by incorrect reasoning
in the chain of thought — the model reached the right answer by the wrong path.
For physics: this means the final equation alone cannot be trusted as a quality
signal; the intermediate steps must be checked. An LLM derivation with a plausible
chain of reasoning and a correct-looking final expression may be producing the right
answer for the wrong reasons. This is especially dangerous for Type 2 failures,
where the reasoning sounds correct to anyone who does not already know the answer.

**Citation hallucination — quantified** (Ghareeb et al., 2026): When raw o4-mini was
used to generate drug candidate reports without literature-retrieval agents,
**44.5 ± 6.4% of references were hallucinated** — fabricated citations that do not
exist. With Robin's full Crow/Falcon literature-grounded architecture: **0%**. This is
the sharpest available quantitative measure of the hallucination problem in scientific
LLM use, and of how far mitigation can go. For physics: a hallucinated reference is
particularly damaging because it is indistinguishable from a real citation in the
output text, and because a plausible-sounding fake result can propagate into subsequent
reasoning. The mitigation — literature-grounded retrieval agents that check every
claim against real papers — exists and works, but requires engineering effort and adds
latency. Unmitigated frontier LLMs used directly for scientific literature synthesis
operate at roughly a 44% fabrication rate on citations.

**A related failure mode from Wang et al. (2024) — physical world modeling**:
Distinct from all three types above. ChatGPT can correctly identify the relevant
physics (e.g., torques for a mechanical system) but misrepresent the physical
situation (e.g., cannot correctly identify the pivot point, or fails to account for
all bodies in a force diagram). Wang et al. found this was the dominant failure for
GPT-4 on under-specified introductory physics problems (14/28 incorrect solutions).
The error is in the physical representation, before any formula is applied — correct
physics applied to an incorrect model of the situation. Expert physicists construct
this representation automatically; LLMs cannot reliably do it when the problem
requires inferring spatial relationships or physical constraints not explicitly stated.
This failure mode is distinct from Type 2 (wrong physics, right representation) and
from the implicit-knowledge gap (missing field conventions, →§4.3) — it is wrong
physical representation, independent of physics knowledge.

### 4.3 The Implicit-Knowledge Gap

Pan et al. identify a specific failure mode that cuts across all three types:
**implicit field conventions** — knowledge that every practitioner has but no paper
states. The standard Fourier transform definition in second-quantized notation,
the usual fermionic boundary conditions, the conventional factor ordering in the
BdG Hamiltonian. These are the things a graduate advisor corrects once in year one
and never mentions again. They are not on arXiv. LLMs have absorbed the explicit
literature but not this register of tacit knowledge.

This connects to something deeper. Lu et al. note that physics requires "connecting
mathematical abstractions to physical reality" — and a significant part of that
connection is carried by implicit conventions, by what "everybody knows," by the
distinction between a matrix and the physical operator it represents in a specific
Hilbert space. The Chern number example makes this precise: the linear algebra is
trivial, but the physics is in the winding number, and knowing to look for the
winding number is tacit knowledge, not derivable from the formalism alone.

### 4.4 The Expert Bottleneck

This is the central organizing principle across all three papers, stated differently
by each:

- Hsu: *"Non-expert use of AI in frontier research — even by individuals, such as
  PhD students, with considerable background — is likely to lead to large volumes
  of subtly incorrect output."*
- Lu et al.: Current LLMs are "inadequate" without "domain-specialized training and
  tooling" — but the tooling they envision is precisely the kind of structured
  framework an expert builds.
- Pan et al.: The HF template was designed by expert condensed matter physicists.
  GPT-4 executes brilliantly inside it. The template design is not automated.

The bottleneck is not model capability in isolation. It is the combination of
model capability with expert scaffolding: structuring the task, catching Type 3
errors, supplying implicit-knowledge context, deciding which model outputs are
worth pursuing. Hsu's deep familiarity with his 2014 paper and the TS formalism
was what allowed him to recognize the GPT-5 suggestion as novel and correct —
and to reject the Reeh-Schlieder suggestion as plausible but wrong.

**For the audience**: This framing is honest and useful. It does not dismiss LLMs
("they're just autocomplete"). It does not uncritically celebrate them ("AI is
doing physics"). It says: the tool is real, the limitation is also real, and the
limiting factor is human expertise, which is not going away.

### 4.5 The Generate-Verify Principle

Three independent research groups arrived at the same structural solution:

| Paper | Name | Structure |
|-------|------|-----------|
| Hsu | Generate-Verify | One model generates; separate instance checks independently |
| Lu et al. | Deriver-Critic loop | Deriver proposes; critic checks without seeing artifacts |
| Pan et al. | Sequential correction | Human expert checks each step before the next runs |

All three converge on the same principle: **structured human oversight between
steps is necessary**. The differences are operational:
- Hsu uses parallel independent model instances; faster, scales to model capabilities
- Lu et al. call for critic isolation to prevent contamination of the verification
- Pan et al. use human-in-the-loop at every step; most labor-intensive, most reliable
  for well-defined tasks

The IMO parallel (Hsu): the same Generate-Verify structure, applied to
International Math Olympiad problems, reached gold-medal level. This is independent
corroboration from a domain with formal correctness criteria. Convergent positive
Verifier responses are a good (not perfect) signal for correctness; lack of
convergence is a reliable signal that something is wrong.

**Majority voting as a simpler antecedent** (Lewkowycz et al., 2022): Before
multi-agent verification, Lewkowycz et al. introduced maj1@k — generate k independent
solutions, select the most common answer. The intuition: "the truth is a Schelling
point." Correct answers cluster on a single value; wrong answers distribute across
many. This works as a verification signal even without an expert or a separate Verifier
instance — purely statistical. Hsu's Generate-Verify and Lu et al.'s Deriver-Critic
are architecturally more sophisticated versions of the same core insight: independent
generations that converge are more reliable than a single generation. The added value
of expert oversight is precisely catching the cases where wrong answers also cluster —
Type 3 confabulations that sound correct to anyone without deep subfield expertise.

### 4.5a GPT-1900: A Direct Test of Reasoning vs. Pattern Matching

Hla, M. "Machina Mirabilis." Blog post, 2026. https://michaelhla.com/blog/machina-mirabilis.html
GitHub: https://github.com/michaelhla/gpt1900

**The experiment**: A 3.3B parameter LLM trained exclusively on pre-1900 text (~22B
tokens, British Library + institutional books + American newspapers; additional 290M
tokens of Maxwell/Newton/Faraday midtraining). No Einstein, no Planck, no QM,
no relativity — filtered aggressively to exclude even post-1900 forewords. Then
asked: can it reason toward 20th-century physics it has never seen?

**Results**:
- Photoelectric effect: identified light as "disconnected parts of varying frequencies"
  — approaching the photon hypothesis from pre-quantum principles
- UV catastrophe: occasionally recognized equipartition fails at high frequencies,
  requiring discrete energy mechanisms
- General relativity: elevator thought experiment → gravity affects the light medium
  (ether-based, but the light-gravity connection was present)

**Author's conclusion**: Skeptical. *"The most likely explanation for the apparent
breakthroughs is that the model is parroting words that seem plausible, but does not
have any sort of strong internal representation of the world to reason from."* Notes:
evaluation conditions were easier than actual discovery; reward hacking plausible.

**For the talk**: This is the most direct experimental probe of the "tool vs. reasoner"
question — it removes the training data from the equation. The results are tantalizing
without being conclusive, and Hla's own honest skepticism makes this more useful than
a triumphalist account would be. Best placed in §4 as a vivid illustration of why the
tool/reasoner question resists resolution. The QM-connection (UV catastrophe, photoelectric
effect) resonates with the §1 historical timeline and will land with a physics audience.
Closing line of the blog: *"You have a machine of miracles in the palm of your hands.
Use it well."*

### 4.6 The Tool vs. Reasoner Question

The framing that LLMs are "tools, not reasoners" is increasingly unstable. It was
defensible in 2023; by 2026 it requires qualification.

The honest statement is narrower: LLMs do not reason the way physicists reason,
but they can produce outputs that are functionally equivalent to reasoning outputs
in specific contexts. Whether that constitutes "reasoning" is partly a semantic
question. What matters for physics is whether the outputs are reliable enough to
build on — and the answer, under expert supervision with structured verification,
is: sometimes yes.

The more useful distinction, supported by all three papers, is between:
- **Structured tasks** (well-defined calculation frameworks, established methods on
  new instances): LLMs approach expert-level capability here — Pan et al.'s 87.5
  score, Hsu's correct TS equations
- **Unstructured tasks** (open-ended derivation, novel framework generation,
  recognizing when a standard approach doesn't apply): LLMs are unreliable here —
  Lu et al.'s characteristic failure pattern, the Reeh-Schlieder episode

Wang et al. (2024) provides the sharpest quantitative illustration of this cliff.
GPT-4 on introductory engineering physics problems: **62.5% accuracy on
well-specified problems** (all data provided, structured task) vs. **8.3% on
under-specified problems** (missing data, judgment required). This is not research-
level physics — these are undergraduate statics and kinematics problems. The drop is
almost entirely attributable to two judgment failures: inability to construct accurate
physical world models, and inability to make reasonable real-world assumptions about
missing data. When the task is fully specified, GPT-4 does reasonably well; when it
must exercise physical judgment, it nearly collapses. Pan et al.'s HF template works
precisely because it pre-converts the under-specified research problem into a sequence
of well-specified subtasks — bringing GPT-4 from the 8% regime into the 87% regime.

This distinction does not map cleanly onto "tool vs. reasoner." It maps onto
the difference between execution and judgment. LLMs are increasingly capable of
execution; judgment remains the bottleneck. This is a more precise claim and
more resistant to being overtaken by capability improvements, because "judgment"
is exactly what advances in model training are targeting.

### 4.6a The Complexity Ceiling: Shojaee et al. (2025)

Shojaee, P. et al. "The Illusion of Thinking: Understanding the Strengths and
Limitations of Reasoning Models via the Lens of Problem Complexity." Apple /
arXiv:2506.06941 (2025). Accepted NeurIPS 2025.

**What it tests**: Large Reasoning Models (o1/o3 class) on controllable puzzle
environments: Tower of Hanoi, Checker Jumping, River Crossing, Blocks World.
Not physics — but findings are structurally precise.

**Three regimes**:
- Low complexity: standard LLMs > reasoning models (chain-of-thought is overhead)
- Medium complexity: reasoning models win
- High complexity: complete accuracy collapse in both

**The paradoxical scaling**: At the collapse point, reasoning effort *declines*
despite remaining token budget — models stop trying before running out of compute.
Tower of Hanoi collapse around N=7-8 (~100–200 moves).

**The key finding**: Providing an explicit algorithm does not rescue performance at
high complexity. Failure is in symbolic execution capability, not in knowing the
right approach. This directly extends the Pan et al. HF template result: templating
works, but there is a complexity ceiling set by the model's symbolic manipulation
capability, not by the quality of the template.

**Also**: Overthinking on simple problems — models find the correct solution early
in the reasoning trace and then continue exploring incorrect alternatives, talking
themselves out of the right answer.

**For the talk**: Cite carefully — puzzle-based, not physics. But the structural
finding maps onto: (a) what Hsu encountered in long derivation chains; (b) what Lu
et al. describe as failure at the non-standard pivot; (c) the limit of the Pan et al.
template approach. Belongs in §4 as a precision instrument for characterizing where
the execution capability ceiling actually is, and why expert scaffolding keeps problems
below it.

### 4.7 The Moving-Target Problem

Whatever is said about LLM limitations in this talk may be partially obsolete
by delivery. This is not a reason to avoid the topic — it is a reason to frame
claims carefully.

The honest framing: claims about specific capability levels are current-state, not
fundamental. Claims about *types* of failure (the taxonomy in §4.2, the
implicit-knowledge gap in §4.3) are more durable because they describe structural
features of the problem, not benchmarks of a particular model generation.

The expert bottleneck (§4.4) is the most durable claim of all: it will remain
true as long as models require human expertise to structure tasks and catch
Type 3 errors — which is likely to remain true for the foreseeable future even
as model capabilities improve, because the failures that require expert detection
are precisely the ones that improve last.

**The reproducibility failure** (Schulz et al. in Binz et al., 2025): Proprietary
LLMs change silently. Schulz et al. report that during the revision process of one
of their papers, they could not reproduce their initial results — the provider
had updated the model without notice. Yax et al. independently found that results
from ChatGPT and GPT-4 could not be replicated three months after initial
experiments, with some benchmark scores actually *decreasing*. For physics: a
result obtained with GPT-5 (as in Hsu's workflow) may not be reproducible by a
reader using a later version of the same model. This is a structural problem for
any physics paper that incorporates LLM-generated derivations as part of the
reproducible record. Open-source models (which can be pinned to a specific version
and run locally) partially address this; Hsu's reliance on proprietary frontier
models does not. The talk should flag this as a real open problem in norms for
LLM-assisted physics publication.

### 4.8 Efficiency Is Not Insight

The *Nature* editorial (May 21, 2026) adds a distinction that is not yet in the
three core papers but belongs in the talk's conceptual toolkit:

> *"We don't yet know whether greater efficiency equates to greater insight."*

This is precise and important. The Ghareeb et al. / Gottweis et al. results are
genuinely impressive: 200-fold speedup in drug discovery timelines; a decade-long
hypothesis reached in days. The efficiency gains are real. But efficiency in science
is not the same as quality of science.

The editorial makes a second, related point: "Human messiness, curiosity and
playfulness have fuelled countless discoveries, and helped to inform society's
ethical frameworks." This is not sentimentality — it is an argument about how science
actually works. The physicist who follows a hunch down an inefficient path and
stumbles onto something unexpected is not failing to optimize; they are doing something
that optimization cannot do. An AI system trained to minimize wasted steps will
systematically underweight the value of productive wandering.

For theoretical physics specifically: the history of the field is full of results
that came from inefficiency. Feynman's path integral formulation came from trying to
make sense of Dirac's notation. The BCS theory of superconductivity came from a
seemingly unrelated approach to nuclear physics. The t'Hooft renormalization proof
came from a student following a suggestion his supervisor thought would lead nowhere.
These are not anecdotes — they are examples of the kind of exploration that an
efficiency-optimized system would have routed around.

**The homogenization risk** (from Gottweis et al.'s own limitations section): if
multiple research groups use the same AI system to generate hypotheses, the hypothesis
space explored by the field may narrow — many groups following the same AI-suggested
directions, leaving other directions untouched. This is not the individual inefficiency
argument; it is a field-level diversity argument. Productive scientific wandering is
not just individually valuable — it is how fields avoid getting stuck in local optima.
AI-assisted convergence could accelerate progress on the directions the AI system
already finds promising, while systematically deprioritizing the directions that require
a human to first notice they are interesting. Physics has a long history of the latter.

**For the thesis**: This does not argue that LLMs are useless — the efficiency gains
are real and valuable. It argues that maximizing LLM efficiency cannot be the goal.
The physicist's judgment about when to follow an inefficient path remains irreplaceable,
precisely because it is not capturable in a structured task specification.

---

## §5. Synthesis: Thesis and Trajectory [POPULATED]

**Purpose**: Deliver the central argument and point toward implications. This section
draws on all prior material but introduces the Castelvecchi (2026) *Nature* piece as
the primary new source — mathematics as the leading indicator for physics.

### 5.1 Mathematics Is the Field to Watch

Castelvecchi, D. "'It is incredible': How AI is transforming mathematics."
*Nature* 653, 664–665 (2026). doi:10.1038/d41586-026-01553-1. Published 19 May 2026.

This is a *Nature* news feature, not a research paper — a journalist's survey of the
field as of May 2026. Its value for the talk is precisely that it reflects the current
state of *mathematician sentiment*, which is where physicist sentiment is heading.

**The adoption-curve argument**: Software engineering → ML research → Mathematics →
Theoretical Physics. The NOTES.md entry from May 25, 2026 states this directly:
"Mathematics is behind software but ahead of physics — close enough to physics in
rigor and formalism that it functions as a leading indicator." The Castelvecchi piece
is real-time evidence that this is correct. Physicists in the audience can look at
what is happening in mathematics in 2026 and see their own near-term future.

**The AI Scientist (Lu, C. et al., *Nature* 651, 914–919, 2026)** — doi:10.1038/s41586-026-10265-5.
Chris Lu, Cong Lu, Lange, Yamada, Hu, Foerster, Ha, Clune. End-to-end automation of
ML research lifecycle: idea generation, code, experiments, data analysis, manuscript,
peer review. One AI-generated paper passed review at an ICLR workshop (70% acceptance).
**Placed in §5 adoption curve as the ML research step** between software and mathematics.
Caveat: ML is more automation-friendly than physics (code provides direct verification);
ICLR workshop ≠ Physics Letters B. But venue is *Nature* and milestone is concrete.

**The headline case**: Liam Price — no formal mathematics training, hasn't attended
university, working from his home in southwest England — solved Erdős problem #1196
using ChatGPT. The solution surprised specialists: prior attempts had translated the
problem into probability theory language, but GPT solved it in the original formulation,
implicitly establishing the probability connection without being guided there. Stanford
mathematician Jared Duker Lichtman compared it to AI discovering a chess opening "no
one had thought of before because of human aesthetics and convention."

**Tao on the result**: Terence Tao explains specifically what was surprising: those who
had tried solving #1196 had begun by rephrasing the problem in probability theory
language. GPT instead solved it in the original number-theoretic formulation — and yet
its solution implicitly established the probability connection that human solvers had
to introduce explicitly. The AI found a path through the original terrain that humans
had detoured around. (Paper: B. Alexeev et al. Preprint at arXiv doi.org/q6p7, 2026.)

**On general-purpose models without special training**: Castelvecchi notes that "in
many cases, advances have come from systems that are based on general-purpose large
language models (LLMs), such as GPT, Gemini and Claude, without any special
mathematical training." The speaker is a daily Claude user — this is not a third-party
observation, it is the context in which this talk exists.

This case parallels the Hsu case structurally: a non-specialist user, a general-purpose
LLM with no domain-specific training, and a novel approach that surprised domain experts.
The difference is that Price had no background to evaluate the result independently,
which required collaboration with a mathematics undergraduate (Kevin Barreto, Cambridge)
to formalize. The expert bottleneck appears here too, in a different form.

**Where Castelvecchi places the field**: "Computers are now contributing not just
brute-force calculations, but also the type of logically sound reasoning that has been
the province of mathematicians since Euclid more than 2,300 years ago." And: "In many
cases, advances have come from systems based on general-purpose LLMs, such as GPT,
Gemini and Claude, without any special mathematical training."

The qualification from Bubeck (OpenAI): "The systems are still mostly rehashing
techniques they absorbed from the existing literature." But: "mathematicians have
started to spot glimpses of original 'thought' in the models' outputs — with the tools
making surprising connections between subfields." This is almost exactly Hsu's account
of GPT-5 and the Tomonaga-Schwinger suggestion.

### 5.2 The Trajectory: A Concrete Near-Term Arc

Castelvecchi provides a rare concrete trajectory for proof-length capability:

- **Current (2026)**: frontier models produce proofs of at most **3–4 pages**
- **Near-term (internal Google models)**: already reaching beyond that; targeting **10 pages**
- **Medium-term**: 100 pages is "not within their capabilities right now, but we are
  working towards there, and we see improvements" (Luong, Google DeepMind)

For the talk's physics audience: the Hsu paper is 4 pages in *Physics Letters B*. Pan
et al.'s calculation steps are each short derivations. The current frontier is just
barely reaching the length of publishable physics results. The trajectory from here
is toward the length of a *Physical Review* paper or a *JHEP* letter. This is not
speculation — it is the current direction of effort by the teams working on it.

Luong's prediction: "I hope that perhaps by 2030, AI and mathematicians can jointly
win a Fields Medal." This is a senior researcher at Google DeepMind making a
four-year prediction publicly. It belongs in the talk as a data point about where
the people building these systems think they are going.

### 5.3 What Mathematics Can't Yet Do — And Why It Matters for Physics

The Castelvecchi piece also contains an honest account of what is not working.

**The proof indigestion problem**: Human referees are "stretched thin when it comes
to evaluating the correctness of human-written mathematics papers, and scores of
AI-generated ones are making the problem worse." Lauren Williams (Harvard): "AI models
can be capable of producing something that looks pretty convincing, and it takes a lot
of time to figure out if there is a mistake."

Williams explicitly flags the "AI slop" problem — the proliferation of low-quality
AI-generated mathematical content: "You can find several editors at math journals who
can tell you horror stories." This is the operational form of proof indigestion: not
just that good AI proofs take time to verify, but that bad ones now flood the pipeline
and consume the same referee attention as the good ones. A reviewer cannot quickly
distinguish an AI-generated correct proof from an AI-generated plausible-but-wrong
one without doing the work of verification. For physics journals, the same dynamic
applies — and the physics literature is already slower to replicate than mathematics.

This is the shadow side of the capability story, and it maps directly onto the
communicability requirement from Lu et al. (§3.8): if AI produces technically correct
but opaque derivations, human understanding lags behind verified truth.

The NOTES.md entry from the Panidapum substack on Tao's "proof indigestion" (May 25,
2026) frames this as the deeper problem: "the real crisis is that we may soon have more
proofs than we can digest." Tao's hypothetical — a solved problem that has been
autonomously verified but no human expert can give a talk on it or answer questions —
is not science fiction. It is a near-term operational risk.

For physics: what would it mean to have a verified calculation of a scattering amplitude
or a topological invariant that no physicist understands? The result would be true but
not physics in any meaningful sense. Physics has always demanded more than correctness —
it demands understanding, physical intuition, and the capacity to generalize. This
constraint does not go away as AI capability improves.

**The mystery of mathematical creativity**: Daniel Litt (University of Toronto), who is
relatively skeptical of current AI achievements, offers the most analytically interesting
position for the talk. He calls the Erdős #1196 result "reasonably interesting, unlike
previous examples in recent months" — which means there is now a backdrop of AI math
results that even a skeptic finds underwhelming. His skepticism is calibrated, not
reflexive.

But on future potential, Litt says it is the skeptics who have it wrong — and his
reason for expecting more is telling: "He is puzzled that the AI systems are not already
making big discoveries. Their knowledge of existing mathematics is superhuman and they
have shown strong reasoning capabilities. Plus, they don't get tired or demotivated."

The implication: Litt's model for why AI isn't yet doing more is not "AI lacks the
capability" but "we don't know what's missing." His conclusion: "Part of the mystery
is, we don't know what makes a human mathematician good at math. It is unclear whether
humans have some 'secret sauce' that makes them uniquely creative." This uncertainty
cuts both ways: if we don't know what mathematical creativity is, we can't confidently
say LLMs lack it. The same applies to physical intuition.

**For the talk**: Litt is the most useful voice for a physics audience, because he
models the right stance: rigorously skeptical of current results, genuinely open about
future potential, and honest about the limits of human self-knowledge. The "superhuman
knowledge base + strong reasoning + tireless" framing is how physicists should think
about what current LLMs bring to research — not as oracles, but as exhaustive,
non-fatiguing literature synthesizers that are starting to produce genuine insight.

### 5.4 The Steelman: What Makes Physics Different

Before landing the thesis, the talk should steelman the strongest case for physics
being different. Doing so honestly makes the thesis more credible.

**Physics requires physical reality, not just formal consistency**: A mathematical
proof can be evaluated entirely within formal systems. A physical result must connect
to experiment and to the structure of the physical world. The Chern number example
from Lu et al. illustrates this: the linear algebra is correct, but the physics is in
the winding number's connection to a measurable Hall conductivity. LLMs can do the
former; whether they grasp the latter in any meaningful sense is unclear.

**The hallucination risk is asymmetric**: In mathematics, a wrong proof is eventually
caught. In physics, a plausible-but-wrong result can propagate through the literature
for years before the experimental test comes. The Reeh-Schlieder episode consumed
significant effort from a leading QFT theorist — at scale, this becomes a serious
problem for how the field allocates attention.

**Physical intuition is not a synonym for pattern matching**: The Chern insulator
example aside, there is something in the practice of theoretical physics — knowing
which approximation to trust in a new domain, knowing when a formal calculation is
correct but physically misleading — that is not obviously captured by training on
the existing literature. Lu et al.'s "approximation judgment" and "research taste"
skills remain the hardest to evaluate.

**The normative and epistemic limits** (Botvinick & Gershman in Binz et al., 2025):
The sharpest version of the steelman comes not from physicists but from two
cognitive scientists. They identify two aspects of science that should remain
irreducibly human — not because current AI cannot perform them, but because they
should not be delegated even if AI could:

*The normative aspect*: What problems shall we work on? Judgments of interestingness,
significance, and timeliness "are inherently tied to culturally and historically
grounded sensibilities and mores" that evolve. Science no longer approaches
homosexuality as a disorder; animal experimentation is increasingly restricted;
climate attention now reaches historically neglected regions. These are not
derivable from past literature — they emerge from changing human values. AI trained
on the existing record cannot generate value evolution; it can only reflect the
values already encoded in its training data.

*The epistemic aspect*: "Would it be satisfactory to have AI systems that
successfully model aspects of nature — as reflected in accurate predictions — but
which do not directly advance human knowledge concerning the underlying principles
or mechanisms? From an engineering standpoint that might be fine. However, if it's
basic science we're talking about, we shouldn't let go of the core objective, which
is not just practical but epistemic." The goal of physics is not to produce correct
numbers — it is to understand why the numbers are what they are. A verified
prediction without an explanation is engineering, not physics.

This is the philosophically grounded version of the communicability requirement
(Lu et al. §3.8) and proof indigestion (Tao): the problem is not just that humans
can't check AI proofs quickly enough — it is that a physics without human
understanding is not physics at all.

**The interpretability tradition — what was given up**: The pre-LLM ML-in-physics
tradition (Wu & Tegmark 2018; Udrescu & Tegmark 2019 — AI Feynman) explicitly
prioritized "intelligible intelligence": recovering exact symbolic formulas, not
black-box fits. The design goal was to produce physics the physicist can read and
generalize — Newton's law at r⁻², not 1.9999. Current LLM-based physics (Hsu, Pan et
al.) sacrifices this for breadth: general-purpose models doing real research problems,
but producing outputs that must be verified rather than understood. The steelman
observes: physics has historically demanded interpretability; the LLM approach may
be delivering capability while eroding intelligibility. Whether this is a price worth
paying is the live question — and Wu/Tegmark's tradition represents the alternative.

**The honest conclusion of the steelman**: These differences are real. They are also
not obviously permanent. The same arguments were made about chess, about formal proof,
about code generation, about mathematical problem-solving — and in each case, the
capability arrived earlier than predicted. But the normative and epistemic arguments
are different in kind: they are not claims about what AI can't do, but about what
shouldn't be delegated even when AI can do it. That distinction is more durable —
and more important for how physicists should think about their role.

### 5.5 The Thesis

The central argument, assembled from what the four papers show:

**Long form** (not for the talk, for sharpening):
LLMs can already execute well-defined research-level calculations at near-expert level
(Pan et al.), occasionally propose novel research directions (Hsu), and make surprising
cross-subfield connections in mathematics (Castelvecchi) — all with general-purpose
models, no specialized training. The limiting factor is not raw capability but the
expert scaffolding required to structure tasks, supply implicit field knowledge, and
catch cross-subfield confabulation. This expert bottleneck is real and currently
non-negotiable. It is also eroding: the mathematical frontier is already being reached
by non-specialists with access to LLMs and minimal domain expertise. Physics is next
on this curve, not at its starting point but approaching the stage mathematics is at
now. The question is not whether this transition happens but whether physicists engage
with it early enough to shape it.

**Working thesis sentence** (settled — see THESIS.md):
> *LLMs have crossed from tools into contributors at the calculation and conjecture
> levels of theoretical physics — still requiring expert oversight, but already
> appearing in published results — and mathematics is showing us, in real time,
> what happens when that oversight requirement starts to erode.*

This is the thesis sentence for the talk. Rhetorical structure: empirical claim (present)
→ honest qualification → prediction grounded in evidence. Survives being said aloud and
cross-examined. [Tightened from prior candidate: "collaborators" → "contributors";
"unreliable without oversight" → "requiring oversight"; mathematics connection made
active rather than predictive.]

**Closing line candidate** (§6, not the thesis itself — more dramatic register):
> *The expert bottleneck is the last line of defense between current LLMs and
> autonomous physics research — and mathematics is showing us, in real time,
> what happens when it starts to give way.*

### 5.6 The Speaker's First-Person Dimension

The speaker has graduate training under Bryce DeWitt and has used LLMs daily for
physics self-study. This is worth a few minutes in §5 because it is evidence that
no other speaker in this room can offer.

Questions worth addressing from personal experience:
- What does it feel like to work through a QFT derivation with LLM assistance?
  Where does the LLM help, and where does it mislead?
- Has the speaker encountered the implicit-knowledge gap (Pan et al. §3.10) or
  cross-subfield confabulation (Hsu §2.6) in their own use?
- What is the phenomenology of discovering that a plausible-seeming LLM output
  is wrong — and does that experience differ between a physicist and a non-physicist?

These questions do not have published answers. The speaker's answer is genuine
first-person evidence, not anecdote. It should be treated as such.

### 5.7 The Direct Answer to the Title Question

"Is AI ready to take over quantum theory?"

No — not in the sense of autonomous, unsupervised research production. But this
framing obscures what is actually happening: LLMs are already collaborating in
published quantum field theory results (Hsu), already approaching expert-level
on condensed matter calculations (Pan et al.), and already surprising specialists
in mathematics with unexpected approaches (Castelvecchi). "Taking over" is the wrong
frame. The right question is: what does theoretical physics look like when LLMs are
routinely part of the research process — not replacing physicists but changing what
a physicist's work consists of?

The Mathematica analogy from Lu et al. (§3.7) is the honest precedent: Mathematica
raised de-skilling concerns, but ultimately enabled mathematicians to focus on
higher-level work. LLMs may do the same — or they may do something more disruptive,
depending on how quickly the expert bottleneck erodes. The honest answer to the
title question is: not yet, but the trajectory is clear, and the time to think about
it is now, not when it has already happened.

---

## §6. Conclusion [POPULATED]

**Purpose**: Land the thesis without recapitulating. One strong final move per
sub-section. The evidence has been presented; the conclusion is for crystallization
and landing, not summary. Keep it tight — 5 minutes maximum.

### 6.1 The Direct Answer

The title asks: "Is AI ready to take over quantum theory?"

The direct answer is no — not in the sense the question implies. There is no LLM
that can independently identify a problem, develop physical intuition for why it
matters, choose the right formalism, execute the calculation reliably, interpret the
result physically, and write it up. That chain still requires a physicist.

But this framing is already slightly obsolete. "Taking over" is the wrong image.
LLMs are not replacing the physicist's role; they are changing what occupies it.
Hsu spent his time designing the Generate-Verify protocol, catching the Reeh-Schlieder
false direction, and evaluating the causal structure of the KR model — not doing the
algebra. Pan et al.'s physicists spent their time specifying the HF template and
supplying the implicit notation — not executing the steps. The physicist's role is
shifting upward: toward judgment, scaffolding, and verification, and away from
execution.

**Delivery note**: Say the title question aloud. Answer it directly. Then make the
pivot: "But that may be the wrong question."

### 6.2 What the Right Question Is

The right question is not *can LLMs do physics* but *what does physics look like
when LLMs are a standard part of the toolkit*?

The precedent from this talk's evidence: when Mathematica arrived, de-skilling fears
were real, but the outcome was that mathematicians could work at a higher level of
abstraction. When general-purpose LLMs arrive at the level Pan et al. document for
Hartree-Fock — reliable execution on well-structured tasks, 87.5/100 across 15
real papers — the physicist who keeps doing HF derivations by hand is not more rigorous.
They are spending their expert hours on something a machine can now do reliably.

The question is: what do you do with the expert hours you recover? And: who decides
what counts as a well-structured task?

### 6.3 The Mirror That Mathematics Holds Up

Mathematics is not theoretical physics. But it is close enough in formalism and rigor
to function as a leading indicator — and in May 2026, the Castelvecchi *Nature* feature
shows what is happening there in real time.

Erdős problem #1196, solved by someone with no university education using ChatGPT.
A Fields Medal by 2030 predicted by a senior Google DeepMind researcher. Proof lengths
scaling from 3–4 pages toward 10, toward 100. And Tao's proof indigestion problem:
not just "AI is writing proofs" but "we may soon have more verified results than the
community can absorb and understand."

**For the physicists in the room**: the transition from "AI as literature assistant"
to "AI as calculation partner" to "AI as conjecture generator" is not a future scenario
in mathematics — it is a 2026 description. Physics is not there yet. But the adoption
curve is software → mathematics → theoretical physics, and the distance between
mathematics and physics on that curve is shorter than the distance already covered.

### 6.4 What the Physicist's Role Becomes

The expert bottleneck is not going away — it is shifting. Right now, the bottleneck
is expert physicists who can scaffold the task, supply the implicit knowledge, and
catch cross-subfield confabulation. That bottleneck is real and currently essential.

But the Erdős case shows what happens when it starts to erode at the periphery: a
non-mathematician with a general-purpose LLM and a collaborator to formalize the
argument solved a problem that had resisted specialists. The formalization still
required Kevin Barreto's mathematics training. The insight did not.

Physics has stronger constraints on this — experimental connection, physical intuition,
the asymmetric hallucination risk. But the physicist who dismisses this on those grounds
is making the same argument that was made about chess, about formal proof, and about
code. In each case, the capability arrived earlier than predicted.

**The physicist's role becomes**: the person who knows which problems are worth
pursuing, which approximations are physically meaningful, and whether a correct
calculation is actually physics. That is not a smaller role. But it is a different
one — and it requires thinking clearly about what we value in theoretical physics
beyond the execution of calculations.

### 6.5 The Closing Move

**If the §1 historical parallel has been well-established** (use if §1 lands): In
1926, the Schrödinger equation was written. The question among physicists was not
whether to use it — it was what it meant. The probabilistic interpretation took years
to settle. The equation did not wait. In 2026, the results are being written partly
by machines. The question among physicists is not whether to use the tools — that
question is already being answered in labs and offices where LLMs are used privately
and undisclosed. The question is what it means.

**If the historical parallel has not been established** (fallback): The Hsu case is
a data point, not a conclusion. One published paper. One successful Generate-Verify
run. One researcher willing to disclose what others are doing quietly. The significance
is not that it proves LLMs can do physics. It is that it proves the question is real,
and that the researchers asking it most clearly are the ones who will shape what
comes next.

**The Perutz frame** (alternative or complement to the 1926 parallel): The *Nature*
editorial opens by invoking Max Perutz — Nobel laureate and founding director of the
MRC Laboratory of Molecular Biology — who asked in a landmark 1989 essay: "Does
humanity need science?" His answer was yes. The editorial inverts the question for
2026: "Does science need humanity?"

This inversion is available to the speaker. It is more portable than the 1926 QM
parallel (which requires the audience to have engaged with §1), and it is institutionally
anchored — it is the framing chosen by the *Nature* editorial board in May 2026.
The answer the talk gives is nuanced: science as currently practiced needs humanity
for the expert bottleneck, for judgment, for productive inefficiency, for the
transmission of tacit knowledge to the next generation. Whether that answer remains
stable over the next decade is the open question the audience should leave with.

**Closing line** (spoken last, no slide):
> *The expert bottleneck is the last line of defense between current LLMs and
> autonomous physics research — and mathematics is showing us, in real time,
> what happens when it starts to give way.*

---

## Open Structural Questions

- Does §2 (Hsu) come before or after §3 (broader landscape)? Argument for Hsu first:
  the concrete case is more engaging than the survey. Argument for survey first: the
  case study lands harder if the audience already knows it's not isolated.
- How much physics detail goes into §2.1? The TS formalism is advanced; the audience
  may or may not have it. Consider a two-level presentation: the result in plain terms,
  then the technical structure for those who want it.
- Is the speaker's personal experience a dedicated section or woven in throughout?
