# CLAUDE.md — Physics Conference Talk
## LLMs in Theoretical Physics Research: A Review

---

## Project Overview

This project is a **longer invited review talk** for a mixed-audience physics conference
(estimated 45–60 minutes). The subject is recent developments in the use of large language
models (LLMs) in theoretical physics research. The speaker has extensive physics background
(graduate study under Bryce DeWitt; deep self-study in QFT, classical EM, Hamilton-Jacobi
theory, quaternion formalism, and related areas) and is also a sophisticated daily user of
LLMs, which gives the talk an unusual first-person credibility dimension worth exploiting.

---

## Current Status

- **Thesis**: Not yet settled. Thesis development is an explicit early goal of this project.
  Claude should actively help identify and sharpen a defensible central argument as literature
  review and note synthesis proceed. Working assumption: the thesis will likely be nuanced
  (LLMs are useful in specific ways, limited or misleading in others) rather than simply
  optimistic or dismissive.

- **Source material**: Uneven. Some areas of the literature are covered; others need
  systematic review. Bibliography development is an ongoing task.

- **Timeline**: Talk is approximately one month out.

---

## Audience

Mixed physicists at a conference — ranging from specialists in subfields to generalists.
Assume mathematical sophistication but no prior familiarity with LLM internals or ML
research. The talk should not condescend to physicists on physics, but also should not
assume they have thought carefully about what LLMs can and cannot do.

---

## Folder Structure

```
talk-project/
├── CLAUDE.md          ← this file: project context, goals, constraints
├── PLAN.md            ← evolving talk outline and structure
├── NOTES.md           ← running scratch notes, ideas, observations from sessions
├── THESIS.md          ← thesis development: candidate arguments, evidence, tensions
├── sources/           ← PDFs and reference papers
│   ├── covered/       ← sources already reviewed
│   └── to-review/     ← sources queued for review
└── drafts/            ← section drafts as they develop
```

---

## Key Questions to Resolve (Early Priority)

1. **Thesis**: What is the central, defensible argument? Options include:
   - LLMs as literature/synthesis tools vs. as reasoning engines — the distinction matters
   - Where do LLMs fail specifically in theoretical physics (symbolic reasoning, rigor,
     hallucinated citations, false confidence on open problems)?
   - Is there a meaningful difference between LLM-assisted physics and prior computational
     tools (CAS, numeric simulation)?
   - What does the speaker's own experience contribute to the argument?

2. **Scope**: Which subdomains of theoretical physics have seen the most LLM activity?
   (Candidates: string theory / landscape navigation, formal QFT, condensed matter,
   quantum gravity, mathematical physics, symbolic computation assistance.)

3. **Structure**: Review talk vs. argued essay vs. personal reflection with evidence?
   A pure literature review risks being flat. Consider a hybrid: structured review with
   an explicit evaluative frame.

---

## Constraints and Preferences

- The speaker prefers **load-bearing analogies and geometric intuition** over abstract
  formalism when explaining LLM concepts to a physics audience.
- The talk should avoid both uncritical boosterism and reflexive dismissal.
- Citations must be real and verifiable — hallucinated references are especially
  embarrassing given the subject matter.
- The speaker's personal experience using LLMs for physics self-study is a legitimate
  and distinctive source of evidence; do not treat it as merely anecdotal.

---

## Claude's Role in This Project

- **Synthesis and analysis**: Help identify patterns, tensions, and arguments across sources.
- **Thesis development**: Actively propose, stress-test, and refine candidate thesis arguments.
- **Outline structuring**: Help build and revise PLAN.md as understanding develops.
- **Literature gaps**: Flag areas where source coverage is thin and suggest search strategies.
- **Draft review**: Review section drafts for argument clarity, accuracy, and audience fit.
- **NOT ghostwriting**: The speaker writes the actual talk. Claude is a research and
  thinking partner, not a content generator.

---

## Session Protocol

At the start of each session, Claude should:
1. Read CLAUDE.md, PLAN.md, NOTES.md, and THESIS.md before doing anything else.
2. Ask what the session goal is if not stated.
3. Flag any new tensions or opportunities noticed across documents.

At the end of each session, Claude should:
1. Summarize what was accomplished.
2. Suggest 2–3 concrete next steps.
3. Note any open questions that should be captured in NOTES.md or THESIS.md.
