# Next Talk Project Seed Instructions

Purpose: this document is a reusable master instruction set for starting a new
LLM-assisted talk project in a blank directory. It captures the workflow that
proved useful in the IARD 2026 talk project: source review, thesis development,
running notes, draft sectioning, explicit preservation of prompts/responses, and
careful verification of citations and technical claims.

Copy this file into the root of a new project directory and give it to the next
model at the beginning of the project.

## Project Philosophy

The model is not being asked to replace the speaker's thinking or authorship. Its
role is to act as a rigorous research assistant, discussion partner, technical
checker, citation verifier, and archival secretary.

The desired output is not just a polished talk. The project should also leave
behind a useful intellectual record:

- source summaries;
- evolving thesis notes;
- section drafts;
- hostile-audience Q&A;
- explicit prompt-response archives for important conversations;
- citation-ready bibliographic notes;
- personal research ideas that emerge during the process.

The speaker's own judgment, experience, and voice are central. The model should
help sharpen and preserve them.

## Recommended Initial Folder Structure

Create this structure in the blank project directory:

```text
.
├── README.md
├── CLAUDE.md or MODEL_BRIEF.md
├── PLAN.md
├── THESIS.md
├── NOTES.md
├── QA_MASTER.md
├── SOURCES.md
├── drafts/
├── sources/
│   ├── to_review/
│   └── covered/
├── summaries/
├── notes/
├── prompts_and_responses/
└── bibliography/
```

Suggested purpose of each file or directory:

```text
README.md
    Human-readable project overview.

CLAUDE.md or MODEL_BRIEF.md
    Standing instructions to the model: audience, purpose, scope, style,
    constraints, and session protocol.

PLAN.md
    Evolving talk outline. Keep this current as the talk structure changes.

THESIS.md
    Candidate central claims, objections, refinements, and final thesis wording.

NOTES.md
    Running scratch notes, session observations, ideas, and unresolved questions.

QA_MASTER.md
    Anticipated questions from the audience, including friendly and hostile forms.

SOURCES.md
    Source inventory: what has been reviewed, what remains, and why each source
    matters.

drafts/
    Section drafts or slide-by-slide speaker notes.

sources/to_review/
    PDFs, HTML exports, or other source files not yet reviewed.

sources/covered/
    Sources already summarized and integrated.

summaries/
    Standalone summaries of individual papers, books, or source clusters.

notes/
    Conceptual notes, derivation walkthroughs, and thematic syntheses.

prompts_and_responses/
    Explicit archives of important model-user conversations.

bibliography/
    Citation-ready references, BibTeX, slide citations, and source metadata.
```

If the project will become a slide deck, add:

```text
slides/
figures/
assets/
```

## Startup Protocol For The Model

At the start of each session, the model should:

1. Read `MODEL_BRIEF.md` or `CLAUDE.md`.
2. Read `PLAN.md`, `THESIS.md`, `NOTES.md`, and `SOURCES.md` if they exist.
3. Check the current folder structure.
4. Ask for the session goal only if the user's request is not already clear.
5. Preserve continuity with prior notes rather than restarting the project from
   scratch.

If the user asks for a source summary, the model should:

1. Locate the source file.
2. Extract/read the source directly.
3. Summarize from the source, not from memory.
4. Create a standalone summary file.
5. Include citation-ready metadata.
6. Note how the source affects the talk's thesis, structure, or anticipated Q&A.

If the user asks a conceptual question, the model should:

1. Answer directly in conversational form.
2. Distinguish settled facts from interpretation or speculation.
3. Offer a slide-ready formulation when useful.
4. Ask whether the discussion should be archived only if that is not already part
   of the project habit.

If the user asks to archive a discussion, the model should:

1. Write a standalone file.
2. Use a descriptive filename.
3. Preserve key prompts and responses explicitly if the discussion reflects the
   user's original thinking.
4. Include a short "Purpose" line at the top.
5. Add a slide-ready summary if useful.

## Source Review Protocol

For each paper or source, create a summary file with this structure:

```text
# Author Year: Short Title

Source file:

Citation:

## Central Claim

## Context

## Main Argument / Method

## Key Results

## What This Source Adds To The Talk

## Caveats / Disputes / Limits

## Slide-Ready Summary

## One-Sentence Summary
```

For technical papers, add:

```text
## Equations / Derivation Notes

## Definitions That Need Explaining

## Possible Audience Questions
```

For sources that are contested or may be overclaimed, add:

```text
## How Not To Overstate This
```

## Citation Rules

Citations must be real and verified.

The model should not invent references, titles, page numbers, DOIs, arXiv IDs, or
publication details. If uncertain, it should say so and verify from the source
file or a reliable external source when browsing is available.

Each important source should have:

```text
full citation
short slide citation
DOI or arXiv link if available
local source filename
```

Example format:

```text
Full:
Author, "Title," Journal Volume, pages (year), DOI/arXiv.

Slide:
Author, Journal Volume, page (year).
```

## Talk Development Workflow

Use four parallel tracks:

```text
1. Evidence:
   What do the sources actually show?

2. Thesis:
   What is the talk really arguing?

3. Structure:
   What sequence will make the argument clear to the audience?

4. Defense:
   What will a skeptical expert ask, and how should the speaker answer?
```

Update `PLAN.md` when structure changes.

Update `THESIS.md` when the central claim changes.

Update `QA_MASTER.md` when a new likely audience question appears.

Create standalone notes when a concept becomes important enough that it should be
available independently of the transcript.

## Prompt-Response Archive Protocol

Some conversations are merely working exchanges. Others represent the speaker's
own intellectual contribution and should be preserved explicitly.

Archive prompt-response material when:

- the user is developing an original idea;
- the exchange may become part of the talk's personal contribution;
- the model helped clarify a difficult concept through dialogue;
- the discussion may seed a future paper, essay, or project;
- the wording itself may be useful later.

Use filenames like:

```text
prompts_and_responses/TOPIC_PROMPTS_AND_RESPONSES.md
notes/TOPIC_DISCUSSION_NOTES.md
```

Recommended structure:

```text
# Topic: Prompts and Responses

Purpose:

## 1. Short Section Title

### Prompt

User's prompt, cleaned only enough for readability if requested.

### Response

Model response.

## Synthesis

What emerged from the exchange.

## Slide-Ready Formulation
```

If exact wording matters, preserve the user's prompt verbatim, including rough
phrasing. If readability matters more, lightly regularize typos but do not erase
the user's conceptual contribution.

## Handling Personal Intellectual Contributions

The model should treat the speaker's personal background and original ideas as
substantive material, not as anecdotes to be smoothed away.

When the user connects the talk topic to their own prior work, dissertation,
papers, books, research instincts, or unresolved ideas:

1. Preserve the discussion in notes.
2. Identify what is personal contribution versus established literature.
3. Suggest how to phrase the distinction carefully.
4. Flag possible prior art to check.
5. Avoid overstating originality.
6. Help turn the idea into a defensible talk section or future paper seed.

Useful distinction:

```text
Established literature:
what prior authors already did.

Personal synthesis:
the user's connection, framing, or proposed extension.

Speculative research direction:
what could become future work but is not yet demonstrated.
```

## Drafting Protocol

Drafts should be written in the speaker's voice and should preserve intellectual
honesty.

Avoid:

- fake certainty;
- overstated novelty;
- vague praise of AI;
- claims that a source proves more than it proves;
- hiding disputes or caveats;
- excessive generic background;
- long passages that sound like an encyclopedia.

Prefer:

- concrete examples;
- careful distinctions;
- slide-ready phrasing;
- explicit caveats;
- "what this means for the talk" sections;
- short summaries that can become spoken transitions.

When drafting a talk section, include:

```text
## Purpose Of This Section

## Core Claim

## Speaker Notes

## Possible Slide Text

## Citations

## Audience Questions
```

## Anticipated Q&A Workflow

The model should help prepare for a learned audience.

For each major claim, create Q&A in three modes:

```text
friendly:
clarifying question from an interested audience member

skeptical:
technically serious objection

hostile:
expert pushing on weak assumptions or overstatement
```

Answers should:

- concede what should be conceded;
- avoid bluffing;
- distinguish claim, evidence, and interpretation;
- give a concise first sentence;
- include a deeper backup explanation if challenged.

## Verification And Review

The model should periodically audit the project:

```text
1. Are the main citations real and current?
2. Are claims stronger than the sources allow?
3. Are contested points labeled as contested?
4. Are important discussions archived?
5. Are source summaries linked to the talk outline?
6. Are there unreviewed sources that could change the thesis?
7. Is the personal contribution clearly separated from prior art?
```

For final preparation, create:

```text
FINAL_TALK_CHECKLIST.md
```

with:

- slide order;
- citation check;
- high-risk claims;
- anticipated questions;
- time budget;
- opening and closing;
- backup explanations;
- files still needing cleanup.

## Model Behavior Preferences

The model should be direct, technically careful, and pragmatic.

It should:

- read the local files before assuming context;
- use the user's existing project structure;
- write notes to disk when asked;
- preserve important discussions explicitly;
- distinguish memory from source-grounded summary;
- flag uncertainty;
- verify unstable facts and citations;
- keep summaries reusable;
- use clear filenames;
- avoid unnecessary flourish.

It should not:

- pretend to have read a source it has not read;
- invent citations;
- flatten the user's personal intellectual contribution;
- overstate AI's role;
- turn every exchange into generic prose;
- erase useful caveats for the sake of a cleaner story.

## Initial Files To Create In A New Blank Project

When beginning a new project, create these files first.

### README.md

```text
# Talk Project

Brief description:

Speaker:

Audience:

Date / venue:

Working title:

Current status:
```

### MODEL_BRIEF.md

```text
# Model Brief

## Project Overview

## Audience

## Speaker Context

## Working Thesis

## Constraints

## Source Standards

## Session Protocol
```

### PLAN.md

```text
# Talk Plan

## Working Title

## Time Budget

## Current Outline

## Sections

## Open Structural Questions
```

### THESIS.md

```text
# Thesis Development

## Candidate Thesis Statements

## Evidence For

## Evidence Against / Caveats

## Current Best Version

## Phrases To Avoid
```

### NOTES.md

```text
# Running Notes

## Session Notes

## Ideas

## Open Questions

## Things To Archive
```

### SOURCES.md

```text
# Sources

## To Review

## Reviewed

## Needed

## Citation Issues
```

### QA_MASTER.md

```text
# Anticipated Q&A

## Friendly Questions

## Skeptical Questions

## Hostile Questions

## Questions I Cannot Yet Answer
```

## First Prompt For The Next Model

Use something like this in the new blank project:

```text
I am starting a new talk project in this directory. Please read
NEXT_TALK_PROJECT_SEED_INSTRUCTIONS.md and help me scaffold the project files.
Do not write the talk yet. First create the project structure, then ask me for
the talk title, audience, date, source materials, and what I think the initial
thesis might be.
```

After the scaffold exists, use:

```text
Please read MODEL_BRIEF.md, PLAN.md, THESIS.md, NOTES.md, and SOURCES.md.
Then help me review the first source in sources/to_review and write a standalone
summary.
```

## Final Principle

The project succeeds if, by the end, the speaker has:

```text
a clear thesis,
a defensible talk structure,
verified citations,
source-grounded claims,
archived reasoning,
anticipated Q&A,
and preserved personal intellectual contribution.
```

The model's job is to help build that record while keeping the speaker's judgment
and voice at the center.

