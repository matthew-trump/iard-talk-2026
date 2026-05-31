# Pan et al. (2025) — Communications Physics
## Tier 1 · Main quantitative evidence

**Full citation**: Pan, L. et al. "Quantum many-body physics calculations with large
language models." *Communications Physics* 8:49 (2025).
doi:10.1038/s42005-025-01956-y.
Cornell / Google Research / Harvard / Google DeepMind.
Submitted September 2024; accepted January 2025.
[Local PDF](../../sources/to_review/pan_et_al_2025.pdf)

---

## What it is

An empirical study with real numbers. GPT-4 executing Hartree-Fock (HF) mean-field
theory derivations on real condensed matter papers, using a structured prompt template
with human expert correction at each step.

---

## The task: Hartree-Fock mean-field theory

The workhorse approximation method of condensed matter physics. Replaces many-body
interactions with mean fields, separating the problem into an analytic derivation of
the HF Hamiltonian H_HF and a computational self-consistency equation.

- Over 6,456 cond-mat arXiv papers reference HF in abstracts in the last decade
- Requires graduate-level knowledge; "years of study to do reliably"
- Five-step procedure: (1) set up Hamiltonian, (2) Fourier transform, (3) apply
  Wick's theorem, (4) simplify quadratic Hamiltonian, (5) identify order parameter structures

---

## Method: The HF template

A multi-step prompt structure decomposing the calculation into 11 sub-tasks, written
like instructions to a beginning graduate student. Each step's output checked by a
human expert before becoming input to the next step (sequential correction).

Tested on 15 real APS-journal papers spanning a decade of condensed matter research.

---

## Key results

| Metric | Result |
|--------|--------|
| Average score (all rubric layers, all papers) | **87.5 / 100** |
| Mathematical Rigor | consistently **above 95** |
| Final H_HF correctly derived | **13 of 15** papers |
| Performance across calculation steps | uniform — not front-loaded |
| Training cutoff (Sep 2021) effect | flat — performance equal before and after |

As a byproduct: GPT-4 **identified typographical errors in published papers** —
computing intermediate steps the papers didn't show and finding the printed answer
inconsistent with correct derivation.

---

## The information extraction task

Pan et al. also tested GPT-4 extracting template placeholders directly from paper
excerpts (eliminating the human setup step):

- **High scores**: system-specific information; explicit notation stated in the paper
- **Poor scores**: implicit notation — field conventions every practitioner knows,
  no paper writes down (standard Fourier transform convention, second-quantized
  operator conventions, fermionic statistics handling)
- One-shot prompting (one example excerpt + correct extraction) jumped one task
  from **44 ± 8** to **80 ± 6**

Most ambitiously: from just an abstract and 10 guided questions, GPT-4 could sometimes
infer system-specific information and carry out the full HF derivation.

---

## What this establishes

The calculational execution layer of theoretical physics is **largely within reach**
of current LLMs when the task is appropriately structured. The ceiling on this
capability, within a well-structured template, is close to human expert level.

**The key limitation**: The HF template was designed by expert condensed matter
physicists. GPT-4 executes inside the framework brilliantly. The template design
is not automated.

**The Wang et al. connection**: Pan et al.'s 87.5% is achievable precisely because
the HF template converts under-specified research problems into well-specified
sub-tasks. Wang et al.'s 62.5% / 8.3% cliff shows what performance looks like
without that conversion (see `09_wang_et_al_2024.md`).

---

## Key framing for the talk

- Pan et al. = Stage 3 in the Lu et al. taxonomy (analytical derivation and computation)
- Hsu = Stage 2 (hypothesis formulation). Different modes of contribution; both real.
- The template designer is the physicist: "Without the template: 8.3% regime. With
  the template: 87.5% regime. The template is the physicist."

---

## Where it appears in the talk

§3 (Stage 3 calculation execution section, full treatment). Referenced in §4
(expert bottleneck, execution/judgment cliff), §5 (thesis parsing).
