# Polchinski 1991 Summary

## Citation

Joseph Polchinski, "Weinberg's nonlinear quantum mechanics and the
Einstein-Podolsky-Rosen paradox," *Physical Review Letters* 66, 397-400 (1991).
DOI: 10.1103/PhysRevLett.66.397.

Published January 28, 1991.

---

## Core Result

Polchinski's paper is the standard sharp objection to Weinberg-style nonlinear
quantum mechanics.

His result is a dilemma:

> Weinberg's nonlinear quantum mechanics leads either to communication through
> Einstein-Podolsky-Rosen correlations, or to communication between branches of the
> wavefunction.

The first horn is the famous one: superluminal signaling.

In ordinary linear quantum mechanics, Alice cannot use her choice of measurement on
one half of an entangled pair to send a signal to Bob. Bob's local density matrix is
unchanged, and all equivalent ensemble decompositions of that density matrix give the
same local predictions.

In nonlinear quantum mechanics, that protection can fail. If Bob's time evolution
depends nonlinearly on the state, then it can depend on the particular pure-state
decomposition of his density matrix, not only on the density matrix itself. Alice's
choice of measurement basis can remotely prepare different ensemble decompositions
for Bob. If Bob's nonlinear dynamics can distinguish those decompositions, EPR
correlations become a signaling channel.

The second horn is subtler. One might try to avoid EPR signaling by making subsystem
evolution depend only on the reduced density matrix. Polchinski argues that this
blocks ordinary EPR communication only at the cost of a different pathology:
communication between different branches of the total wavefunction. He called this
an "Everett phone."

---

## Why It Matters

Polchinski's point is not merely that Weinberg's particular formalism has a technical
flaw. The broader lesson is that the no-signaling theorem of ordinary quantum
mechanics relies heavily on linearity.

Once evolution is nonlinear, operationally equivalent mixtures can evolve differently.
That makes entanglement dangerous: different remote measurement choices can become
locally distinguishable.

For the talk, the concise version is:

> Polchinski showed that Weinberg-style nonlinear quantum mechanics cannot keep all
> the usual separations intact. If nonlinear evolution acts on pure states in the
> natural way, EPR correlations become usable for superluminal signaling. If one
> reformulates the theory to avoid that by evolving reduced density matrices
> independently, one gets the strange alternative of communication between branches
> of the wavefunction.

---

## Relation to Hsu and Diosi

Polchinski is the background result both Hsu and Diosi are working against.

Polchinski establishes the nonlinear-QM causality problem: nonlinear dynamics can
turn entanglement into a signaling resource unless the theory is reformulated in a
very nonstandard way.

The Hsu/Diosi dispute is narrower. It is not over whether nonlinear quantum mechanics
has causality problems. It is over how to diagnose them in the relativistic QFT
setting:

- Hsu argues that state-dependent nonlinear QFT evolution generically violates
  Tomonaga-Schwinger foliation independence, hence relativistic covariance.
- Diosi argues that this is the wrong diagnosis. In his formulation, the nonlinear
  Tomonaga-Schwinger equation can remain covariant and integrable, while the
  causality problem remains an operational signaling problem of the Polchinski/Gisin
  type.

Useful phrasing:

> Polchinski gives the reason nonlinear quantum mechanics is dangerous. Hsu and
> Diosi are arguing about whether, in the QFT setting, that danger shows up as failure
> of Tomonaga-Schwinger covariance or as a separate no-signaling problem despite
> formal covariance.

---

## One-Line Version

> Polchinski showed that Weinberg-style nonlinear quantum mechanics gives you either
> superluminal EPR signaling or an "Everett phone" between wavefunction branches.
