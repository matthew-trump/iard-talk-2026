# Tomonaga-Schwinger Equation Basic Summary

## Basic Idea

The Tomonaga-Schwinger equation is the relativistic-QFT version of the Schrodinger
equation.

In ordinary quantum mechanics, the state evolves from one global time slice to the
next:

```text
i d|psi(t)> / dt = H |psi(t)>
```

The whole state is labeled by a single time parameter `t`.

In the Tomonaga-Schwinger formalism, the state is instead attached to an entire
spacelike hypersurface:

```text
|Psi[Sigma]>
```

where `Sigma` is a spacelike slice through spacetime.

The equation says:

> A quantum field theory state is attached to a spacelike hypersurface, and the state
> changes when you locally deform that hypersurface forward in spacetime.

---

## The Equation

Schematically:

```text
i delta |Psi[Sigma]> / delta Sigma(x) = H_int(x) |Psi[Sigma]>
```

Meaning:

- `Sigma` is a spacelike hypersurface.
- `|Psi[Sigma]>` is the quantum state assigned to that hypersurface.
- `x` is a point on the hypersurface.
- `delta / delta Sigma(x)` means: push the hypersurface forward a tiny amount near
  the point `x`.
- `H_int(x)` is the local interaction Hamiltonian density at that spacetime point.

So the equation says:

> If I advance the hypersurface locally near point `x`, the state changes according
> to the local Hamiltonian density there.

---

## How to Picture It

Start with a spacelike hypersurface `Sigma`.

The state `|Psi[Sigma]>` describes the quantum fields on that whole surface.

Now deform a small patch of `Sigma` forward near a point `x`. The Tomonaga-Schwinger
equation tells you how the state changes under that local deformation.

Then deform another patch. Then another. By many small local deformations, you evolve
from one spacelike hypersurface to another.

This replaces the ordinary idea of "evolving from time `t` to time `t + dt`" with a
more relativistic idea:

> evolve by arbitrary local deformations of spacelike slices.

---

## Why This Matters

The ordinary Schrodinger equation uses a preferred global time coordinate.

That is natural in nonrelativistic quantum mechanics, but awkward in relativistic
QFT, where no inertial frame's time coordinate should be physically preferred.

The Tomonaga-Schwinger equation removes that preferred global time by allowing
evolution along arbitrary spacelike hypersurfaces.

---

## The Consistency Condition

The crucial requirement is path independence.

Suppose `x` and `y` are spacelike-separated points on the hypersurface.

You can deform the surface:

1. first near `x`, then near `y`;
2. first near `y`, then near `x`.

Relativistic consistency requires that these two routes give the same final state.

Roughly, this requires:

```text
[H_int(x), H_int(y)] = 0
```

for spacelike-separated `x` and `y`.

This is microcausality: local operations at spacelike separation must commute.

If this condition fails, the final state can depend on the order in which spacelike
deformations are applied. That means the theory depends on the chosen foliation of
spacetime, which is a problem for relativistic covariance.

---

## Relation to Hsu

Hsu uses the Tomonaga-Schwinger formalism to ask whether state-dependent nonlinear
modifications of quantum mechanics can be made compatible with relativistic QFT.

The issue is:

> If the local generator of evolution depends nonlinearly on the global quantum state,
> can local deformations of spacelike hypersurfaces still commute?

Hsu argues that they generically cannot: the nonlinear state-dependence spoils the
Tomonaga-Schwinger integrability condition, so the result depends on the foliation.

Diosi disputes this diagnosis. He argues that, in a proper interaction-picture
formulation, the Tomonaga-Schwinger equation can remain covariant even though
nonlinear quantum mechanics still has Polchinski/Gisin-type signaling problems.

So, for the talk:

> The Tomonaga-Schwinger equation is the mathematical language in which Hsu tries to
> turn the old Weinberg-Polchinski nonlinear-QM signaling problem into a relativistic
> covariance or foliation-independence problem.

---

## One-Line Version

> The Tomonaga-Schwinger equation is the Schrodinger equation rewritten so that QFT
> states evolve by local deformations of arbitrary spacelike hypersurfaces, rather
> than by one preferred global time.
