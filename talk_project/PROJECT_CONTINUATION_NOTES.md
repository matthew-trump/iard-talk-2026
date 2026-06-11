# Project Continuation Notes

## Status After Talk Delivery

The talk has been delivered, but the project should remain active.

The next possible phase is development of a paper, preprint, or IARD proceedings
contribution based on the talk and the associated research notes.

This means the repository should not be treated as a frozen archive. It is now a
living project with at least three possible trajectories:

```text
1. Continue developing the talk material into a paper or proceedings article.
2. Continue collecting new references and notes as the subject evolves.
3. Eventually migrate the workflow into a new project seed, or continue within
   this repository if that proves more useful.
```

## Fast-Evolving Subject Matter

James O'Brien noted after the talk that the subject itself is evolving quickly.
Within two years, much of the current material may be out of date by the next
conference.

This should be treated as a structural feature of the project, not a failure of
the current talk. The repository should remain open to:

```text
new notes in NOTES.md
new papers in sources/to_review/
new source summaries
new reference digests
new Q&A documents
changes to the core thesis
```

## Thesis May Continue To Evolve

The current thesis served the delivered talk, but it may not be the final thesis
of a paper.

Future work may redirect or sharpen the basic argument. Possible shifts include:

```text
from conference talk to proceedings article
from AI-in-theoretical-physics survey to Hsu-focused case study
from Hsu-focused case study to broader expert-bottleneck argument
from talk analysis to methodological paper on LLM-assisted physics workflows
from Section 6 speculation to a separate technical paper seed
```

Until a preprint or proceedings article is submitted, the thesis should remain
editable.

## Workflow Going Forward

Continue using the established project workflow:

```text
NOTES.md
    running observations, new comments, conference aftermath, new ideas

sources/to_review/
    newly discovered papers and PDFs

talk_project/reference_summaries/
    concise source digests for core references

talk_project/
    standalone conceptual notes, derivation notes, Q&A, and archival documents

drafts/
    future article sections, revised talk sections, or proceedings draft
```

When new sources are added:

1. Put the file in `sources/to_review/`.
2. Create or update a source summary.
3. Add citation details to `talk_project/MASTER_CITATIONS.md` if the source may
   appear in slides, proceedings, or a paper.
4. Update `NOTES.md` with why the source matters.
5. Reassess whether it changes `THESIS.md` or `PLAN.md`.

## Best-Practices Discovery

One of the ongoing questions is methodological:

> Should future projects fork into a fresh seed directory after a talk is
> delivered, or should the same repository continue to accumulate the paper,
> proceedings, notes, and follow-up work?

This is itself part of the continuing discovery of best practices for using LLMs
in theoretical physics and related research.

Possible criteria for deciding:

```text
Continue in this repository if:
    the paper/proceedings remains tightly coupled to the delivered talk;
    the existing notes are still directly useful;
    continuity matters more than cleanliness.

Migrate to a new seed if:
    the project develops a substantially new thesis;
    the paper becomes technically independent of the talk;
    the existing repo becomes too cluttered for efficient work;
    the goal shifts from talk preservation to article production.
```

The decision should be made pragmatically when the next phase becomes clear.

## Larger Multi-Artifact Structure

After the talk, the project is also being organized as a larger research and
writing environment defined by a shared reference pool rather than by a single
talk.

The first artifact remains the delivered IARD 2026 talk:

```text
artifacts/iard-2026-talk/
```

The first explicit side quest is nonlinear quantum mechanics:

```text
side_quests/nlqm/
```

This side quest is for the Weinberg 1989 rabbit hole and the broader subject of
nonlinearities in quantum theory. It may later become a paper, future talk, or
separate project.

References remain shared for now in `sources/`, with citation details collected in
`talk_project/MASTER_CITATIONS.md`. Artifact-specific slides and Q&A should live
with the relevant artifact; side-quest conceptual notes and draft research lines
should live with the side quest.

The detailed structure is documented in `PROJECT_STRUCTURE.md`.
