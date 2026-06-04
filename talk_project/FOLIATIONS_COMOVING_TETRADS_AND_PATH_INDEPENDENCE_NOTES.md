# Foliations, Comoving Tetrads, and Path-Independence Notes

## Context

These notes archive the discussion connecting:

- spacelike Cauchy hypersurface foliations;
- discrete and continuous foliation pictures;
- local slabs of spacetime;
- topology and non-intersection of foliation leaves;
- accelerated worldline comoving tetrads;
- Frenet-Serret / Fermi-Walker observer frames;
- extension of local comoving frames into Cauchy hypersurfaces;
- and the return to Tomonaga-Schwinger integrability/path independence.

The guiding question was whether a local observer-adapted construction, based on the
instantaneous rest frame of an arbitrarily accelerated classical particle, could be
used to parameterize Tomonaga-Schwinger hypersurfaces, at least locally, and what
invariance requirements would make the resulting physics meaningful.

---

## Continuous Foliations and Spacetime Slabs

A continuous foliation is a one-parameter family of spacelike hypersurfaces:

```text
Sigma_s,   s in [s_i, s_f]
```

Each `Sigma_s` is a three-dimensional spacelike surface in four-dimensional
spacetime.

As `s` varies continuously, the union of the hypersurfaces fills out a four-dimensional
spacetime region:

```text
R = union_s Sigma_s
```

In physical spacetime, the family sweeps out a four-dimensional spacetime volume.
In the infinite-dimensional space of hypersurfaces, the map:

```text
s -> Sigma_s
```

is instead a path through the space of possible hypersurfaces.

For a discrete foliation, replace the smooth family with a sequence:

```text
Sigma_0, Sigma_1, ..., Sigma_N
```

The region between neighboring leaves is a spacetime slab:

```text
R_k = region between Sigma_k and Sigma_{k+1}
```

The thickness of a slab is not generally a single invariant number. Locally it is
measured by the proper normal separation:

```text
Delta sigma_k(x)
```

meaning the amount by which `Sigma_{k+1}` lies to the future of `Sigma_k` in the
normal direction near point `x`.

For flat constant-time slices:

```text
Sigma_k:     t = k Delta t
Sigma_{k+1}: t = (k+1) Delta t
```

the slab thickness is simply `Delta t` in that frame.

In the general case, the local thickness is a function over the hypersurface:

```text
Delta sigma_k(x)
```

In the continuum limit:

```text
Delta sigma_k(x) -> delta sigma(x)
```

which is the local normal deformation appearing in the Tomonaga-Schwinger equation.

---

## Topology of Foliations: Non-Intersection of Leaves

For a proper foliation, leaves in the same family do not intersect.

Strictly:

```text
R = union_s Sigma_s
Sigma_s intersect Sigma_s' = empty    for s != s'
```

Each spacetime point in the foliated region lies on exactly one leaf.

If two leaves of the same foliation intersect, the same spacetime event belongs to
two different "times" or evolution steps. That breaks the idea that the foliation
parameter cleanly orders events.

For a discrete foliation:

```text
Sigma_0, Sigma_1, ..., Sigma_N
```

the leaves should likewise be ordered and nonintersecting. Otherwise the slab between
`Sigma_k` and `Sigma_{k+1}` becomes ill-defined.

Important distinction:

- Leaves within one foliation should not intersect.
- Leaves from different foliations may intersect.

The same physical system can be described by multiple different foliations. Within
each foliation, the leaves are disjoint. Across different foliations, slices generally
cross. Tomonaga-Schwinger covariance is precisely the demand that these different
slicings give the same physical results.

---

## Hypersurfaces as Generalized Simultaneity Slices

In flat spacetime, the simplest spacelike hypersurfaces are constant-time planes for
an inertial observer:

```text
t = constant
```

These are surfaces of simultaneity for that observer.

Another inertial observer has different tilted surfaces:

```text
t' = constant
```

In the more general Tomonaga-Schwinger setting, a spacelike hypersurface can be viewed
as a generalized simultaneity slice for some chosen time function:

```text
T(x) = constant
```

The level surfaces:

```text
Sigma_T = { x : T(x) = constant }
```

are the hypersurfaces.

The essential condition is that each `Sigma_T` be spacelike. Equivalently, tangent
displacements within the hypersurface have no increment in the chosen foliation time:

```text
dT = 0
```

The normal direction to a spacelike hypersurface is timelike. Tomonaga-Schwinger
evolution proceeds by pushing the hypersurface forward in this normal direction:

```text
delta sigma(x)
```

---

## Separation Between Leaves

The leaves of a spacelike foliation are locally separated in a timelike normal
direction.

However, "the distance between two hypersurfaces" is not uniquely defined unless one
specifies how points on one leaf are matched to points on the next.

In lapse/shift language, the evolution vector field can be written:

```text
t^mu = N n^mu + N^mu
```

where:

- `n^mu` is the future-directed unit normal to the leaf;
- `N` is the lapse, measuring normal advance;
- `N^mu` is the shift, tangent to the leaf.

The normal part is timelike. The total coordinate displacement can also include a
tangential shift.

For Tomonaga-Schwinger discussions, the main object is the local normal deformation:

```text
delta sigma(x)
```

---

## Local Normal Neighborhood Theorem

For a smooth spacelike leaf of a well-behaved foliation, there is a nonzero local
spacetime neighborhood in which short normal displacements from that leaf intersect
nearby leaves uniquely.

This is an instance of standard local geometry:

- the tubular neighborhood theorem;
- Gaussian normal coordinates;
- and the local product structure theorem for foliations.

A precise version:

> Given a smooth spacelike hypersurface in a Lorentzian manifold, there exists a
> sufficiently small neighborhood in which the exponential map along the timelike
> normal defines a local product structure. In that neighborhood, short normal curves
> from the hypersurface intersect nearby leaves of a smooth spacelike foliation
> uniquely.

Important qualifications:

- local, not global;
- requires smooth embedded hypersurfaces;
- normal geodesics must not have developed caustics or intersections;
- the foliation must be regular in the neighborhood.

Globally, normal curves can cross, form caustics, leave the coordinate patch, or fail
to provide a good map from one leaf to all later leaves.

---

## States on Lorentzian Spacetime

A quantum field state is not assigned to a single spacetime point. It is assigned to
an entire spacelike Cauchy hypersurface:

```text
|Psi[Sigma]>
```

where `Sigma` lies in a Lorentzian spacetime.

A Lorentzian spacetime is a smooth manifold with a Lorentzian-signature metric,
which defines light cones, timelike directions, spacelike directions, null directions,
and causal structure.

Cases:

1. **Minkowski spacetime**
   Flat Lorentzian spacetime with global inertial frames related by the Poincare
   group.

2. **Accelerated coordinates in Minkowski spacetime**
   Same flat geometry, but described by non-inertial observers or nontrivial
   foliations, such as Rindler-like constructions.

3. **Curved Lorentzian spacetimes**
   General-relativistic cases. Usually no global Poincare symmetry, but local Lorentz
   structure remains.

4. **General globally hyperbolic Lorentzian backgrounds**
   Spacetimes admitting suitable spacelike Cauchy hypersurfaces on which field states
   can be specified.

The Tomonaga-Schwinger picture is:

```text
Lorentzian spacetime M
spacelike Cauchy surface Sigma subset M
state |Psi[Sigma]> assigned to Sigma
```

Evolution replaces one hypersurface with another:

```text
Sigma_initial -> Sigma_final
|Psi[Sigma_initial]> -> |Psi[Sigma_final]>
```

---

## Comoving Tetrads Along Accelerated Worldlines

Consider a classical particle with timelike worldline:

```text
z^mu(tau)
```

where `tau` is the particle's proper time.

The four-velocity is:

```text
u^mu(tau) = dz^mu / d tau
```

with:

```text
u^mu u_mu = -1
```

in the `(-,+,+,+)` signature convention.

At each point on the worldline, the particle has an instantaneous rest frame. The
time axis is:

```text
e_0^mu(tau) = u^mu(tau)
```

The spatial axes:

```text
e_i^mu(tau),   i = 1,2,3
```

span the rest space orthogonal to `u^mu`:

```text
e_i . u = 0
```

Neighboring comoving frames can be related by **Fermi-Walker transport**, the natural
nonrotating transport law along an accelerated worldline. For a vector `V^mu`:

```text
dV^mu/dtau = (u^mu a_nu - a^mu u_nu) V^nu
```

where:

```text
a^mu = du^mu/dtau
```

is the four-acceleration.

This preserves:

```text
e_i . u = 0
e_i . e_j = delta_ij
```

and introduces no artificial rotation according to the accelerated observer.

---

## Frenet-Serret / Serret-Frenet Worldline Invariants

For a sufficiently regular timelike worldline in flat spacetime, the spacetime
Frenet-Serret frame gives a canonical moving tetrad.

Start with the unit tangent:

```text
e_0 = u = dz/ds
```

where `s` is proper time / metric arc length.

Successive orthonormal directions are built from derivatives of the curve. The
invariant scalar functions are:

```text
kappa      = proper acceleration magnitude
tau_1      = torsion
tau_2      = hypertorsion
```

depending on notation.

With one common sign convention, the equations are:

```text
de_0/ds = kappa e_1
de_1/ds = kappa e_0 + tau_1 e_2
de_2/ds = -tau_1 e_1 + tau_2 e_3
de_3/ds = -tau_2 e_2
```

The attraction is that the scalars:

```text
kappa(s), tau_1(s), tau_2(s)
```

are Lorentz invariant. They characterize the local geometry of the worldline
independent of coordinates.

Interpretation:

- `kappa`: how strongly the worldline departs from inertial motion;
- `tau_1`: how the acceleration direction rotates relative to the osculating plane;
- `tau_2`: how the curve twists out of the next-order hyperplane.

Using an arbitrary parameter `lambda` instead of proper time is allowed if:

```text
ds/dlambda != 0
```

smoothly along the curve. The invariants are still cleanly defined with respect to
proper time `s`, then composed with `s(lambda)`:

```text
kappa(lambda) = kappa(s(lambda))
tau_1(lambda) = tau_1(s(lambda))
tau_2(lambda) = tau_2(s(lambda))
```

If the equations are written directly in `lambda`, the coefficients acquire factors
of:

```text
ds/dlambda
```

The key conceptual distinction:

> The Frenet-Serret tetrad gives a canonical local frame along the worldline,
> determined by Lorentz-invariant data of the curve. Turning that local moving frame
> into global spacelike hypersurfaces is an additional foliation problem.

---

## Local Comoving Foliations

If the quantum state is considered only locally around the classical trajectory, the
comoving tetrad can define a local family of spacelike slices.

Construction in flat spacetime:

```text
z^mu(tau)          classical worldline
u^mu(tau)          four-velocity
e_i^mu(tau)        comoving spatial tetrad vectors
Sigma_tau          local rest-space slice at proper time tau
|Psi[Sigma_tau]>   field state represented on that local slice
```

Nearby spacetime points can be parameterized as:

```text
x^mu(tau, X^i) = z^mu(tau) + X^i e_i^mu(tau)
```

This is essentially the Fermi-normal-coordinate construction, or a related accelerated
tetrad coordinate system if the tetrad is not Fermi-Walker transported.

Therefore:

> In a tubular neighborhood of an accelerated worldline, a comoving tetrad can define
> a local foliation by instantaneous rest-space slices. One may represent a
> Tomonaga-Schwinger state locally on these slices, using the particle's proper time
> as the foliation parameter.

Caveats:

- these are generally local hypersurface patches, not guaranteed global Cauchy
  surfaces;
- for arbitrary acceleration, instantaneous rest spaces may intersect if extended too
  far;
- a Tomonaga-Schwinger state is usually defined on a complete spacelike Cauchy
  surface, so a local tube is more naturally a local algebra/subsystem description;
- the tetrad foliation is a convenient observer-adapted representation, not extra
  physical structure unless the theory makes it so.

---

## Extending Local Comoving Frames to Full Cauchy Hypersurfaces

Using the comoving tetrad as starting data, one can often construct extended spacelike
Cauchy hypersurfaces filling a desired region of spacetime, while preserving a proper
foliation.

The construction:

1. Start with the accelerated worldline:

```text
z^mu(tau)
```

2. At each `tau`, take the comoving tetrad:

```text
e_0^mu(tau) = u^mu(tau)
e_i^mu(tau)
```

3. Near the worldline, define the local instantaneous rest-space patch:

```text
x^mu(tau, X^i) = z^mu(tau) + X^i e_i^mu(tau)
```

4. Extend that patch outward into a complete spacelike Cauchy hypersurface:

```text
Sigma_tau
```

5. Choose the extensions smoothly in `tau`, avoiding intersections between leaves.

If successful, this gives a proper foliation:

```text
{ Sigma_tau }
```

with each leaf anchored to the particle's instantaneous rest frame along the
worldline.

The key limitation:

> The tetrad gives canonical local data along the worldline, but it does not uniquely
> determine the full hypersurface away from the worldline.

The extended Cauchy surfaces require extra choices away from the trajectory. In flat
Minkowski spacetime this is usually flexible, but one must avoid:

- intersections between leaves;
- caustics;
- horizons or coordinate breakdowns;
- loss of spacelikeness.

A precise way to formulate the extension is through a time function:

```text
T(x)
```

such that:

```text
T(z(tau)) = tau
```

and near the worldline:

```text
grad_mu T |_{z(tau)} proportional to u_mu(tau)
```

If:

```text
grad_mu T is timelike
```

then the level sets:

```text
Sigma_tau = { x : T(x) = tau }
```

are spacelike.

So the clean construction is:

> Use the comoving tetrad to specify local conditions on a time function near the
> worldline, then extend that time function smoothly to the desired spacetime region
> with timelike gradient everywhere. Its level sets give the extended foliation.

---

## Invariance Requirements

If the extended Cauchy hypersurfaces are partly a choice of representation, then the
physics must be invariant under transformations that preserve the foliation structure
or, more strongly, under changes of foliation itself.

There are two related requirements.

### 1. Foliation-Preserving Transformations

Suppose a foliation has been built:

```text
Sigma_tau
```

anchored to the comoving tetrad along the worldline.

One can change coordinates within that foliated spacetime without changing the leaves
as physical slices. These are foliation-preserving transformations, roughly:

```text
tau' = f(tau)
X'^i = X'^i(tau, X^j)
```

They relabel the same foliation or move coordinates around within each leaf.

Physics should be invariant under these. Otherwise predictions would depend on
arbitrary coordinates on the same hypersurfaces.

### 2. Foliation-Choice Independence

More strongly, the extension from the local comoving tetrad patch to a full Cauchy
hypersurface is not unique.

One can choose different global extensions:

```text
Sigma_tau
tilde{Sigma}_tau
```

that agree near the worldline but differ far away, or even different foliations
connecting the same initial and final surfaces.

If the extension is not physical, observables localized near the trajectory should not
depend on it.

This is the Tomonaga-Schwinger lesson:

> A meaningful covariant dynamics should not depend on arbitrary choices of spacelike
> slicing.

The mathematical condition is the integrability/path-independence condition:

```text
[ delta/delta sigma(x), delta/delta sigma(y) ] |Psi[Sigma]> = 0
```

for spacelike-separated local deformations.

If this holds, changing the foliation away from the worldline does not change the
final physical state, except by the expected unitary equivalence.

If it fails, the theory has introduced a preferred slicing or a dependence on the
arbitrary extension of the comoving frame. That is suspect unless the foliation itself
is promoted to real physical structure.

---

## Clean Formulation

> If the Cauchy foliation is auxiliary, the dynamics must be invariant under
> foliation-preserving coordinate transformations and independent of arbitrary
> foliation extensions. Otherwise the theory's predictions depend on representational
> choices rather than physical data.

---

## One-Line Version

> A comoving tetrad supplies natural local observer data along an accelerated
> worldline, but any extended Cauchy foliation built from it is auxiliary unless the
> theory makes it physical; meaningful covariant dynamics must therefore be
> foliation-preserving and path-independent.
