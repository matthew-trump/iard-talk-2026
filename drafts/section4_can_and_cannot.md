# §4 Draft — What LLMs Can and Cannot Do
## Target: 8–10 minutes | Estimated actual: ~11 minutes

*Working draft for speaker revision. Delivery notes in [brackets].
This section synthesizes rather than introduces. The evidence has been
presented; the job here is to give the audience a usable conceptual frame —
not a technical tutorial, but a physicist's working model.
Shorter sentences than §2 and §3. More declarative.*

---

[No slide needed to open. This section is a structured argument.
Use slides sparingly — the failure taxonomy slide, the Wang et al. table.
Otherwise talk, not slides.]

---

### A physicist's map of LLM failure

Before I give you the thesis, I want to give you a map.

The failures documented across these papers are not random. They have structure.
If you're going to use these tools — and you will, if you aren't already —
you need to know which failures to expect and which to worry about most.

Three types. Each harder to catch than the last.

---

**Type 1: Calculation errors.**

Index mistakes. Sign errors. Inconsistent unit conventions — mixing SI and natural
units within a derivation. Lu et al. note these despite strong benchmark performance.
Pan et al. assigned partial credit for a sign error in a magnetic field momentum
shift in one of their fifteen papers.

These are detectable. Check the output against dimensional analysis, energy
conservation, symmetry. They are annoying and common; they are not the failure
mode that produces publications with wrong physics.

---

**Type 2: Plausible-but-wrong conceptual steps.**

The LLM produces a reasoning step that sounds correct, is internally consistent,
and is factually wrong. Lu et al.'s clearest example: applying perturbation theory
without stating the validity condition. The output looks like physics. It has the
right form. Detecting it requires knowing the content — not just the form — well
enough to notice that the condition isn't satisfied.

This is harder. It requires a reader who already knows enough to see what's missing.

---

**Type 3: Cross-subfield confabulation.**

The LLM draws on genuine knowledge from a distant part of the literature to
construct a plausible-sounding but incorrect argument in the problem at hand.

The Reeh-Schlieder episode in Hsu is the canonical example. The models correctly
understood the theorem. They correctly knew it was relevant to operator algebras
in relativistic QFT. They incorrectly concluded it could be used to prove the TS
integrability conditions must be violated.

Hsu's diagnosis is worth repeating here because it applies beyond his paper:

> *"Model expertise extends across the entire literature of our subject, and hence
> they are fully capable of introducing plausible-sounding applications of techniques
> from distant subfields. These are often the most difficult confabulations to detect."*

The same capability that allows GPT-5 to propose the TS framework — broad exposure
to the literature across subfields — also allows it to construct the Reeh-Schlieder
suggestion. The model does not know which connection is real and which is wrong.
It cannot. That distinction requires depth in both subfields simultaneously.

Type 3 errors are the ones that consume expert effort. They are also, structurally,
the last to be automated away — because catching them requires exactly the expertise
that makes someone an expert in the first place.

---

### The false positive problem

There is a structural issue that cuts across all three types and makes them harder
to detect than they look.

In 2022, the Minerva paper from Google tested large-scale language models on
mathematics benchmarks. One finding has not received enough attention in the
physics community.

At the hardest difficulty level on the MATH benchmark: **30% of problems with
correct final answers had incorrect chain-of-thought reasoning.** The model reached
the right answer by the wrong path.

[Optional slide: "30% of correct answers — at hardest difficulty — have wrong reasoning"]

For physics: this means the final equation alone is not a quality signal. A
derivation that ends in the right expression may have been produced via a chain
of reasoning that is factually wrong at intermediate steps. The physicist who checks
only the result — and who sees the correct result — has no reason to go back and
audit the reasoning. This is how a Type 2 error survives.

The threshold for when this matters is not the easy problems. It is exactly the
hard ones — which is to say, the problems where the derivation itself carries
information, where the steps are the physics, and where an error in intermediate
reasoning matters even if the final answer happens to come out right.

---

### The implicit-knowledge gap

Pan et al. identify a failure mode that sits between Type 2 and the expert bottleneck
more broadly, and it deserves its own name.

**Implicit field conventions**: knowledge that every practitioner in a subfield has
but that no paper states. The standard Fourier transform definition in second-quantized
notation. The conventional factor ordering in the BdG Hamiltonian. The usual way to
handle fermionic statistics at zero temperature. These are things a graduate advisor
corrects once in year one and never mentions again. They are not on arXiv. LLMs have
absorbed the explicit literature but not this register.

When Pan et al. tested GPT-4's ability to extract information directly from paper
excerpts — without human-supplied context — it scored high on explicit notation
and system-specific information, and poorly on implicit conventions. One-shot
prompting (providing a single example of an excerpt and its correct extraction)
jumped performance on one template task from 44% to 80%.

The gap is not ignorance. It is the absence of the tacit knowledge that makes someone
a member of a research community rather than a reader of its papers. That tacit
knowledge is not captured in any single document; it is transmitted in the gap
between documents — in supervision, in seminar questions, in the culture of how a
subfield works.

This connects to something Lu et al. say carefully: theoretical physics requires
"connecting mathematical abstractions to physical reality." The Chern insulator
example makes it concrete. Diagonalizing a 2×2 matrix is trivial linear algebra.
The Bloch Hamiltonian H(k) = d(k)·σ of a Chern insulator is that 2×2 matrix.
Finding eigenvalues ±|d(k)| is mathematically simple. But the physics is in the
winding of d(k) in momentum space — a topological invariant that determines a
measurable Hall conductivity. An LLM that executes the linear algebra may miss
the physics entirely. Knowing to look for the winding number is not derivable
from the formalism. It is what the formalism is for — and knowing that requires
having been a physicist, not just having read physics.

---

### A direct test: GPT-1900

Before putting numbers on the execution/judgment distinction, I want to mention
an experiment that addresses the "tool vs. reasoner" question more directly than
any benchmark — because it removes the training data from the question entirely.

Michael Hla, in a 2026 blog article titled "Machina Mirabilis," trained a 3.3
billion parameter language model exclusively on text published before January 1,
1900. No Einstein. No Bohr. No Planck. No quantum mechanics, no special relativity.
The dataset was aggressively filtered to remove even post-1900 author forewords and
footnotes. He then asked the model physics questions to see whether it could reason
its way toward discoveries it had never seen.

The results are tantalizing and honest in equal measure.

On the photoelectric effect: the model identified that light cannot be continuous and
consists of *"disconnected parts of varying frequencies"* — approaching Einstein's
photon hypothesis from pre-quantum principles, without having seen Einstein.

On the ultraviolet catastrophe — the very failure of classical physics that was sitting
unsolved in 1900 — the model occasionally recognized that the equipartition theorem
fails at high frequencies, requiring discrete energy mechanisms.

On general relativity: when given the elevator thought experiment, it reasoned that
gravity must affect the medium through which light travels. It reached for the ether —
the 19th-century concept — but the physical intuition that gravity and light are
connected was there.

Hla's own assessment is the right one to quote: *"the most likely explanation for
the apparent breakthroughs is that the model is parroting words that seem plausible,
but does not have any sort of strong internal representation of the world to reason
from."* He is skeptical of genuine discovery. The evaluation conditions were easier
than the original discovery context. Reward hacking is possible.

But here is what the experiment establishes regardless of how you read it: a model
that has never seen modern physics nonetheless produces outputs that shadow the
structure of modern physics when asked the right questions. Whether that is reasoning
or sophisticated interpolation over pre-1900 literature is exactly the question that
cannot currently be answered. The experiment does not resolve the tool/reasoner debate.
It shows why the debate is not merely semantic.

---

### The execution / judgment cliff

[Slide: a simple two-column table]

| Problem type | Accuracy |
|---|---|
| Well-specified (all data given) | 62.5% |
| Under-specified (judgment required) | 8.3% |

This is from Wang et al. — Stanford, Carl Wieman (Nobel, 2001) among the authors.
GPT-4, tested on introductory engineering physics problems. Statics, kinematics,
momentum, fluids. Not research-level physics. Forty problems, varying one dimension:
whether all required data was provided, or whether the model had to make physical
assumptions.

The cliff is statistically significant. Fisher's exact test, p < 0.001.

When everything is specified and the task is structured: 62.5% accuracy.
When the model must exercise physical judgment: 8.3%.

The dominant failure for the under-specified problems was not calculation error.
It was **physical world modeling**: ChatGPT correctly identified the relevant physics
— torques, force diagrams — but misrepresented the physical situation. Wrong pivot
point. Missing bodies in the force diagram. A model that computed a building's weight
but failed to account for the concrete slab and pile weights, never having formed
an accurate geometric model of the structure.

The error is in the representation, before any formula is applied.

Why does this matter for a research audience? Because it explains precisely why the
Pan et al. HF template works. The template converts what would be an under-specified
research problem — "apply Hartree-Fock to this paper's system" — into a sequence of
well-specified sub-tasks. The expert who designs the template is doing exactly what
Wang et al.'s failure modes demand: constructing the accurate physical model and
specifying all required data before handing the problem to the LLM.

Without the template: 8.3% regime.
With the template: 87.5% regime.

The template is the physicist.

---

### The expert bottleneck, stated cleanly

All three core papers converge on the same conclusion, stated in different registers.

Hsu: *"Non-expert use of AI in frontier research — even by individuals with
considerable background, such as PhD students — is likely to lead to large volumes
of subtly incorrect output."*

Lu et al.: Current LLMs are "inadequate" without "domain-specialized training
and tooling" — but the tooling they envision is exactly the kind of structured
framework an expert builds.

Pan et al.: The HF template was designed by expert condensed matter physicists.
GPT-4 executes brilliantly inside it. The template design is not automated.

The bottleneck is not model capability in isolation. It is the combination of
model capability with expert scaffolding: structuring the task, catching Type 3
errors, supplying the implicit-knowledge register, and deciding which model outputs
are worth pursuing.

The *Nature* editorial board — in the same issue that published the Robin and
Co-Scientist papers — puts this directly: humans framing the project, running
experiments, offering guidance, and checking output along the way is *"a feature,
not a bug — and shutting humans out of the loop would not be easy."*

That formulation is worth keeping. The expert bottleneck is not a temporary
limitation of current models to be engineered away. It is the design. The physicist
who structures the task, catches the Reeh-Schlieder error, and decides which conjecture
is worth pursuing is not a workaround — they are the reason the system works.

This framing is honest and it is useful. It does not dismiss LLMs — the 87.5 score
is real, the TS suggestion is real, the ripasudil finding is real. It does not
uncritically celebrate them. It says: the tool is powerful, the limiting factor is
human expertise, and that limiting factor is not going away on its own.

---

### The complexity ceiling — and the algorithm that doesn't help

One more finding that belongs in this section, from a 2025 Apple paper by Shojaee
et al. titled "The Illusion of Thinking."

The paper tested frontier reasoning models — the o1/o3 class that produces extended
chains of thought before answering — on controlled puzzle environments (Tower of Hanoi,
River Crossing, Blocks World). The tasks are not physics. But the findings are precise
and sobering.

Three performance regimes emerge consistently:

- **Low complexity**: standard LLMs outperform reasoning models — the extended
  "thinking" is overhead, not value
- **Medium complexity**: reasoning models pull ahead — the chain-of-thought is earning
  its cost
- **High complexity**: both collapse completely

At the collapse point, something counterintuitive happens. The models begin *reducing*
their reasoning effort — generating fewer thinking tokens — despite having remaining
token budget available and harder problems to solve. They are not running out of
compute. They are stopping trying.

The most important finding for our purposes: giving the model an explicit algorithm
to follow does not improve performance at high complexity. The model knows the
procedure; it still fails at the same complexity threshold. The failure is in symbolic
execution — reliably carrying a multi-step procedure to completion — not in knowledge
of what to do.

This is the deeper limitation behind the Pan et al. result. The HF template works
brilliantly at the complexity level of a Hartree-Fock derivation. What the Apple
paper tells us is that template-based approaches have a ceiling — one set by the
model's symbolic manipulation capability, not by the quality of the template. The
expert who designs the template is not just clarifying the task; they are also
keeping the problem inside the regime where the model can actually execute.

[Delivery note: flag that this is puzzle-based research, not physics — but the
structural finding maps directly onto what Hsu encountered with long derivation
chains and what Lu et al. describe as failure at the non-standard pivot step.]

---

[Transition to §5:]

One final distinction that belongs in the synthesis rather than the map: efficiency
is not the same as insight. The *Nature* editorial's line — *"we don't yet know
whether greater efficiency equates to greater insight"* — is where §5 begins.

With that map in place, I want to turn to the central argument and to the field
that is showing us, right now, where physics is heading.
