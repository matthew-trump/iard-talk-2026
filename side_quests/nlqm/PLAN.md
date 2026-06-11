# NLQM Plan

Purpose: organize the nonlinear quantum mechanics side quest as a historical and
technical investigation leading up to a thorough understanding of Weinberg's 1989
paper.

## Working Aim

Develop a historically grounded understanding of nonlinear quantum mechanics
(NLQM), with Weinberg 1989 as the first major focal point.

The initial goal is not to argue for NLQM, but to understand:

```text
1. Why nonlinear modifications of quantum mechanics were considered.
2. What mathematical forms they took before Weinberg.
3. What Weinberg changed in 1989.
4. Why Polchinski/Gisin-style objections became decisive.
5. How later QFT and Tomonaga-Schwinger analyses reframed the issue.
```

## Current Starting Point

The project already contains several relevant source files:

```text
sources/to_review/weinberg_1989.pdf
sources/to_review/polchinski_1991.pdf
sources/to_review/ho_and_hsu_2014.pdf
sources/to_review/hsu_2025_physical_review_letters_b.pdf
```

Existing summaries and notes are in `talk_project/`, but this side quest should
develop its own reading sequence and conceptual map.

## Historical Reading Sequence

### Phase 1: Before Weinberg

Questions:

```text
What did "nonlinear quantum mechanics" mean before Weinberg?
Were nonlinearities proposed as collapse mechanisms, effective approximations,
or fundamental modifications?
What pathologies were already known?
```

Candidate references:

```text
de Broglie, nonlinear wave mechanics / causal interpretation
Mielnik, generalized quantum mechanics
Pearle, collapse-related nonlinear/stochastic ideas
Bialynicki-Birula and Mycielski, logarithmic nonlinear Schrodinger equation
Haag and Bannier
Kibble
Heslot, quantum mechanics as classical Hamiltonian theory
```

Need to collect exact citations and source files.

### Phase 2: Weinberg 1989

Primary source:

```text
sources/to_review/weinberg_1989.pdf
```

Questions:

```text
What exactly is Weinberg generalizing?
What is meant by observables as real homogeneous functions on Hilbert space?
What does "ray-based" mean?
How does the Hamiltonian structure work?
How are eigenvalues and stationary states defined?
How does Weinberg treat separated systems?
What did Weinberg know about possible pathologies?
What does the note added in proof say about Polchinski?
```

Goal:

Produce a line-by-line conceptual guide to the paper, not merely a summary.

### Phase 3: Gisin And Polchinski

Primary source already present:

```text
sources/to_review/polchinski_1991.pdf
```

Questions:

```text
What exactly is the EPR signaling argument?
What is the difference between EPR phone and Everett phone?
What does Polchinski assume about measurement, reduced density matrices, and
separated systems?
What is inherited from Weinberg and what is Polchinski's contribution?
```

Need Gisin source(s).

### Phase 4: QFT Recasting

Primary source:

```text
sources/to_review/ho_and_hsu_2014.pdf
```

Questions:

```text
How does the functional Schrodinger picture change the framing?
What does separability mean for spacelike separated field regions?
What does Ho-Hsu add beyond Polchinski?
Why is instantaneous entanglement generation stronger/different from EPR signaling?
```

### Phase 5: Covariant / Tomonaga-Schwinger Recasting

Primary source:

```text
sources/to_review/hsu_2025_physical_review_letters_b.pdf
```

Related:

```text
Diósi comment, arXiv:2602.06845
Kaplan-Rajendran, Phys. Rev. D 105, 055002 (2022)
Tomonaga 1946
Schwinger 1948, 1951
```

Questions:

```text
What does TS covariance add beyond fixed-foliation QFT?
What is Hsu's nonlinear TS integrability condition?
What does Diósi object to?
Is the dispute about covariance, no-signaling, or both?
```

## Immediate Next Tasks

1. Build a source inventory for NLQM.
2. Identify missing pre-Weinberg references and collect PDFs if possible.
3. Start a detailed Weinberg 1989 reading guide.
4. Create a glossary for Weinberg's formalism.
5. Create a timeline of NLQM from pre-Weinberg to Hsu/Diósi.

## Working Output Types

Use:

```text
notes/
    Conceptual notes, derivation walkthroughs, reading logs.

drafts/
    Possible future paper/talk sections.

qa/
    Expert objections and self-questioning.
```

## Guiding Principle

Do not rush to the Hsu/Diósi endpoint. The side quest begins historically and
builds forward step by step. Weinberg 1989 is the first major destination.

