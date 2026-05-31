# Hsu (2025) — "Theoretical Physics with Generative AI"
## Tier 1 · Source of all the detail in §2

**Full citation**: Hsu, S.D.H. "Theoretical Physics with Generative AI." Preprint,
December 1, 2025.
[Google Drive PDF](https://drive.google.com/file/d/16sxJuwsHoi-fvTFbri9Bu8B9bqA6lr1H/view)
[Substack](https://stevehsu.substack.com/p/theoretical-physics-with-generative)
[Local PDF](../../sources/to_review/hsu_2025_b_cs_ai_physics.pdf)

---

## What it is

A methodology companion to the PLB paper. Contains verbatim transcripts of GPT-5
exchanges. Aimed at both AI researchers and theoretical physicists. The source for
essentially all of the specific claims in §2 that go beyond the published paper.

---

## The key GPT-5 exchange

Hsu was testing GPT-5 on his own 2014 paper. He asked it to compare nonlinearity
in non-relativistic QM with what happens when you impose full QFT structure. GPT-5
responded correctly and then **volunteered**:

> *"If you want, I can sketch the Tomonaga-Schwinger version of this (evolution by
> spacelike hypersurfaces) to show explicitly why a hypersurface-local generator that
> depends nonlinearly on the global state cannot remain foliation-independent without
> collapsing back to linear dynamics."*

Hsu said yes. GPT-5 generated the TS setup, the integrability condition including the
Fréchet derivative cross-terms, and the key operator constraint.

Hsu's assessment:
> *"This exchange is remarkable because GPT-5 proposes a novel research direction."*

The word **"de novo"** appears in the abstract of this paper. The equations from that
exchange "form the core of the resulting paper."

---

## The Generate-Verify protocol

- **Generate step**: One model instance proposes a research step or calculation.
- **Verify step**: A separate model instance — given no context about what the first
  produced — checks it. Minimal Verifier prompt: *"You are a world class theoretical
  physicist. Check the following for errors. Review each equation and reasoning step.
  Identify all problems and summarize your findings."*
- Models used: GPT-5, Gemini 2.5 Pro, Qwen-Max (primary); DeepSeek V3.1, Grok-4 (final checks).

Key asymmetry:
> *"Convergent positive Verifier responses are a good signal for correctness.
> Lack of convergence is a reliable signal that something is wrong."*

Hsu's colleague analogy:
> *"Using LLMs as noisy Verifiers of a research step is not very different, in my
> experience, from going down the hall to explain the new idea to a colleague. Even
> an expert colleague will not render a completely reliable opinion; however the
> resulting discussion is useful to discover problems and to calibrate conviction levels."*

---

## The Reeh-Schlieder failure

Multiple LLMs suggested using the Reeh-Schlieder theorem and the "split property"
from axiomatic QFT to prove the TS integrability conditions must be violated.
**These suggestions were wrong.**

Hsu:
> *"I expended a significant amount of effort to determine this, given that my
> background is not in axiomatic field theory."*

The models correctly understood the theorem and correctly knew it was about operator
algebras in relativistic QFT — and incorrectly concluded it was applicable.

Hsu's diagnosis:
> *"Model expertise extends across the entire literature of our subject, and hence
> they are fully capable of introducing plausible-sounding applications of techniques
> from distant subfields. These are often the most difficult confabulations to detect!"*

The failure was caught because Verifier instances couldn't converge — the asymmetry
worked as a signal. Resolution required Hsu to study axiomatic QFT in enough depth
to understand the theorem's limitations himself.

---

## Key quotes for the talk

- *"Research with an LLM might be compared to collaboration with a brilliant but
  unreliable human genius who is capable of deep insights but also of errors both
  simple and profound."*
- *"Non-expert use of AI in frontier research — even by individuals, such as PhD
  students, with considerable background — is likely to lead to large volumes of
  subtly incorrect output."*

---

## Where it appears in the talk

§2 throughout. The verbatim GPT-5 exchange, the workflow description, the
Reeh-Schlieder episode, and both key quotes all originate here.
