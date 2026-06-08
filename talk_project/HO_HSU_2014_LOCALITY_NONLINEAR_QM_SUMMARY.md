# Ho and Hsu 2014: Locality and Nonlinear Quantum Mechanics

Source PDF: `sources/to_review/ho_and_hsu_2014.pdf`

Paper:

Chiu Man Ho and Stephen D. H. Hsu, **"Locality and Nonlinear Quantum Mechanics"**,
arXiv:1401.7018v2, dated January 2015.

## Central Claim

Ho and Hsu argue that nonlinear modifications of quantum mechanics generically
violate relativistic locality. Their formulation is especially useful because it
uses quantum field theory in the functional Schrodinger picture, rather than only
ordinary nonrelativistic quantum mechanics.

Their core point is:

> Generic nonlinear Schrodinger evolution causes almost instantaneous
> entanglement between initially unentangled spacelike separated systems.

This is distinct from, though related to, the better-known Gisin/Polchinski
argument that nonlinear quantum mechanics can allow superluminal signaling through
measurements on entangled states.

## Functional Schrodinger Setup

In the functional Schrodinger picture, a quantum field state is represented by a
wavefunctional:

```text
Psi[phi(x), t]
```

Here `phi(x)` is a whole spatial field configuration. Ordinary linear quantum
field evolution is written:

```text
i d_t Psi[phi, t] = H Psi[phi, t]
```

For a local relativistic quantum field theory, the Hamiltonian is an integral of
local Hamiltonian-density terms. For a scalar field, the Hamiltonian contains the
usual kinetic, gradient, and mass terms.

If two regions `A` and `B` are widely separated and initially unentangled, the
wavefunctional approximately factorizes:

```text
Psi[phi, t] = psi_A[phi_A, t] psi_B[phi_B, t] ...
```

In ordinary linear QFT, locality implies that the Hamiltonian separates into
local pieces acting independently on `A` and `B`, at least until causal
propagation has had time to connect the regions.

## Nonlinear Modification

Ho and Hsu consider a nonlinear generalization:

```text
i d_t Psi = (H + F(Psi*, Psi)) Psi
```

The nonlinear term `F` is a functional of the state itself. Their claim is that a
generic such term does not respect the product structure:

```text
psi_A psi_B
```

Instead, the nonlinear term couples the two factors. Consequently, the evolution
of the state in region `A` immediately depends on the state in region `B`, and
vice versa, regardless of the spacelike separation between the two regions.

The result is nonlocality in a direct field-theoretic sense: initially separable
states of spacelike separated regions become entangled almost instantly.

## Relation To Weinberg, Gisin, and Polchinski

The paper explicitly belongs to the Weinberg/Gisin/Polchinski line of argument.

Weinberg had proposed a systematic nonlinear generalization of quantum mechanics
in which observables become homogeneous real-valued functions on Hilbert space.
Gisin and Polchinski then showed that nonlinear quantum mechanics can generically
turn EPR correlations into genuine superluminal signaling.

Ho and Hsu sharpen the concern in QFT language:

```text
Weinberg:
Can quantum mechanics be made slightly nonlinear?

Gisin / Polchinski:
Nonlinear quantum mechanics plus entanglement threatens superluminal signaling.

Ho / Hsu:
Generic nonlinear wavefunctional evolution creates nonlocal entanglement between
spacelike separated regions, even when the initial state is unentangled.
```

So the Ho-Hsu point is not merely that measurement on an already entangled state
can become dangerous. It is that nonlinear field evolution itself tends to
destroy separability across spacelike regions.

## Examples Of Nonlinear Terms

The paper discusses several forms of nonlinear modification.

### Simple Nonlinear Term

A term such as

```text
F(Psi*, Psi) = epsilon |Psi|^2
```

violates separability directly. If `Psi = psi_A psi_B`, then `|Psi|^2` depends on
both `psi_A` and `psi_B` multiplicatively, so the evolution of one factor depends
on the other.

### Logarithmic Nonlinearity

The Bialynicki-Birula/Mycielski logarithmic nonlinearity has the form:

```text
F(Psi*, Psi) = b log |Psi|^2
```

This has a special separability property for simple product states because:

```text
log |psi_A psi_B|^2 = log |psi_A|^2 + log |psi_B|^2
```

However, Ho and Hsu argue that this does not solve the general problem. For
superpositions, especially identical-particle states, separability still fails.

### Weinberg-Type Nonlinearities

Weinberg's framework is more systematic because it respects homogeneity under
rescaling of the state vector:

```text
Psi and Z Psi represent the same physical state
```

Ho and Hsu acknowledge this as an important improvement over simpler nonlinear
proposals. But they argue that Weinberg-type nonlinearities still generically
violate separability and therefore locality.

## Free Field Theory Example

The paper gives a concrete example using free scalar field theory.

This is important because free field theory removes ordinary interaction effects
and avoids complications from renormalization. The point is to show that the
nonlocality arises from the nonlinear state evolution itself, not from ordinary
field interactions.

They consider two coherent wave-packet states localized in widely separated
regions `A` and `B`. Coherent states are useful because they are semiclassical,
minimum-uncertainty states and can approximately represent localized particles or
wave packets.

The wavefunctional for two widely separated coherent states approximately
factorizes:

```text
Psi[phi] ≈ psi_A[phi_A] psi_B[phi_B]
```

The appendix proves this approximate factorization. Mixed terms vanish as the
separation between `A` and `B` grows, so the product approximation becomes
arbitrarily accurate for widely separated regions.

Then the paper shows that a generic nonlinear term spoils this factorization.
Even in free field theory, the nonlinear term makes the evolution of the
wavepacket in `A` depend on the wavepacket in `B`.

## Main Conclusion

Ho and Hsu conclude that nonlinear quantum mechanics appears generically
incompatible with relativistic causality. Nonlinear terms in the Schrodinger
equation tend to produce nonlocal effects that are absent in ordinary linear
Lorentz-invariant QFT.

They quote Weinberg's later admission from *Dreams of a Final Theory* that he
could not find a way to extend nonlinear quantum mechanics to special relativity
without "wrecking it altogether."

The paper also briefly speculates about nonlinear modifications of the
Wheeler-DeWitt equation in quantum gravity. Since quantum gravity lacks an
ordinary fixed background notion of locality, nonlinearities might behave
differently there. However, Ho and Hsu caution that such nonlinearities would
likely reappear in semiclassical spacetime and then produce the same locality
problems.

## Relevance To The Talk

This paper is a useful bridge between the older Weinberg/Polchinski story and
Hsu's later AI-assisted work on nonlinear quantum dynamics.

For the talk, the paper can be used to support the following progression:

```text
1. Weinberg proposed a controlled nonlinear generalization of quantum mechanics.

2. Gisin and Polchinski showed that nonlinear quantum mechanics can turn
   entanglement into superluminal signaling.

3. Ho and Hsu recast the issue in QFT language and argued that generic nonlinear
   wavefunctional evolution creates instantaneous entanglement between spacelike
   separated systems.

4. Hsu's later work asks whether AI-assisted reasoning can help identify or
   formalize consistency constraints on nonlinear relativistic quantum dynamics.
```

The important interpretive point is that Ho and Hsu make the pathology look less
like a special measurement-theory oddity and more like a structural conflict
between nonlinear quantum evolution and spacetime locality.

## One-Sentence Summary

Ho and Hsu argue that in the functional Schrodinger picture of quantum field
theory, generic nonlinear modifications of quantum evolution destroy the
factorization of spacelike separated systems and thereby create nearly
instantaneous nonlocal entanglement, even in free field theory.

