# §1 Draft — Introduction: Two Timelines
## Target: 5–8 minutes

*Working draft for speaker revision. Delivery notes in [brackets].
Aim for the faster end of the time budget — §2 is where the time is spent.*

---

[Title slide up. Say the question aloud before anything else.]

Is AI ready to take over quantum theory?

[Beat. Let it sit.]

I'm going to answer that question directly before this talk is over. But first I want
to tell you about two timelines — because the question only makes sense if you take
the pace of what's happening seriously, and the best way I know to do that is to put
it next to a pace you already know.

[Two-column slide: "1913–1926" on the left, "2017–2026" on the right. Both columns
populated with dates but not yet highlighted. Walk the left column first.]

---

### Timeline one: the birth of quantum mechanics

This is the column you know. I'm going to go through it anyway, because I think we
don't always notice how it actually moved.

In 1913, Niels Bohr published two papers proposing that electrons occupy discrete
orbits around the nucleus. No derivation. No mechanism. A postulate. It worked for
hydrogen. Physicists knew something had changed; they didn't know what.

For the next twelve years, the old quantum theory was extended — Sommerfeld added
elliptical orbits and fine structure in 1916; Stern and Gerlach demonstrated
directional quantization in 1922; Compton showed in 1923 that X-rays scatter from
electrons as particles. De Broglie proposed in his 1924 thesis that matter has wave
properties. Einstein read it and called it significant. Most physicists waited.

Twelve years of accumulation. And then:

July 1925 — Heisenberg submits the Umdeutung paper. "Über quantentheoretische
Umdeutung kinematischer und mechanischer Beziehungen." The reinterpretation of
kinematics and mechanics. He abandons classical trajectories entirely. Position and
momentum are no longer continuous variables — they are tables of transition
amplitudes. Born recognizes within weeks that this is matrix algebra.

By November, Born, Heisenberg, and Jordan have the complete theory. The Dreimännerarbeit.
The commutation relation [q,p] = iℏ. Quantum mechanics — mathematically complete,
physically bewildering.

January 27, 1926: Schrödinger submits the Erste Mitteilung to *Annalen der Physik*.
"Quantisierung als Eigenwertproblem." The wave equation. He will publish three more
papers in the same journal that year, including a proof that wave mechanics and matrix
mechanics — two routes taken in opposite directions — are mathematically equivalent.

June 1926: Born's probability rule. The wavefunction is not a physical wave; its
squared modulus is a probability density. The probabilistic interpretation. It will
win him the Nobel Prize in 1954, which tells you how long it took the community to
accept what had happened.

Here is the compression to notice: from Heisenberg's Umdeutung paper in July 1925
to Born's probability rule in June 1926 is eleven months. In eleven months: matrix
mechanics, the three-man paper, the Schrödinger equation in four installments, the
proof of equivalence, and the Born rule. The complete theoretical structure of
quantum mechanics assembled in under a year. The people doing this were in constant
correspondence; some were visiting each other's institutes. The field moved faster
than anyone predicted, including the people making it move.

Thirteen years of slow buildup. Eleven months of explosion.

[Shift to the right column.]

---

### Timeline two: large language models

Now the column on the right.

2017: Vaswani and colleagues at Google publish "Attention Is All You Need." The
transformer architecture. Attention mechanisms allow models to relate distant parts
of a sequence without recurrence. A technical contribution — not obviously
revolutionary at the time.

2019 to 2022: scaling. GPT-2, then GPT-3 — 175 billion parameters, few-shot learning
emerging. The discovery that capability improves predictably with compute and data.
Scaling laws. The field is building; the public isn't watching yet.

November 2022: ChatGPT. Not a research paper — a product. The broader world encounters
the capability directly. I'll ask you to recall where you were when you first used it,
and what you asked it about your own work.

Two weeks after launch, Gerardo Adesso at Nottingham published the first paper
"entirely generated with outputs from ChatGPT" — a physics-themed experiment with
no actual scientific content, explicit about its limitations. His conclusion in
November 2022: ChatGPT "is not at the level of autonomously making and developing
original scientific contributions." That is the baseline.

Also in 2023, Terence Tao wrote — I'll quote him exactly, because this talk is in
some sense a response: *"The 2023-level AI can already generate promising leads to a
working mathematician. When integrated with tools such as formal proof verifiers,
internet search, and symbolic math packages, I expect, say, 2026-level AI will be
a trustworthy co-author."*

We are in 2026. Tao named this year. The evidence I'm about to show you is the test
of whether he was right, and on what terms.

2025: Stephen Hsu, theoretical physicist at Michigan State, publishes a result in
*Physics Letters B*. Quantum field theory. Nonlinear quantum mechanics. Tomonaga-Schwinger
formalism. The main research direction — the conceptual move that made the paper
possible — was proposed unprompted by GPT-5 during a Q&A session. Published after
standard peer review.

May 2026: *Nature* runs a feature: "How AI is transforming mathematics." General-purpose
language models contributing to solved problems in number theory. A Fields Medal
predicted by 2030. Proof-length capabilities scaling. This is happening in mathematics
now. I'll argue it's where theoretical physics is heading.

The compression: from "Attention Is All You Need" in 2017 to a published QFT result
with an LLM-generated conjecture in 2025 is eight years — shorter than the thirteen
years from Bohr to Schrödinger. From ChatGPT in November 2022 to that same result
is three years. Three years from "not at the level of making original contributions"
to a peer-reviewed contribution in *Physics Letters B*.

The explosive phase — the eleven-month equivalent — may be the interval we are
currently inside.

---

### What the parallel claims, and what it doesn't

I want to say this once clearly, before you push back silently.

The parallel does not claim that LLMs describe physical reality the way quantum
mechanics does. It does not claim that AI will be as significant to physics as quantum
mechanics. It does not claim to predict what will happen, only to make a point about
pace. The two timelines are not analogous in content — they're analogous in the
pattern of how capability arrived: slowly, then faster than anyone predicted, then
all at once.

The QM parallel has one function. You know how fast 1925 to 1926 actually moved.
Most of us, even knowing the history, are still surprised by eleven months. That
surprise is what I want you to carry into the rest of this talk — not as a claim about
AI, but as a calibration about how fast fields can move when the foundational piece
falls into place.

---

### The evidence base

Everything I'm going to show you is drawn from published or preprint sources: one
peer-reviewed physics paper, one empirical study with numbers, one position paper from
physicists and ML researchers, one piece from *Nature* on the mathematics frontier,
and several supporting sources. No speculation. No demos. No benchmark theater.

[Transition — spoken without slide:]

We are 100 years from the moment the wave equation was written. The question I want
to explore today is whether we are also inside a comparably compressed moment —
and what that would mean for how we do theoretical physics.
