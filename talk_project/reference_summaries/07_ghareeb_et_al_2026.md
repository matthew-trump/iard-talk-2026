# Ghareeb et al. (2026) — Nature (Robin)
## Tier 2 · The 44.5% number and the controlled comparison

**Full citation**: Ghareeb, A.E. et al. "A multi-agent system for automating
scientific discovery." *Nature* doi:10.1038/s41586-026-10652-y (2026).
FutureHouse / Fordham University / University of Oxford.
[Local PDF](../../sources/to_review/ghareeb_et_al_2025.pdf)

---

## What it is

A multi-agent AI system (Robin) applied to drug discovery for dry age-related macular
degeneration (dAMD), the leading cause of blindness in the developed world.
Lab-in-the-loop architecture: Robin handles the intellectual steps, humans run the
experiments.

---

## Robin architecture

Three specialized agents in a continuous loop:
- **Crow**: concise literature search via PaperQA2
- **Falcon**: deep literature evaluation
- **Finch**: scientific data analysis in Jupyter notebooks

Workflow: identify relevant in vitro assays → propose drug candidates ranked by LLM
tournament → humans conduct experiments → Robin receives raw data → Robin analyzes
and generates updated hypotheses.

---

## Scientific results (confirmed in vitro)

**Ripasudil** (ROCK inhibitor, already approved for glaucoma in Japan):
- Proposed by Robin for dAMD via phagocytosis enhancement of retinal pigment epithelium
- Application to dAMD **never previously proposed**
- Result: **1.89-fold** increase in RPE cell phagocytosis (1.75-fold in independent
  human analysis)
- Mechanism existed in literature (ROCK inhibition enhances phagocytosis;
  phagocytic dysfunction present in dAMD) but the connection had never been made

**KL001** (circadian clock modulator):
- Proposed based on circadian control of RPE phagocytosis
- Confirmed hit
- "To our knowledge no one has previously proposed KL001 as an enhancer of phagocytosis"

**ABCA1 upregulation** (Finch RNA-seq analysis):
- 3-fold upregulation, p = 2.13×10⁻⁸³
- Possible novel mechanistic target "that might have otherwise remained unexplored"

---

## The 200-fold speedup — actual numbers

| Metric | Value |
|--------|-------|
| Papers analyzed by Robin | 551 in 30 minutes |
| Human equivalent | ~540 hours |
| Total cognitive labor per cycle | 872–937 human hours → under 2 hours |
| Cost per Robin run | $10.76 (45 Crow + 30 Falcon calls) |

---

## The Deep Research control — the most important comparison

Same drug generation prompt given to OpenAI Deep Research (powerful general-purpose
multi-step research agent). Deep Research generated 17 unique candidates.
**None were hits in the RPE phagocytosis assay.** Deep Research did not suggest
ROCK inhibition as a mechanism.

This is a controlled within-paper comparison demonstrating that the literature-grounded
architecture (Crow/Falcon) adds genuine value beyond what a generic powerful LLM
agent produces — not just a better model, but a better architecture.

---

## Hallucination rates — the sharpest quantitative number in the talk

When Crow/Falcon were ablated and replaced with raw o4-mini calls:
- **44.5 ± 6.4%** of references in drug candidate reports were hallucinated (fabricated)

With full Robin architecture (Crow + Falcon):
- **0%** hallucinated references

This is the sharpest available quantitative measure of:
(a) The severity of the hallucination problem in unmitigated scientific LLM use
(b) How far mitigation can go with the right architecture

For physics: a hallucinated reference is indistinguishable from a real citation in
the output text, and a plausible-sounding fake result can propagate into subsequent
reasoning.

---

## Finch BixBench performance

On 170 expert-generated bioinformatics/statistics question-answer pairs:
- Finch (with agent harness): **22.8 ± 1.7%**
- Claude Sonnet 3.7 alone: **1.6 ± 1.2%**
- Finch on single-step statistics: 47.9% vs. 15.3% on multi-step bioinformatics

The single-step/multi-step gap maps onto Wang et al.'s well-specified/under-specified
cliff.

---

## "Combinatorial synthesis" framing

Robin's authors describe what it does as identifying non-obvious connections between
disparate fields that human experts overlook due to knowledge compartmentalization.
The ripasudil insight existed in the literature in two separate places but had never
been connected to dAMD therapeutics. Robin connected them.

This is the productive version of what Lu et al. call cross-subfield connection —
the same mechanism that enables LLM confabulation (Hsu's Reeh-Schlieder episode)
also enables genuine cross-domain synthesis when the literature grounding is reliable.
**The difference is verifiability.**

---

## Where it appears in the talk

§3 (Stage 1 literature synthesis, Robin/Co-Scientist section; hallucination number).
§4 (citation hallucination quantified; expert bottleneck "feature not a bug").
