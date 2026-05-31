# Binz et al. (2025) — PNAS
## Tier 2 · The Tao prediction and the philosophical steelman

**Full citation**: Binz, M. et al. "How should the advancement of large language
models affect the practice of science?" *PNAS* 122(5), e2401227121 (2025).
doi:10.1073/pnas.2401227121.
Max Planck Institute for Biological Cybernetics / Helmholtz Center / TU Munich /
UC Santa Barbara / Harvard / Google DeepMind / University of Washington / Indiana
University and others. Published January 27, 2025.
[Local PDF](../../sources/to_review/binz_et_al_2024.pdf)

---

## What it is

A structured debate — four distinct groups of scientists presenting positions and
responding to each other. Not consensus. The value is the range of positions the
community was already staking out in early 2025, before the Hsu and Co-Scientist
results landed.

---

## The Tao 2023 prediction

> *"The 2023-level AI can already generate promising leads to a working mathematician.
> When integrated with tools such as formal proof verifiers, internet search, and
> symbolic math packages, I expect, say, 2026-level AI will be a trustworthy co-author."*

The talk is being given in 2026 — the year Tao named. The Hsu paper, Pan et al.,
and Castelvecchi are the evidence base for evaluating whether the prediction is being
borne out. "Trustworthy co-author" implies expert oversight (a co-author you trust
is still one you check); it does not imply autonomous research. On that reading,
Hsu's workflow precisely matches.

---

## The four perspectives

### Schulz et al. — "More Like a Human Collaborator than a Software Tool"

LLMs are not traditional software; the collaborator framing better captures their
capabilities and failure modes.

**Reproducibility failure**: During revision of one paper, Schulz et al. could not
reproduce their initial results — the provider had updated the model without notice.
Yax et al. independently found results from ChatGPT/GPT-4 couldn't be replicated
three months after initial experiments, with some benchmark scores *decreasing*.

For physics: a result obtained with GPT-5 (as in Hsu's workflow) may not be
reproducible by a reader using a later version of the same model. Open-source models
(which can be pinned to a specific version) partially address this.

---

### Bender et al. — "Science Is a Social Process That Cannot Be Autocompleted"

The harshest view. LLMs are "models of word form distributions — not models of the
information that people might get from reading that text."

**The cognitive vulnerability argument**: "We are ill-positioned to effectively
evaluate LLM output because we can't help but make sense of it." Human linguistic
processing is "instinctual and reflexive" — fluent text is processed as meaningful
even when it isn't. This is a structural reason why Type 2 and Type 3 failures are
hard to catch: the fluency itself disarms critical reading.

**Epistemic diversity**: "Widespread use of one or a few LLMs could undercut epistemic
diversity in science. When asked to provide a hypothesis, experiment, or mode of
explanation, LLMs may repeatedly offer similar solutions, instead of leveraging the
parallel creativity of an entire science community."

**Writing is thinking**: The claim that LLMs can "relieve scientists of the drudgery
of writing" rests on a "false dichotomy between communication and investigation...
[that] ignores the role of writing in the process of formulating, organizing, and
refining ideas."

---

### Marelli et al. — "A Matter of Principles, Not Just Regulations"

Practical contribution: disclose which LLMs were used and how; publish prompts as
supplementary material; use the CRediT taxonomy to code AI contribution without
granting authorship.

This is exactly the reform called for by the disclosure gap in §2.9: Hsu's published
acknowledgements say "check results, format latex, and explore related work"; the
companion paper reveals the AI proposed the main research direction.

---

### Botvinick & Gershman — "AI Can Help, But Science Is for People"

**The normative aspect**: What problems shall we work on? Judgments of
"interestingness, significance, and timeliness are inherently tied to culturally
and historically grounded sensibilities and mores" that evolve. Science no longer
approaches homosexuality as a disorder; animal experimentation increasingly restricted;
new attention to historically neglected climate regions. These shifts are not
derivable from prior literature — they emerge from changes in human values. AI
trained on the existing record cannot generate value evolution.

**The epistemic aspect**:
> *"Would it be satisfactory to have AI systems that successfully model aspects of
> nature — as reflected, for example, in accurate predictions — but which do not
> directly advance human knowledge concerning the underlying principles or mechanisms?
> From an engineering standpoint that might be fine. However, if it's basic science
> we're talking about, we shouldn't let go of the core objective, which is not just
> practical but epistemic. We cannot cede understanding to artificial systems."*

Physics has always demanded more than correct numbers — it demands understanding why
the numbers are what they are. A verified prediction without an explanation is
engineering, not physics.

**The subjective limit**: Humans have a "point of view" — knowledge that is meaningful
to us (epistemic) and values that are meaningful to us (normative). These map onto
Tao's proof indigestion and the homogenization risk respectively.

---

## The Galactica episode

Meta released Galactica (2022), a science LLM promoted as able to summarize papers,
solve math problems, generate wiki articles, write scientific code. Taken offline
after **three days** due to fabricated papers (sometimes attributing them to real
authors) and fake wiki articles including "history of bears in space."

For the talk: the negative anchor. The Hsu paper is not the first attempt to use
LLMs in science — the previous high-profile attempt failed visibly. The contrast
shows what the expert bottleneck makes possible.

---

## Where it appears in the talk

§1.5 (Tao prediction as live test). §5 (steelman — Botvinick/Gershman normative and
epistemic arguments). §4.7 (reproducibility failure from Schulz et al.).
