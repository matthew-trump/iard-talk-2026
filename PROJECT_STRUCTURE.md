# Project Structure

Purpose: define the repository as a larger ongoing research/writing project, not
only as the archive of one delivered talk.

The project is organized around one shared pool of references, plus multiple
artifacts and side quests.

## Core Idea

The larger project is defined by a shared reference pool:

```text
sources/
talk_project/MASTER_CITATIONS.md
summaries/
bibliography/
```

Specific outputs are **artifacts**:

```text
artifacts/iard-2026-talk/
```

Exploratory research directions are **side quests**:

```text
side_quests/nlqm/
```

This lets the same repository support:

```text
conference talks
proceedings papers
preprints
technical side investigations
future talks
methodological notes on LLM-assisted research
```

## Shared Reference Pool

References remain shared for now.

```text
sources/to_review/
    New PDFs, HTML exports, and source files waiting to be digested.

sources/covered/
    Sources already reviewed.

talk_project/MASTER_CITATIONS.md
    Slide-ready and bibliography-ready citation list.

summaries/general/
    General-purpose summaries useful across multiple artifacts.

summaries/artifact_specific/
    Summaries written for a particular talk or paper.

summaries/side_quests/
    Summaries written for exploratory side investigations.

bibliography/
    Future home for BibTeX, CSL, reference exports, or final bibliography files.
```

Reference summaries can belong to more than one context. For example, a Weinberg
summary may be useful for the delivered IARD talk, the proceedings paper, and the
NLQM side quest. Do not duplicate unless the artifact-specific framing is genuinely
different.

## Artifacts

Artifacts are concrete outputs: a talk, slide deck, paper, proceedings article,
essay, or preprint.

Current first artifact:

```text
artifacts/iard-2026-talk/
```

Artifact directories may contain:

```text
slides/
    Keynote, PowerPoint, PDF exports, images, and slide-specific assets.

drafts/
    Speaker notes, proceedings drafts, paper drafts tied to this artifact.

qa/
    Audience-specific Q&A for this artifact.

notes/
    Notes specific to this artifact's framing, delivery, and aftermath.

proceedings/
    IARD proceedings draft if developed.
```

The existing root-level `drafts/` and `talk_project/` directories are retained for
continuity. Future work can gradually migrate material into artifact directories
when useful, but no move is required until there is a clear benefit.

## Side Quests

Side quests are exploratory research lines that arise from the project but are not
identical with any single artifact.

Current first side quest:

```text
side_quests/nlqm/
```

NLQM means nonlinear quantum mechanics. This side quest includes the Weinberg 1989
rabbit hole, Polchinski/Gisin, Ho-Hsu 2014, Hsu 2026, Diósi's comment, Kaplan-
Rajendran, Tomonaga-Schwinger covariance, and related questions about nonlinear
state-dependent Hamiltonian evolution.

Side quest directories may contain:

```text
notes/
    Conceptual notes, derivation walkthroughs, question logs.

drafts/
    Possible paper sections, speculative essays, future talk sections.

qa/
    Expert objections and self-interrogation.
```

Side quests may later become artifacts. For example:

```text
side_quests/nlqm/
    -> artifacts/nlqm-paper/
    -> artifacts/nlqm-talk-2028/
```

## Where To Put New Material

Use this rule of thumb:

```text
New source PDF:
    sources/to_review/

General source summary:
    summaries/general/
    or talk_project/reference_summaries/ while the old structure remains active

Citation likely to be reused:
    talk_project/MASTER_CITATIONS.md

Note specific to the delivered IARD talk:
    artifacts/iard-2026-talk/notes/
    or talk_project/ while continuity matters

Keynote or PDF slides from the delivered talk:
    artifacts/iard-2026-talk/slides/

Proceedings draft from the delivered talk:
    artifacts/iard-2026-talk/proceedings/

Weinberg / nonlinear-QM rabbit-hole note:
    side_quests/nlqm/notes/

Possible NLQM paper draft:
    side_quests/nlqm/drafts/
```

## Migration Policy

Do not reorganize aggressively just for cleanliness. Existing links and notes are
valuable.

Prefer:

```text
1. Add new scaffold.
2. Put new material in the better location.
3. Add pointers from old locations when needed.
4. Move old files only when a concrete workflow benefit appears.
```

This repository is also an experiment in best practices for LLM-assisted
theoretical physics research. The structure should evolve pragmatically as that
experiment teaches us what actually works.

