# Hsu TS Integrability: Recent Discussion Notes

Purpose: preserve the recent discussion after the state-dependent Hamiltonian
nonlinearities note. These notes focus on Hsu's 2026 Tomonaga-Schwinger analysis,
its relation to Ho-Hsu 2014 and Polchinski 1991, and the mathematical clarifications
around Frechet derivatives, hypersurface deformations, product rules, and
microcausality.

## Hsu 2026 As A Covariant Extension Of Ho-Hsu 2014

Hsu's 2026 paper can be understood as an attempted covariant
Tomonaga-Schwinger extension of the concern developed in Ho-Hsu 2014.

Ho-Hsu 2014 works in the functional Schrodinger picture on fixed equal-time slices:

```text
Psi[phi(x), t]
```

It argues that nonlinear state-dependent evolution generically creates
instantaneous entanglement between initially separable spacelike regions.

Hsu 2026 asks the analogous question in a hypersurface-based relativistic setting:

```text
|Psi, Sigma>
```

Instead of asking only whether separated regions remain separable on one chosen
time slicing, it asks whether evolution is independent of the choice of spacelike
foliation:

```text
[delta_x, delta_y] |Psi> = 0
```

The progression is:

```text
Ho-Hsu 2014:
fixed-foliation QFT language
-> nonlinear evolution threatens separability/locality

Hsu 2026:
Tomonaga-Schwinger covariant language
-> nonlinear evolution threatens foliation independence / TS integrability
```

Caveat for the talk: Diosi disputes whether Hsu's 2026 argument succeeds as a
covariance no-go result. It is safest to call it Hsu's attempted covariant
generalization rather than a settled theorem.

## What Ho-Hsu 2014 Added Beyond Polchinski 1991

Polchinski 1991 showed that Weinberg-style nonlinear quantum mechanics creates a
causality problem when applied to entangled separated systems.

The essential Polchinski setup is EPR-like:

```text
Alice and Bob share an entangled state.
Alice chooses a measurement basis.
Bob's reduced density matrix may be the same, but its ensemble decomposition changes.
If Bob's nonlinear evolution depends on the pure-state decomposition, Bob can detect
Alice's choice.
```

So Polchinski's result is:

> Nonlinear quantum mechanics can turn entanglement into superluminal signaling.

Ho and Hsu 2014 showed something related but phrased at a different structural
level. In the functional Schrodinger picture of QFT, nonlinear evolution can
create instantaneous entanglement between initially unentangled spacelike separated
regions:

```text
Psi[phi] = psi_A[phi_A] psi_B[phi_B]
```

becomes, generically,

```text
Psi[phi_A, phi_B]
```

with `A` and `B` dynamically coupled.

Compact distinction:

```text
Polchinski 1991:
Given entanglement, nonlinear QM permits superluminal signaling.

Ho-Hsu 2014:
Generic nonlinear field evolution creates nonlocal entanglement even from initially
unentangled spacelike separated field states.
```

For the talk:

> Polchinski showed that nonlinear QM makes EPR entanglement operationally
> dangerous. Ho and Hsu showed that, in QFT language, the danger is even more
> structural: nonlinear evolution generically destroys separability between
> spacelike separated regions, even before one invokes an EPR measurement protocol.

## Functional Schrodinger Picture

The functional Schrodinger picture is the Schrodinger picture applied to fields
instead of particles.

For an ordinary particle, the wavefunction is a function of position:

```text
psi(x, t)
```

For a quantum field, the configuration is an entire field shape over space:

```text
phi(x)
```

The quantum state is therefore a wavefunctional:

```text
Psi[phi(x), t]
```

It assigns an amplitude to each possible field configuration. It is called
"functional" because `Psi` is a function whose input is itself a function:

```text
ordinary wavefunction:
x -> psi(x)

field wavefunctional:
phi(x) -> Psi[phi(x)]
```

For a scalar field, the functional Schrodinger equation is schematically:

```text
i hbar d_t Psi[phi, t] = H Psi[phi, t]
```

where the Hamiltonian contains functional derivatives such as:

```text
delta / delta phi(x)
```

Ho-Hsu 2014 uses this framework to ask whether a field wavefunctional factorizes
between two spatial regions:

```text
Psi[phi] = psi_A[phi_A] psi_B[phi_B]
```

This is the field-theory version of saying that regions `A` and `B` are initially
unentangled.

### Origin / Citation

There is no single clean origin citation because the idea grows out of canonical
field quantization. For slides, the most useful modern reference is:

**K. Symanzik**, "Schrodinger Representation and Casimir Effect in Renormalizable
Quantum Field Theory," *Nuclear Physics B* **190**, 1-44 (1981).
DOI: <https://doi.org/10.1016/0550-3213(81)90482-X>

A useful pedagogical/modern reference:

**R. Jackiw**, "Analysis on Infinite-Dimensional Manifolds: Schrodinger
Representation for Quantized Fields," MIT-CTP-1632; later included in *Diverse
Topics in Theoretical and Mathematical Physics*, World Scientific (1995).
INSPIRE: <https://inspirehep.net/literature/263889>

Slide wording:

> Functional Schrodinger picture: a QFT Schrodinger representation in which states
> are wavefunctionals `Psi[phi(x),t]` over classical field configurations. Modern
> systematic treatment: Symanzik, *Nucl. Phys. B* **190**, 1 (1981); pedagogical
> formulation: Jackiw, "Schrodinger Representation for Quantized Fields" (1988/1995).

## Unit Normal Versus Frechet Derivative

The unit normal to a Cauchy hypersurface is not defined by the Frechet derivative.
They are different objects.

The unit normal is geometric. Given a spacelike hypersurface `Sigma`, its
future-directed unit normal vector field `n^mu(x)` satisfies:

```text
n^mu tangent-orthogonal to Sigma
g_{mu nu} n^mu n^nu = -1
```

assuming metric signature `(-,+,+,+)`.

The Frechet derivative is a state-space derivative. In Hsu's paper, it measures how
the state-dependent operator

```text
N_x[Psi]
```

changes when the quantum state changes:

```text
D N_x|_Psi [Phi]
```

Meaning:

> the first-order change in `N_x` when `Psi` is varied in the direction `Phi`.

The chain of concepts is:

```text
hypersurface has unit normal n^mu(x)
-> deform Sigma locally along n^mu(x)
-> state |Psi, Sigma> changes by delta|Psi>/delta sigma(x)
-> since N_x depends on |Psi>, N_x changes too
-> that last change is computed with the Frechet derivative
```

The unit normal belongs to spacetime geometry. The Frechet derivative belongs to
functional analysis on state space.

## State Variation Versus Hypersurface Deformation

There are two variations in play.

### 1. Variation Of The State On A Fixed Hypersurface

This is the Frechet derivative part. Hold the hypersurface `Sigma` fixed and
imagine changing the state:

```text
|Psi, Sigma> -> |Psi, Sigma> + epsilon |Phi, Sigma>
```

Then ask how the state-dependent operator changes:

```text
N_x[Psi] -> N_x[Psi + epsilon Phi]
```

The Frechet derivative measures this first-order change:

```text
D N_x|_Psi [Phi]
```

### 2. Deformation Of The Hypersurface

This is the Tomonaga-Schwinger part. Deform the hypersurface locally near a
spacetime point `y`:

```text
Sigma -> Sigma + delta sigma(y)
```

That deformation changes the state according to the TS equation:

```text
delta_y |Psi> = delta |Psi> / delta sigma(y)
```

### Connection By Chain Rule

Because `N_x` depends on `Psi`, and `Psi` changes when the hypersurface changes,
the hypersurface deformation induces a state-space variation:

```text
delta_y N_x = D N_x|_Psi [delta_y Psi]
```

That is the chain rule:

```text
deform hypersurface at y
-> state changes
-> state-dependent operator at x changes
```

## Physical Meaning Of Hypersurface Deformation

A deformation of the hypersurface corresponds physically to advancing the quantum
state locally through spacetime.

In ordinary Schrodinger evolution, the entire equal-time slice advances:

```text
|Psi(t)> -> |Psi(t + dt)>
```

In the Tomonaga-Schwinger picture, the state is attached to a spacelike
hypersurface:

```text
|Psi, Sigma>
```

Instead of advancing the whole surface at once, one may advance a small patch of
the surface near a point `x` in the future-directed normal direction:

```text
Sigma -> Sigma + small bump near x
```

Physically, this means including an additional infinitesimal spacetime volume near
`x` in the region whose dynamics has acted on the state.

The TS equation says:

```text
i hbar delta |Psi, Sigma> / delta sigma(x) = H(x) |Psi, Sigma>
```

Meaning:

> the rate at which the state changes when the hypersurface is locally pushed
> forward at `x` is generated by the local Hamiltonian density there.

The consistency requirement is that if `x` and `y` are spacelike separated, it
should not matter which patch is advanced first:

```text
advance x then y = advance y then x
```

This is TS integrability/foliation independence.

## Global Time

In the fully relativistic Tomonaga-Schwinger setting, there is no preferred global
time in the sense of one universal physical clock shared by all observers.

There are two uses of "global time":

### Ordinary Schrodinger Global Time

In nonrelativistic quantum mechanics:

```text
|Psi(t)>
```

Here `t` is a universal time parameter. The whole system evolves from one global
instant to the next.

### Coordinate Time In A Chosen Relativistic Frame Or Foliation

In relativistic QFT, one often still writes:

```text
|Psi(t)>
```

but `t` usually means the time coordinate of a chosen inertial frame, or more
generally a chosen foliation:

```text
Sigma_t
```

Each value of `t` labels one spacelike hypersurface. This `t` is not an
observer-independent universal time. It is a coordinate or foliation parameter.

Tomonaga-Schwinger avoids privileging that choice. Instead of assuming one
preferred family `Sigma_t`, it allows arbitrary spacelike hypersurfaces `Sigma`
and asks whether the final state is independent of the chosen slicing.

Summary:

```text
Nonrelativistic QM:
t is physical universal time.

Relativistic fixed-frame QFT:
t is coordinate time labeling a chosen slicing.

Tomonaga-Schwinger QFT:
no preferred t; the state is attached to arbitrary spacelike hypersurfaces.
```

## Product Rule In Hsu's Derivation

Hsu seeks the commutator between two TS deformation derivatives:

```text
[delta_x, delta_y] |Psi>
```

where:

```text
delta_x = delta / delta sigma(x)
```

For covariant TS evolution, this should vanish for spacelike separated `x` and
`y`:

```text
[delta_x, delta_y] |Psi> = 0
```

In the nonlinear case:

```text
i hbar delta_x |Psi> = G_x[Psi] |Psi>
```

with:

```text
G_x[Psi] = H(x) + N_x[Psi]
```

The product rule enters when differentiating the product of the state-dependent
generator and the state.

Start with:

```text
delta_y |Psi> = -(i/hbar) G_y[Psi] |Psi>
```

Apply `delta_x`:

```text
delta_x delta_y |Psi>
= -(i/hbar) delta_x (G_y[Psi] |Psi>)
```

Now invoke the product rule:

```text
delta_x (G_y[Psi] |Psi>)
= (delta_x G_y[Psi]) |Psi> + G_y[Psi] delta_x |Psi>
```

This is the same rule as differentiating a matrix times a vector:

```text
d/dt [A(t) v(t)] = (dA/dt) v(t) + A(t) (dv/dt)
```

Even though operator action is not scalar multiplication, it is a bilinear action
of operators on vectors, and the derivative obeys the same product-rule structure.

The chain rule/Frechet derivative appears inside the first product-rule term:

```text
delta_x G_y[Psi] = delta_x N_y[Psi]
                 = D N_y|_Psi [delta_x Psi]
```

## Frechet Derivative: Explicit Versus Implicit

One can derive the nonlinear TS integrability condition symbolically without
explicitly writing the Frechet derivative.

If one carries:

```text
delta_y N_x
```

as "the change of `N_x` induced by deforming the hypersurface at `y`," the
integrability condition becomes:

```text
[H(x), N_y] + [N_x, H(y)] + [N_x, N_y]
+ i hbar (delta_y N_x - delta_x N_y) = 0
```

At that level, no explicit Frechet derivative is needed.

The Frechet derivative enters when evaluating what `delta_y N_x` is for a specific
model.

For example, for:

```text
N_x[Psi] = lambda <Psi|O(x)|Psi> O(x)
```

one needs:

```text
D N_x|_Psi [Phi]
= lambda ( <Phi|O(x)|Psi> + <Psi|O(x)|Phi> ) O(x)
```

Then one sets:

```text
Phi = delta_y Psi
```

Therefore:

```text
derive integrability:
carry delta_y N_x formally

evaluate a model:
compute delta_y N_x using the Frechet derivative
```

So if a derivation leaves the change as `delta_y N_x`, the Frechet derivative is
implicit, not missing.

## Microcausality And TS Integrability

In ordinary linear QFT, the TS equation is:

```text
i hbar delta_x |Psi, Sigma> = H(x) |Psi, Sigma>
```

To get foliation independence, local deformations at spacelike separated points
must commute:

```text
[delta_x, delta_y] |Psi> = 0
```

Using the TS equation, this reduces to:

```text
[H(x), H(y)] = 0       for spacelike x, y
```

after smearing, because local field densities are operator-valued distributions.

This is the Hamiltonian-density version of microcausality. More generally,
microcausality says local observables commute, or fermionic fields anticommute
where appropriate, at spacelike separation:

```text
[O(x), O'(y)] = 0
```

In Hsu's nonlinear case:

```text
G_x[Psi] = H(x) + N_x[Psi]
```

The analogous condition is no longer simply `[H(x), H(y)] = 0`. It becomes the
full state-dependent integrability condition with extra derivative terms.

## Hsu's Three Nonlinear Scenarios: What They Fail At

Hsu discusses three nonlinear scenarios.

### 1. Local Weinberg Expectation-Value Nonlinearity

```text
N_x[Psi] = lambda <O(x)>_Psi O(x)
```

The nonlinear TS integrability condition appears to hold if ordinary
microcausality is assumed. But Hsu argues that state-dependent nonlinear evolution
does not preserve microcausality under evolution, because the evolution is not a
fixed state-independent unitary automorphism of the local operator algebra.

So, in Hsu's view, the local Weinberg case fails at:

```text
dynamical preservation of microcausality
```

### 2. Nonlocal Weinberg-Style Mean-Field Generalization

```text
N_x[Psi] = lambda ∫ d^3y f(x,y) <O(y)>_Psi O(x)
```

This fails more directly at:

```text
TS integrability / foliation independence
```

because a deformation near `y` changes the state-dependent generator at distant
`x`.

### 3. Kaplan-Rajendran Retarded Model

```text
N_x[Psi] = ∫ d^4x1 G_R(x;x1) <O(x1)>_Psi P(x)
```

This also fails, according to Hsu, at:

```text
TS integrability / foliation independence
```

Even though the model uses retarded causal dependence, spacelike-separated points
have overlapping past light cones, so the Frechet derivative terms are generically
nonzero and order-dependent.

Compact statement:

> In Hsu's diagnosis, the three models fail at being foliation-independent
> relativistic quantum dynamics. The local Weinberg case fails because
> state-dependent evolution does not preserve microcausality, while the nonlocal
> mean-field and Kaplan-Rajendran cases fail more directly because the nonlinear
> TS integrability condition is generically violated.

Caveat:

> Diosi challenges whether this is truly a failure of TS covariance rather than a
> restatement of the familiar nonlinear-QM signaling problem.

## Core Of Hsu's Argument About Microcausality

In ordinary linear QFT, Heisenberg evolution is:

```text
O(t) = U†(t,t0) O(t0) U(t,t0)
```

where `U` is state-independent.

This matters because unitary conjugation preserves commutators:

```text
[O_A(t0), O_B(t0)] = 0
```

implies:

```text
[U† O_A U, U† O_B U] = U† [O_A, O_B] U = 0
```

So if two local observables commute at spacelike separation initially, their
evolved versions continue to commute when the theory is local and linear.

Hsu argues that this mechanism breaks in state-dependent nonlinear evolution:

```text
i hbar d|Psi>/dt = H[Psi] |Psi>
```

The corresponding evolution map is not a fixed `U(t,t0)` but more like:

```text
U[Psi; t,t0]
```

Since the map depends on the state being evolved, one cannot write a universal
Heisenberg operator evolution:

```text
O(t) = U† O(t0) U
```

that works for all states and preserves the local operator algebra.

Compact version:

```text
linear QFT:
fixed unitary evolution -> algebra automorphism -> commutators preserved

Weinberg local nonlinear QM:
state-dependent evolution -> no fixed algebra automorphism -> microcausality not guaranteed
```

This is Hsu's core obstruction for the local Weinberg-type nonlinearity.

## Weinberg's 1989 Paper: Methodological Framing

Weinberg's 1989 paper neither ruled in nor ruled out the use of small nonlinear
corrections to quantum mechanics. Rather, it defined a systematic method for
evaluating such corrections.

He was not saying:

```text
Quantum mechanics is definitely nonlinear.
```

Nor was he saying:

```text
All nonlinear corrections are already impossible.
```

Instead, he constructed a controlled formal framework for asking:

```text
If quantum mechanics had small nonlinear corrections, what would they look like,
and how could experiments bound them?
```

Careful formulation:

> Weinberg did not claim to have established nonlinear quantum mechanics as a
> viable replacement for ordinary quantum mechanics, nor did he rule it out from
> the start. He constructed a systematic Hamiltonian framework for small nonlinear
> corrections, preserving key features such as ray-based states and norm-respecting
> evolution, so that such corrections could be analyzed and experimentally
> constrained.

Slide wording:

> Weinberg's 1989 paper was less a proposal that quantum mechanics is nonlinear
> than a disciplined way to make "nonlinear quantum mechanics" precise enough to
> test.

## Slide-Ready Summary

Recent discussion can be compressed into this narrative:

> Polchinski showed that Weinberg-style nonlinear quantum mechanics makes EPR
> entanglement operationally dangerous. Ho and Hsu recast the danger in QFT's
> functional Schrodinger picture, where generic nonlinear state-dependent evolution
> destroys separability between spacelike separated field regions. Hsu's 2026
> paper then attempts to make the issue covariant using Tomonaga-Schwinger
> hypersurface evolution. The key technical point is that state-dependent
> generators introduce extra derivative terms in the TS integrability condition:
> one must differentiate not only the state but also the state-dependent operator.
> Formally, this can be carried as `delta_y N_x`; to evaluate it for a specific
> nonlinearity one uses the Frechet derivative. In Hsu's diagnosis, nonlinear
> state-dependent evolution either fails to preserve microcausality or directly
> violates TS path independence. Diosi disputes whether this establishes a failure
> of TS covariance, so the claim should be presented as contested.

