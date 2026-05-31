# Gottweis et al. (2026) — Nature (Co-Scientist)
## Tier 2 · Two days vs. a decade

**Full citation**: Gottweis, J. et al. "Accelerating scientific discovery with
Co-Scientist." *Nature* doi:10.1038/s41586-026-10644-y (2026).
Google Cloud AI Research / Google DeepMind / Google Research / Stanford /
Imperial College London.
[Local PDF](../../sources/to_review/gottweiss_et_al_2025.pdf)

---

## What it is

A multi-agent AI system (Co-Scientist) built on Google's Gemini, designed as a
"structured scientific thinking engine." Not a chatbot or literature assistant —
specialized agents that cooperate to generate and refine research hypotheses.

---

## Architecture

**Agents**: Generation, Reflection, Ranking, Evolution, Proximity, Meta-review.

**Core mechanism**: "generate, debate, evolve" paradigm:
1. Agents generate candidate hypotheses
2. Internal self-play debate evaluates them
3. Tournament ranks hypotheses
4. Top candidates evolved through iterative refinement

**Critical property**: Hypothesis quality improves **monotonically with compute time** —
more thinking time produces better hypotheses, with no saturation observed.
Test-time compute scaling applied to scientific reasoning.

**Scientist-in-the-loop by design**: Explicitly "purpose-built for a
'scientist-in-the-loop' collaborative paradigm." Scientists specify goals in natural
language, inject initial hypotheses, give feedback via chat, prioritize outputs.
Experimental validation handed to human wet-lab scientists. "All three validations
involved expert-in-the-loop."

---

## Three validation cases

### 1. AML drug repurposing (acute myeloid leukemia)

Searched 2,300 approved drugs across 34 cancer types. Suggested 5 candidates for
wet-lab validation; 3 showed cell viability inhibition.

- **Binimetinib**: IC50 as low as 2 nM in AML cell lines; significantly higher in
  non-AML control — selective cytotoxicity at clinically relevant concentrations
- **KIRA6** (IRE1α inhibitor): 18-fold IC50 separation between sensitive AML line
  (KG-1a, 10 nM) and non-AML control (TK6, 180 nM)
- Proposed synergistic drug combinations confirmed predominantly synergistic in vitro

### 2. Liver fibrosis

Proposed novel epigenetic targets. Two of three tested showed significant anti-fibrotic
activity in human hepatic organoids. **Vorinostat** (FDA-approved for cancer):
repurposing opportunity via cross-domain connection.

### 3. Antimicrobial resistance — the structurally parallel case

**The question**: How do capsid-forming phage-inducible chromosomal islands (cf-PICIs)
— mobile genetic elements carrying antibiotic resistance genes — achieve broad host
range across bacterial species?

**What Co-Scientist was given**: Only minimal background information.

**In two days**: Co-Scientist independently proposed that cf-PICIs interact with diverse
phage tails to expand their host range.

**The comparison**: This precisely matched the primary finding of an independent
experimental study that had been working on the same question for approximately
**a decade** — and published simultaneously as a co-timed report.

**Two days. A decade.**

This is the structural parallel to the Hsu case: expert-defined problem → AI given
minimal framing → hypothesis matching what domain experts concluded through years of
investigation.

---

## Architecture comparison (for §4.5 in talk)

| Framework | Structure | Human role |
|-----------|-----------|------------|
| Hsu (Generate-Verify) | Two LLM instances | Human physicist structures task, catches errors, judges novelty |
| Lu et al. (Deriver-Critic) | Critic checks without seeing generation artifacts | Expert physicist directs and evaluates |
| Pan et al. (Sequential correction) | Human expert checks each step | Expert corrects between every step |
| Co-Scientist | Multi-agent internal debate and tournament | Scientist specifies goal, provides feedback, validates experiments |

Co-Scientist is the most autonomous — internal debate replaces much step-by-step
human review. But the scientist-in-the-loop remains essential for goal specification,
prioritization, and experimental validation.

---

## Evaluation

On 203 research goals (predominantly biomedical, also including mathematics and
physics goals): monotonic improvement with compute time. On 15 expert-curated
challenging goals: outperformed Gemini 2.0 Pro, Flash Thinking, o1, o3-mini, and
DeepSeek R1 by expert preference ranking.

---

## Limitations (stated by the authors — important for talk's honesty)

- Knowledge constrained by **open-access literature** — no access to paywalled content
  or negative/failed experimental results; systematic bias toward published positive findings
- **Propagation risk**: relies on source literature quality; can amplify erroneous or
  irreproducible findings already in the literature
- **Homogenization risk**: "risk of diminishing critical thinking or homogenizing research
  directions" — if many researchers use the same AI system, the hypothesis space explored
  by the field may narrow
- Inherits LLM limitations: imperfect factuality, hallucinations
- Wet-lab validations are preliminary

---

## The homogenization risk for physics

If multiple research groups use the same AI system to suggest what problems to pursue,
the effect is not amplified serendipity but convergent search — many groups following
the same AI-suggested directions, leaving other directions unexplored. Physics has a
long history of results that required a human to first notice an apparently
unpromising direction was interesting. AI-assisted convergence could systematically
deprioritize those directions.

---

## Where it appears in the talk

§3 (Robin/Co-Scientist section — the two-days/decade comparison). §4 (efficiency is
not insight — homogenization risk). §5 (adoption curve context).
