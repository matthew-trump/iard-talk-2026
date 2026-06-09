# Polchinski 1991 Full Summary

Source PDF: `sources/to_review/polchinski_1991.pdf`

Paper:

Joseph Polchinski, **"Weinberg's Nonlinear Quantum Mechanics and the
Einstein-Podolsky-Rosen Paradox,"** *Physical Review Letters* **66**, 397-400
(1991).

DOI: <https://doi.org/10.1103/PhysRevLett.66.397>

Published January 28, 1991.

## Central Result

Polchinski's paper gives the sharp standard objection to Weinberg's nonlinear
quantum mechanics.

His conclusion is a dilemma:

> Weinberg's nonlinear quantum mechanics leads either to communication through
> Einstein-Podolsky-Rosen correlations, or to communication between branches of the
> wavefunction.

The first possibility is an **EPR phone**: superluminal communication using
entangled separated systems.

The second possibility is an **Everett phone**: communication between different
branches of the wavefunction.

Polchinski's point is not merely that a particular nonlinear term is awkward. The
paper argues that the usual no-signaling protection of quantum mechanics depends
deeply on linearity. Once evolution depends nonlinearly on the state, the structure
that prevents EPR correlations from carrying signals can fail.

## Starting Point: Weinberg's Nonlinear Framework

Weinberg had proposed a general Hamiltonian framework for testing nonlinear
extensions of quantum mechanics. In that framework, ordinary observables are
extended to real homogeneous functions of the state and its complex conjugate.

Polchinski emphasizes that Weinberg's framework contains more observables than
ordinary linear quantum mechanics. He interprets this as meaning that, in a
nonlinear theory, there can be more extractable information in the wavefunction
than in the usual theory.

That raises the central concern:

> The fictitious nonlocality of the ordinary EPR experiment might become real
> nonlocality in nonlinear quantum mechanics.

In ordinary quantum mechanics, EPR correlations do not allow instantaneous
signaling. Polchinski asks what constraints must be imposed on nonlinear
observables to preserve that no-signaling property.

## Setup: Two Widely Separated Systems

Polchinski considers two widely separated systems, labeled I and II.

The composite state is written with two indices:

```text
Psi_ij
```

where `i` labels system I and `j` labels system II.

At time `t = 0`, the two systems have been prepared with correlations. Later, an
observable is measured in system II. A possible signal is sent from system I by
turning on a field that couples to an observable of system I.

For the receiving system II, Polchinski assumes ordinary linear observables are
available. These are represented by Hermitian matrices, as in standard quantum
mechanics.

The question is:

> What restrictions on observables in system I are required so that a field applied
> to system I cannot affect measurement outcomes in distant system II?

## The No-EPR-Signaling Condition

Polchinski writes the equation of motion in Weinberg's Hamiltonian form and
considers a weak perturbing field applied to system I.

Demanding that the expectation value measured in system II not depend on that
field gives a Poisson-bracket condition:

```text
{a_II, a_I} = 0
```

for all ordinary linear observables `a_II` in system II.

Because the ordinary linear observables in system II generate unitary rotations on
the second index of the composite state, this condition means:

> the observable associated with system I must be invariant under arbitrary unitary
> rotations acting on system II.

That invariance forces the system-I observable to depend on the composite
wavefunction only through the reduced density matrix of system I:

```text
rho^I_ik = sum_m Psi_im Psi*_km
```

This is Polchinski's first main result:

> To prevent EPR communication, all observables of an isolated subsystem must
> depend only on that subsystem's reduced density matrix.

## Conflict With Weinberg's Original Treatment Of Separated Systems

Weinberg's original treatment of separated systems did not generally have this
reduced-density-matrix form. For separated systems, Weinberg proposed observables
that are functions of subsystem wavefunctions.

Polchinski says that, except in the linear case, Weinberg's proposed separated-
system observables are not of the required reduced-density-matrix form.

Therefore:

> Weinberg's original separated-system prescription allows EPR communication.

In modern language, the problem is that nonlinear evolution can distinguish
different pure-state decompositions of the same reduced density matrix. Remote
measurements can change the decomposition without changing the density matrix.
If local nonlinear dynamics depends on that decomposition, it can reveal the
remote choice.

## The Attempted Cure: Depend Only On Reduced Density Matrices

Polchinski then asks whether the EPR phone can be blocked by changing the
formalism.

The cure is:

```text
subsystem observables depend only on the subsystem reduced density matrix
```

This prevents ordinary EPR signaling because the local reduced density matrix does
not change under a remote choice of measurement basis.

However, Polchinski argues that this cure leads to a different pathology: the
Everett phone.

## The Everett Phone Thought Experiment

Polchinski constructs a four-step process involving a spin-1/2 ion, a
Stern-Gerlach device, a macroscopic observer, and a nonlinear interaction.

The rough structure is:

1. A spin-1/2 ion enters a Stern-Gerlach device.
2. A macroscopic observer records which outcome occurred.
3. Depending on what the observer saw, the observer either does nothing or rotates
   the spin.
4. A later measurement is made, and the outcome depends on what happened in the
   other branch of the wavefunction.

Polchinski tracks the evolution using partial density matrices associated with the
branches in which the observer saw one outcome or the other.

The key point is that once the nonlinear observable is required to depend on the
total density matrix rather than separate branch wavefunctions, cross terms appear
between macroscopically different observer states.

As a result:

> the observed result in one branch can depend on the action that would have been
> taken in another branch.

Polchinski describes this strikingly: the apparatus seems to read the observer's
mind, because the outcome in the branch where the observer does one thing depends
on what the observer would have done in the other branch.

By iterating the process, observers in different branches can exchange binary
messages. This is the **Everett phone**.

## EPR Phone Versus Everett Phone

Polchinski's dilemma is:

```text
Use Weinberg's original separated-system prescription:
    -> EPR phone / superluminal communication.

Modify the theory so subsystem observables depend only on reduced density matrices:
    -> Everett phone / communication between branches.
```

The second option avoids ordinary EPR signaling but at the price of allowing
communication between branches of the wavefunction.

Polchinski regards the Everett phone as bizarre, but he is careful not to claim
that it is an immediate mathematical inconsistency. It may mean that wavefunction
reduction never occurs and that a many-worlds interpretation becomes natural, but
with communication between worlds now possible.

## Relation To Gisin And Czachor

Polchinski compares his analysis with Gisin and Czachor.

Gisin had argued that nonlinear quantum mechanics leads to EPR communication,
assuming wavefunction reduction, or the projection postulate.

Polchinski's analysis is somewhat different:

- If one keeps the projection postulate and Weinberg's original separated-system
  treatment, EPR communication occurs.
- If one avoids the projection-postulate version by reformulating separated
  systems in reduced-density-matrix terms, EPR communication can be blocked, but
  the Everett phone appears.

Czachor, using Weinberg's original separated-system form, also found EPR
communication by explicit calculation.

## How General Is The Argument?

Polchinski asks how far the result extends beyond Weinberg's exact formalism.

He identifies two main assumptions inherited from Weinberg:

1. The equation of motion has Hamiltonian form.
2. Observables are homogeneous functions of degree `(1,1)` in the wavefunction and
   its complex conjugate.

Polchinski says the first assumption is heavily used and well motivated because it
keeps the connection between symmetries and conservation laws.

The second assumption is less central. It plays no role in the EPR-phone analysis
and only a minor role in the Everett-phone analysis.

Therefore, the core warning is not limited to one arbitrary nonlinear formula.
The danger comes from deterministic nonlinear Hamiltonian evolution of quantum
states.

## Experimental Implications

Polchinski notes that the Everett-phone effect undermines many previous analyses
of experimental bounds on nonlinear quantum mechanics.

Those analyses often treat macroscopic systems as beginning in definite
macroscopic states. But if nonlinear evolution couples different branches of the
wavefunction, then previous branchings of the universe cannot be ignored.

This creates a difficult practical issue:

> nonlinear effects might be diluted across the enormous number of branches of the
> universal wavefunction.

Naively, nonlinearities could be large at a fundamental level yet experimentally
unobservable in a particular branch because the amplitude of that branch is so
small.

Polchinski does not present this as a satisfying resolution, only as a complication
for interpreting experimental constraints.

## Importance For The Hsu / Ho-Hsu / Diosi Thread

Polchinski 1991 is the central background result for the later nonlinear-QM
causality discussion.

The later line can be summarized as:

```text
Weinberg 1989:
constructs a systematic Hamiltonian nonlinear quantum mechanics.

Polchinski 1991:
shows that Weinberg-style nonlinear QM gives either EPR signaling or an Everett
phone.

Ho-Hsu 2014:
recasts the problem in QFT functional-Schrodinger language, arguing that nonlinear
evolution generically creates instantaneous entanglement between initially
unentangled spacelike regions.

Hsu 2026:
attempts a covariant Tomonaga-Schwinger diagnosis: state-dependent nonlinear
Hamiltonian densities threaten microcausality and foliation independence.

Diosi 2026:
disputes Hsu's TS-covariance diagnosis while accepting that nonlinear QM has
Polchinski/Gisin-type causality problems.
```

For the talk:

> Polchinski is the moment when Weinberg's disciplined nonlinear test framework
> becomes a causality problem. The result is not merely that a particular
> nonlinear correction is experimentally constrained. The deeper point is that
> nonlinear evolution changes what entanglement and branch structure can do.

## Slide-Ready Summary

> Polchinski showed that Weinberg-style nonlinear quantum mechanics faces a
> dilemma. If separated systems are treated as Weinberg originally proposed, then
> EPR correlations can be used for superluminal signaling. If the theory is
> modified so that subsystem observables depend only on reduced density matrices,
> EPR signaling can be avoided, but different branches of the wavefunction can
> communicate with one another: an "Everett phone." Either way, nonlinear quantum
> mechanics loses a central protection supplied by linearity.

## One-Sentence Summary

Polchinski showed that Weinberg's nonlinear quantum mechanics gives either an EPR
phone or an Everett phone: nonlinear state evolution makes either spacelike
entanglement or wavefunction branching into a communication channel.

