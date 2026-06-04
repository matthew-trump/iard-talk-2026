# Comoving Tetrad / Foliation Discussion: Prompts and Responses

Purpose: preserve the recent discussion explicitly as prompt-response material for
possible use in section 6 of the talk and as a seed for later paper development.

The central thread:

> Can a comoving tetrad along an arbitrarily accelerated classical worldline provide
> local observer-adapted hypersurface data for Tomonaga-Schwinger states, and what
> invariance/path-independence conditions are required if those hypersurfaces are
> extended into Cauchy foliations?

---

## 1. Continuous Foliations and Spacetime Volume

### Prompt

All right next phase of the discussion. We would like to discuss we definite families
of discrete foliations. The coontinuos nature of the evolving hypersurface defines a
hypervolume in hyperspace, right?

### Response

Yes, but I would phrase it carefully.

A continuously evolving spacelike hypersurface defines a **spacetime region swept out
by the hypersurfaces**, not usually a "hypervolume in hyperspace."

Suppose you have a one-parameter family of spacelike hypersurfaces:

```text
Sigma_s,   s in [s_i, s_f]
```

Each `Sigma_s` is a 3-dimensional spacelike surface in 4-dimensional spacetime.

As `s` varies continuously, the union of all these hypersurfaces fills out a
4-dimensional spacetime region:

```text
R = union_{s in [s_i, s_f]} Sigma_s
```

So if each `Sigma_s` is a 3D slice, and `s` supplies one additional continuous
parameter, the family sweeps out a 4D region of spacetime.

That is the object over which the Tomonaga-Schwinger evolution is being integrated.

The phrase "hyperspace" could mean the infinite-dimensional space of all possible
hypersurfaces. In that sense, the path:

```text
s -> Sigma_s
```

is a **curve in the space of hypersurfaces**, not a volume. The swept-out physical
spacetime region is the 4D volume between the initial and final hypersurfaces.

So there are two related pictures:

```text
Physical spacetime:
Sigma_s sweeps out a 4D spacetime volume R.
```

```text
Space of hypersurfaces:
s -> Sigma_s is a path through the infinite-dimensional configuration space of
hypersurfaces.
```

For the next phase about **discrete foliations**, the continuous version is useful
because a discrete foliation is like replacing the smooth path:

```text
Sigma_s
```

with a sequence:

```text
Sigma_0, Sigma_1, Sigma_2, ..., Sigma_N
```

Each step advances the hypersurface through a finite slab of spacetime:

```text
R_k = region between Sigma_k and Sigma_{k+1}
```

Then the full evolution is built from a product of finite evolution operators across
those slabs.

The continuum Tomonaga-Schwinger equation is recovered when the slabs become
infinitesimally thin.

---

## 2. Thickness of a Spacetime Slab

### Prompt

Slab of spacetime. How thick is it?

### Response

A spacetime "slab" has whatever thickness is set by the separation between two
neighboring hypersurfaces in your chosen discrete foliation.

If you have:

```text
Sigma_k
Sigma_{k+1}
```

then the slab is the 4D region between them:

```text
R_k = region swept out going from Sigma_k to Sigma_{k+1}
```

Its "thickness" is not a single invariant number in general, because the two
hypersurfaces need not be parallel or uniformly separated.

Locally, the thickness is measured by the **proper normal separation** between the two
hypersurfaces at each point:

```text
Delta sigma_k(x)
```

That means:

> how far `Sigma_{k+1}` lies from `Sigma_k` in the future-directed normal direction
> near the point `x`.

If the foliation is simple, say flat constant-time slices in one inertial frame:

```text
Sigma_k:     t = k Delta t
Sigma_{k+1}: t = (k+1) Delta t
```

then the slab thickness is just:

```text
Delta t
```

in that frame.

But for a general curved or tilted foliation, the thickness can vary over space:

```text
Delta sigma_k(x)
```

Some parts of the hypersurface may advance more than others.

So:

- **simple flat foliation:** slab thickness = constant `Delta t`;
- **general foliation:** slab thickness = local function `Delta sigma_k(x)`;
- **continuum limit:** `Delta sigma_k(x) -> 0`.

In Tomonaga-Schwinger language, the infinitesimal version of the slab thickness is
exactly:

```text
delta sigma(x)
```

the local normal deformation of the hypersurface at `x`.

For a discrete foliation, replace that infinitesimal object by a finite local step:

```text
delta sigma(x) -> Delta sigma_k(x)
```

The thinner the slabs, the closer the discrete product of evolution operators is to
the continuous Tomonaga-Schwinger evolution.

---

## 3. Topology: Can Leaves Intersect?

### Prompt

Ah here we get to the point--the topology of these foliations. They can intersect?

### Response

For a **proper foliation**, no: the leaves should not intersect.

A foliation of a spacetime region is a decomposition into disjoint hypersurfaces:

```text
R = union of Sigma_s
Sigma_s intersection Sigma_s' = empty   for s != s'
```

Each spacetime point in the region lies on exactly one leaf of the foliation.

So if two hypersurfaces in the same family intersect, that family is not a foliation
in the strict sense. It is just a collection of hypersurfaces.

Why non-intersection matters:

If two leaves intersect, then the same spacetime event would belong to two different
"times" or two different evolution steps. That breaks the idea that the foliation
parameter orders events cleanly.

For Tomonaga-Schwinger evolution, you normally want a smooth family of
nonintersecting spacelike Cauchy hypersurfaces. That gives you a clean evolution
label:

```text
Sigma_s
```

with each `s` representing one complete "instant" of the field state.

However, two clarifications:

1. **Different foliations can intersect each other.**
   A leaf from foliation A can intersect a leaf from foliation B. That is fine.
   Foliation independence is precisely the demand that different slicings, which may
   cross each other, lead to the same final state.

2. **One foliation's own leaves should not intersect.**
   Within a single chosen foliation:

```text
Sigma_s and Sigma_s'
```

should be disjoint for `s != s'`.

For discrete foliations:

```text
Sigma_0, Sigma_1, ..., Sigma_N
```

you also want the leaves ordered and nonintersecting. Each slab between:

```text
Sigma_k and Sigma_{k+1}
```

should be a well-defined spacetime region.

If adjacent surfaces intersect, the "slab" becomes ill-defined: in one spatial region
`Sigma_{k+1}` may lie to the future of `Sigma_k`, while elsewhere it may cross back.
That can destroy the causal ordering needed for a clean hypersurface evolution.

So the clean answer is:

> Leaves within a single foliation should not intersect. Leaves from different
> foliations may intersect, and covariance/foliation independence is precisely the
> claim that those different slicings give the same physics.

---

## 4. Same System, Multiple Foliations

### Prompt

Ah so the same system can be characters by multiple foliations?

### Response

Yes. The same physical system can be described using many different foliations.

That is the whole point.

In relativistic QFT, there should be no preferred way to slice spacetime into
"instants." One observer might use flat surfaces of constant `t`. Another observer
might use tilted constant `t'` surfaces. A third description might use curved
spacelike hypersurfaces.

All of these can be valid descriptions of the same physical process:

```text
Foliation A:  Sigma_s
Foliation B:  Sigma'_r
Foliation C:  Sigma''_u
```

They may slice the same spacetime region differently.

Within each foliation, its own leaves should not intersect. But leaves from different
foliations can and generally do intersect.

Tomonaga-Schwinger covariance says:

> If you evolve the quantum state from the same initial hypersurface to the same final
> hypersurface using different intermediate foliations, you should get the same final
> physical state.

So the same system can be characterized by multiple foliations, just as the same
relativistic event can be described in multiple coordinate systems.

The physical content should not depend on the foliation. The foliation is part of the
description, not extra physics.

That is why Hsu's issue is serious: if nonlinear state-dependent evolution makes the
final state depend on the chosen foliation, then the theory has introduced unphysical
structure, namely a preferred or dynamically relevant slicing of spacetime.

---

## 5. Hypersurfaces as Simultaneity Slices

### Prompt

Ah these surfaces are those events that are simultaneous to an observer?

### Response

Sometimes, yes. The simplest examples of spacelike hypersurfaces are surfaces of
simultaneity for an inertial observer.

In flat spacetime, an inertial observer with time coordinate `t` has hypersurfaces:

```text
t = constant
```

Each one is the set of events that observer regards as simultaneous.

Another inertial observer moving relative to the first has a different time coordinate
`t'`, with different hypersurfaces:

```text
t' = constant
```

Those are tilted relative to the first observer's slices.

So yes:

> A spacelike hypersurface can be interpreted as a "simultaneous now" for some
> observer or reference frame.

But the Tomonaga-Schwinger formalism is more general.

The hypersurfaces do not have to be flat constant-time planes of inertial observers.
They can be curved spacelike Cauchy surfaces. They may correspond to:

- accelerated observers,
- arbitrary coordinate choices,
- curved spacetime slicings,
- or just a mathematical slicing convenient for calculation.

The essential requirement is not that the surface is "simultaneous" for a simple
inertial observer, but that it is spacelike and Cauchy-like: it can serve as a complete
"instant" on which the field state is specified.

So the careful version is:

> In simple cases, the hypersurfaces are surfaces of simultaneity for an observer.
> More generally, they are arbitrary spacelike Cauchy surfaces that play the role of
> generalized instants in relativistic quantum dynamics.

---

## 6. Level Sets of a Time Function

### Prompt

But they are simultaneous according the t coordinate of some family of references
frame defined by arbitrary spacelike Cauchy surfaces. That's what defines the
hypersurface. Zero locally for spacetime surface.

### Response

Yes, basically.

A spacelike Cauchy hypersurface can be regarded as a generalized "surface of
simultaneity" for some chosen time function.

You define a scalar time coordinate:

```text
T(x)
```

Then the hypersurfaces are level sets:

```text
Sigma_T : T(x) = constant
```

So all events on a given `Sigma_T` are "simultaneous" with respect to that chosen
`T` coordinate.

But this is more general than an inertial reference frame. In special relativity, an
inertial observer's simultaneity surfaces are flat planes:

```text
t = constant
```

In Tomonaga-Schwinger, the surfaces can be curved, tilted, or nonuniform. They come
from an arbitrary foliation:

```text
Sigma_s
```

where `s` is just a label or time function.

The key geometric condition is that each `Sigma_s` is **spacelike**:

> any tangent vector lying within the hypersurface is spacelike or zero, never
> timelike.

Equivalently, in coordinates adapted to the foliation:

```text
T = constant
```

motion within the hypersurface has:

```text
dT = 0
```

So yes: locally, the hypersurface is a "zero time increment" surface for that chosen
time coordinate. But physical proper time still exists along timelike worldlines
crossing the surface.

The normal direction to the surface is timelike. Evolution proceeds by pushing the
hypersurface forward along its normal direction:

```text
delta sigma(x)
```

So the clean version is:

> A spacelike hypersurface is a generalized simultaneity slice: it is a level surface
> of some chosen time function. Points on it have the same foliation time `T`, and
> tangent displacements within it have no `dT` component. The Tomonaga-Schwinger
> formalism lets us choose such slices arbitrarily, provided physical evolution is
> independent of that choice.

---

## 7. Timelike Separation Between Leaves

### Prompt

Are the hypersurfaces of a arbitrary foliation always separated by a timelike
distance?

### Response

Not pointwise in the naive sense, because two different hypersurfaces do not come
with a unique pairing of points unless you choose a flow or coordinate system.

But in a well-behaved foliation by spacelike Cauchy hypersurfaces, the separation
from one leaf to the next is normally along a **timelike normal direction**.

If you choose a foliation:

```text
Sigma_s
```

then locally you can describe the motion from `Sigma_s` to `Sigma_{s+ds}` as:

```text
normal advance + tangential shift
```

The normal advance is timelike because the normal to a spacelike hypersurface is
timelike.

So in adapted language:

```text
delta x^mu = N n^mu ds + shift^mu ds
```

where:

- `n^mu` is the future-directed unit normal to the hypersurface, timelike;
- `N` is the lapse;
- `shift^mu` lies tangent to the hypersurface.

The **normal part** of the separation is timelike.

But the total coordinate displacement between a chosen point on one surface and a
chosen point on the next may include a tangential shift. Depending on how one
identifies "the same spatial point" across slices, the connecting displacement need
not be purely normal.

For Tomonaga-Schwinger discussions, especially Hsu's simplified notation, one usually
focuses on the local **normal deformation**:

```text
delta sigma(x)
```

That is the timelike advance of the surface at point `x`.

So the careful answer:

> The leaves themselves are spacelike. The normal direction along which one locally
> advances a leaf is timelike. But "the distance between two hypersurfaces" is not
> uniquely defined unless you specify how points on one leaf are matched to points on
> the next. With a chosen lapse/shift, the normal separation is timelike, while the
> total displacement may include tangential shift.

---

## 8. Normal Curves and Later Leaves

### Prompt

yes any timelike normal to a hypersurace will intersect all subsequent surfaces in the
foliation?

### Response

For a sufficiently nice foliation, yes locally, but not guaranteed globally without
extra assumptions.

If you have a smooth foliation by nonintersecting spacelike Cauchy hypersurfaces:

```text
Sigma_s
```

then at a point `p in Sigma_s`, the future-directed timelike normal points off the
surface toward nearby later leaves. For sufficiently small `ds`, the normal geodesic
from `p` will intersect `Sigma_{s+ds}` exactly once.

So locally:

> yes, the timelike normal from one leaf intersects nearby subsequent leaves.

Globally, however, a normal curve to one hypersurface need not remain normal to later
hypersurfaces, and it may not intersect every later leaf cleanly unless the foliation
is well-behaved and the normal flow has no caustics or pathologies.

Reasons it can fail globally:

- normal geodesics can focus and cross;
- the foliation can have nontrivial lapse/shift;
- the normal from one leaf may leave the coordinate patch;
- in curved spacetime, the normal congruence can develop caustics;
- a foliation can be smooth as a set of leaves even if the geodesic normals from one
  leaf are not a global coordinate grid.

In canonical language, the evolution vector field is usually written:

```text
t^mu = N n^mu + N^mu
```

where:

- `n^mu` is the unit normal;
- `N` is the lapse;
- `N^mu` is the shift tangent to the hypersurface.

The actual mapping from one leaf to the next follows `t^mu`, not necessarily the
pure normal `n^mu`.

So the careful answer is:

> Locally, the future timelike normal from a spacelike leaf intersects nearby later
> leaves. Globally, whether it intersects all subsequent leaves depends on the
> foliation and spacetime geometry. The foliation itself guarantees each timelike
> worldline, if the leaves are Cauchy surfaces, crosses each leaf once, but it does
> not guarantee that the specific normal geodesics from one leaf provide a global
> intersection map for all later leaves.

---

## 9. Local Normal Neighborhood Theorem

### Prompt

For a given foliation, for each hypersurface in the foliation, there exists a
nonvanishing spacetime region in the vicinity of that foliation for which a normal
will interface all hypersurfaces of the foliation within that region?

### Response

Yes, locally that is right.

For a smooth foliation by spacelike hypersurfaces, around any given leaf `Sigma_s`
and any point `p` on it, there is a small spacetime neighborhood in which the
foliation looks like a clean stack of nonintersecting spacelike slices.

In that local neighborhood:

- each hypersurface `Sigma_s` has a well-defined timelike normal;
- the normal direction is nonzero and transverse to the nearby leaves;
- following the normal from `Sigma_s` intersects nearby leaves `Sigma_{s+ds}`;
- the local slab between nearby leaves is well-defined.

So locally you can picture:

```text
Sigma_s
Sigma_{s+ds}
Sigma_{s+2ds}
```

as a stack, with short timelike normal segments connecting one slice to the next.

The mathematical reason is basically the tubular-neighborhood idea: a smooth embedded
spacelike hypersurface has a neighborhood that can be parameterized by points on the
hypersurface plus a small displacement along the normal direction.

The caveat is that this is local. It need not extend globally through the whole
foliation because normal curves can develop caustics, cross each other, leave the
coordinate patch, or fail to remain a good way of labeling points on later
hypersurfaces.

So the clean version is:

> For any smooth spacelike leaf of a well-behaved foliation, there is a nonzero local
> spacetime neighborhood in which short normal displacements from that leaf intersect
> nearby leaves of the foliation uniquely. This gives the local geometric meaning of
> the Tomonaga-Schwinger deformation `delta sigma(x)`. Globally, one should not
> assume those normal curves provide a valid map through the entire foliation.

### Prompt

Is the statement I just made an existing theorem?

### Response

Yes, it is essentially a standard local result, but it goes by a few related names
depending on the exact formulation.

The closest names are:

1. **Tubular neighborhood theorem**
   A smooth embedded hypersurface has a neighborhood diffeomorphic to its normal
   bundle. In Lorentzian geometry, for a spacelike hypersurface, the normal bundle is
   timelike. So locally you can move a small amount along the normal direction and get
   a well-defined spacetime neighborhood.

2. **Gaussian normal coordinates**
   Near a spacelike hypersurface, one can often introduce coordinates by shooting
   timelike normal geodesics from the hypersurface. Locally, this gives coordinates:

```text
(tau, y^1, y^2, y^3)
```

where `tau` measures proper time along the normal direction and the `y^i` label
points on the hypersurface.

3. **Local product structure theorem for foliations**
   A smooth foliation locally looks like a product:

```text
neighborhood ~= leaf patch x interval
```

The leaves are locally just the slices:

```text
s = constant
```

Your statement combines these ideas. A precise version would be:

> Given a smooth spacelike hypersurface in a Lorentzian manifold, there exists a
> sufficiently small neighborhood in which the exponential map along the timelike
> normal defines a local product structure. In that neighborhood, short normal curves
> from the hypersurface intersect nearby leaves of a smooth spacelike foliation
> uniquely.

The important qualifications are:

- **local**, not global;
- requires smooth embedded hypersurfaces;
- normal geodesics must not yet develop caustics or intersections;
- the foliation must be regular/non-singular in that neighborhood.

So yes: what you said is an instance of the tubular neighborhood / Gaussian normal
coordinate construction, together with the local product structure of smooth
foliations.

---

## 10. States on Lorentzian Spacetimes

### Prompt

Give me an example of a state Psi. Describe the general features of a state.

### Response

A simple example is a one-particle state of a scalar quantum field.

Start with the vacuum:

```text
|0>
```

Then create a particle with momentum `p`:

```text
|p> = a^\dagger(p) |0>
```

That is a state `|Psi>`.

More generally, a one-particle wavepacket would be:

```text
|Psi> = integral d^3p f(p) a^\dagger(p) |0>
```

where `f(p)` is a momentum-space wavefunction telling you the amplitude for the
particle to have momentum `p`.

In ordinary nonrelativistic QM, a state might be:

```text
|psi> = integral d^3x psi(x) |x>
```

where `psi(x)` is the amplitude to find the particle at position `x`.

In QFT, the state is richer. It can contain superpositions of different particle
numbers:

```text
|Psi> =
c0 |0>
+ integral d^3p c1(p) a^\dagger(p)|0>
+ integral d^3p d^3q c2(p,q) a^\dagger(p)a^\dagger(q)|0>
+ ...
```

So a general QFT state can be a superposition of:

- vacuum,
- one-particle states,
- two-particle states,
- many-particle states,
- field configurations,
- entangled states across spatial regions.

General features:

1. It lives in a Hilbert space.
2. It is usually normalized.
3. Overall phase is physically irrelevant.
4. It supports superposition.
5. It determines measurement probabilities.
6. It determines expectation values.
7. In QFT, it is defined relative to a hypersurface.
8. It may encode entanglement.

For the Hsu discussion, the important point is:

> `|Psi>` is not just a number or local field value. It is the full quantum state on a
> spacelike hypersurface. If the nonlinear generator `N_x[Psi]` depends on `Psi`, it
> may depend on global information about the entire hypersurface, including
> spacelike-separated degrees of freedom.

### Prompt

A state is defined on a Lorenz manifold at some point in its history?

### Response

Close, but sharper:

> a state is defined on a spacelike Cauchy hypersurface within a Lorentzian
> spacetime.

In ordinary nonrelativistic QM:

```text
|psi(t)>
```

means the state at time `t`.

In relativistic QFT / Tomonaga-Schwinger language:

```text
|Psi[Sigma]>
```

means the state assigned to the spacelike hypersurface `Sigma`.

The hypersurface `Sigma` is like a generalized "instant" of the system. It cuts
across spacetime and contains all spatial degrees of freedom at that instant.

So:

```text
Lorentzian spacetime M
spacelike Cauchy surface Sigma subset M
state |Psi[Sigma]> assigned to Sigma
```

A local spacetime point `x in Sigma` is where an operator density such as `H_int(x)`
acts locally. But the state itself belongs to the whole hypersurface.

### Prompt

yes that's what I mean. defined on a spacelike hypersurface within a Lorentzian
spacetime. By Lorentzian spacetime we include global insertial frames related to each
other by the Poincare transformations, as well as arbitrary geometries, including the
ones from general relativity, and others related to acceleration particl motion?

### Response

Yes, with one important distinction.

A **Lorentzian spacetime** means a smooth manifold equipped with a metric of
Lorentzian signature, roughly:

```text
(-, +, +, +)
```

or the opposite convention. That metric defines light cones, timelike/spacelike/null
directions, causal structure, and spacelike hypersurfaces.

But:

- **Flat Minkowski spacetime** has global inertial frames related by Poincare
  transformations.
- **Curved GR spacetimes** generally do **not** have global inertial frames or global
  Poincare symmetry.
- They do have **local inertial frames**: near any point, spacetime looks
  approximately Minkowskian, and tangent-space physics has local Lorentz symmetry.

Clean taxonomy:

1. **Minkowski spacetime**
   Flat Lorentzian spacetime. Has global inertial frames related by the Poincare
   group.

2. **Accelerated coordinates in Minkowski spacetime**
   Same flat spacetime, but described by non-inertial observers or foliations, e.g.
   Rindler coordinates. No new spacetime geometry, just a different
   slicing/coordinate system.

3. **Curved Lorentzian spacetimes**
   General relativity cases. The metric is dynamical or externally specified. Usually
   no global Poincare symmetry, but local Lorentz structure remains.

4. **General Lorentzian manifolds used as backgrounds**
   Any spacetime geometry where one can define causal structure and, if well behaved,
   spacelike Cauchy hypersurfaces.

For Tomonaga-Schwinger/QFT language, the key requirement is usually not "global
inertial frame," but:

> a Lorentzian spacetime admitting suitable spacelike Cauchy hypersurfaces, so the
> field state can be assigned to a complete spacelike slice.

That condition is often called **global hyperbolicity**.

So the refined statement is:

> A QFT state in the Tomonaga-Schwinger picture is defined on a spacelike Cauchy
> hypersurface inside a Lorentzian spacetime. In flat spacetime, different global
> inertial descriptions are related by Poincare transformations. In curved or
> accelerated-coordinate settings, one instead works with arbitrary spacelike
> foliations, local Lorentz structure, and, when available, globally hyperbolic
> evolution between Cauchy surfaces.

One caveat: in curved spacetime, notions like "vacuum," "particle," and "positive
frequency" are often not unique. But the idea of a state assigned to a spacelike
Cauchy surface still makes sense in the appropriate algebraic or canonical
formulations.

---

## 11. Comoving Tetrads Along Arbitrarily Accelerated Worldlines

### Prompt

I am interested in defining a general set of reference frames defined by the
instantaneous rest freame of a (classical) particle undergoing arbitrary acceleration.
Such comoving frames are related to each other, one after another, along the proper
time trajectory of the particle.

### Response

Yes. The standard way to formalize this is with a **comoving tetrad** along the
particle's worldline, usually chosen to be **Fermi-Walker transported**.

Let the classical particle have worldline:

```text
z^mu(tau)
```

where `tau` is its proper time.

Its four-velocity is:

```text
u^mu(tau) = dz^mu/dtau
```

with normalization:

```text
u^mu u_mu = -1
```

assuming metric signature `(-,+,+,+)`.

At each event on the worldline, the particle has an **instantaneous rest frame**. This
is the local inertial frame whose time axis is `u^mu(tau)`. The spatial axes span the
3D subspace orthogonal to `u^mu`:

```text
v^mu u_mu = 0
```

So at each `tau`, you have a local frame:

```text
e_0^mu(tau) = u^mu(tau)
e_i^mu(tau),   i = 1,2,3
```

where the `e_i^mu` are spacelike unit vectors orthogonal to `u^mu`.

The question is then: how do you relate the frame at `tau` to the frame at
`tau + dtau`?

The physically natural answer is **Fermi-Walker transport**. It transports the spatial
axes along the accelerated worldline in a way that introduces no artificial rotation.
For a vector `V^mu` transported along the worldline:

```text
dV^mu/dtau = (u^mu a_nu - a^mu u_nu) V^nu
```

where:

```text
a^mu = du^mu/dtau
```

is the four-acceleration.

For the spatial basis vectors `e_i^mu`, Fermi-Walker transport preserves:

```text
e_i . u = 0
e_i . e_j = delta_ij
```

and keeps the frame "nonrotating" according to the accelerated observer.

So the structure is:

```text
worldline z^mu(tau)
      ↓
instantaneous rest frame at each tau
      ↓
Fermi-Walker transport relates neighboring frames
      ↓
proper time tau labels the sequence of comoving frames
```

If you want coordinates around the worldline, this leads to **Fermi normal
coordinates**. Near the particle's trajectory, an event is described by:

```text
(tau, X^i)
```

where:

- `tau` labels the event on the particle's worldline;
- `X^i` are spatial coordinates along geodesics orthogonal to the worldline at that
  `tau`;
- the hypersurface `tau = constant` is the local rest-space slice of the accelerated
  observer.

Important caveat:

These comoving rest frames are generally only **local**. For arbitrary acceleration,
the `tau = constant` hypersurfaces can fail to remain globally well behaved: they can
intersect, develop coordinate horizons, or stop covering all of spacetime. But locally
near the worldline, they are well defined.

Concise formulation:

> A particle undergoing arbitrary acceleration defines a one-parameter family of
> instantaneous rest frames along its worldline. The time axis of each frame is the
> particle's four-velocity, the spatial axes lie in the orthogonal rest space, and
> neighboring frames are naturally related by Fermi-Walker transport along the
> particle's proper time. Locally, this construction gives Fermi normal coordinates
> around the accelerated trajectory.

### Prompt

Dcuring my dissertation work I spend much time attempting to make something out of
the comoving tetrad along arbitrary accelerated worldlines in otherwise flat
spacetimes.

### Response

That tracks directly with the geometry you are circling here.

In flat spacetime, an arbitrarily accelerated worldline gives a very clean local
structure:

```text
z^mu(tau), u^mu(tau), a^mu(tau), e_a^mu(tau)
```

with the tetrad `e_a^mu(tau)` riding along the curve. If the tetrad is
Fermi-Walker transported, it is the natural nonrotating comoving frame.

The seductive thing is that it feels like it ought to define a full observer-adapted
dynamics:

```text
proper time tau
instantaneous rest space orthogonal to u^mu(tau)
local simultaneity slices
fields/states decomposed on those slices
```

But the hard part is exactly what you were likely fighting: the construction is
beautifully local and awkward globally.

For arbitrary acceleration, the instantaneous rest spaces:

```text
Sigma_tau = { events orthogonal to u^mu(tau) at z(tau) }
```

can intersect. The associated Fermi normal coordinates are valid only inside a
tubular neighborhood of the worldline. The admissible radius is limited by
acceleration scales and by where the orthogonal geodesics begin to cross. For uniform
acceleration, this turns into the familiar Rindler horizon structure; for arbitrary
acceleration, the geometry is less tidy.

So you get:

- a clean proper-time parameter `tau`;
- a clean local tetrad;
- a clean notion of local rest space;
- a clean expansion of the metric in Fermi normal coordinates;
- but no guaranteed global foliation of Minkowski spacetime.

That connects to the Tomonaga-Schwinger discussion in an interesting way. TS wants
arbitrary spacelike Cauchy hypersurfaces, but they need to be good leaves of a
foliation if you want global evolution. The comoving tetrad naturally gives
instantaneous local rest spaces, but those rest spaces are not generally a global
foliation.

Conceptual bridge:

> An accelerated observer's comoving tetrad gives a natural local sequence of rest
> frames, but not necessarily a global foliation. Tomonaga-Schwinger evolution can be
> formulated on arbitrary spacelike hypersurfaces, but the surfaces must fit together
> without intersection if they are to define a foliation. The obstruction in the
> accelerated-worldline case is geometric rather than quantum: local simultaneity
> planes need not assemble into a global slicing.

This may be useful for the talk, especially if someone asks whether "arbitrary
spacelike hypersurface" means "any observer's notion of simultaneity." The answer is:
locally yes, globally only if the surfaces form a valid foliation.

---

## 12. Spacetime Frenet-Serret Equations

### Prompt

I derived the spacetime versions of the Serret-Frenet equations and was fascinated by
the idea of using the Lorentz invariant scalar quantities of acceleration, torsion,
and hypertorsion as a function of metric arc length (or other arbitrary parameter
with a nonzero derivative with respect to arc length, a smooth function of the arc
length along the world line)

### Response

That is a very natural line of attack, and it sits right at the intersection of
differential geometry and relativistic observer theory.

For a timelike worldline in flat spacetime, the spacetime Frenet-Serret frame gives a
canonical moving tetrad when the curve is sufficiently regular. You start with the
unit tangent:

```text
e_0 = u = dz/ds
```

where `s` is proper time / metric arc length, then define successive orthonormal
directions from derivatives of the curve. The invariant scalars are the curvatures of
the worldline:

```text
kappa      = proper acceleration magnitude
tau_1      = torsion
tau_2      = hypertorsion
```

depending on notation.

The Frenet-Serret equations in Minkowski signature usually take a form like:

```text
de_0/ds = kappa e_1
de_1/ds = kappa e_0 + tau_1 e_2
de_2/ds = -tau_1 e_1 + tau_2 e_3
de_3/ds = -tau_2 e_2
```

up to sign conventions.

The attraction is clear: these scalars are Lorentz invariant. They characterize the
local geometry of the worldline independent of coordinates. In flat spacetime, they
are the worldline analog of curvature and torsion for a space curve, but now tied to
physical acceleration and rotation properties of the observer's frame.

Useful interpretations:

- `kappa` / acceleration: how strongly the worldline departs from inertial motion.
- `tau_1` / torsion: how the acceleration direction rotates relative to the
  osculating plane.
- `tau_2` / hypertorsion: how the curve twists out of the next-order hyperplane in
  spacetime.
- Constant invariants classify stationary worldlines in Minkowski spacetime. Uniform
  acceleration is one special case; circular motion and helical motions are others.

Using an arbitrary parameter `lambda` rather than proper time is fine if:

```text
ds/dlambda != 0
```

smoothly along the curve. Then the invariants themselves are still most cleanly
defined with respect to proper time `s`, while as functions they can be composed with
`s(lambda)`:

```text
kappa(lambda) = kappa(s(lambda))
tau_1(lambda) = tau_1(s(lambda))
tau_2(lambda) = tau_2(s(lambda))
```

If you write the differential equations directly in `lambda`, the coefficients pick
up factors of:

```text
ds/dlambda
```

For example:

```text
de_0/dlambda = (ds/dlambda) kappa e_1
```

and similarly for the torsion terms.

The bridge to the current Tomonaga-Schwinger thinking:

> A Frenet-Serret tetrad gives a canonical local frame along a worldline, determined
> entirely by Lorentz-invariant data of the curve. But turning that local moving frame
> into a family of global spacelike hypersurfaces is an additional, nontrivial
> foliation problem.

That distinction is exactly the central one: local covariant structure versus global
foliation/integrability.

The FS invariants give a local intrinsic description of an observer's motion. They do
not by themselves guarantee that the observer's instantaneous rest spaces assemble
into a nonintersecting global foliation. That step requires control over the normal
congruence, caustics, and how simultaneity planes evolve.

In the language of the old work:

> The accelerated worldline has an intrinsic invariant signature `kappa(s), tau_1(s),
> tau_2(s)`. That signature determines a canonical moving tetrad, but not
> automatically a globally valid simultaneity slicing. The obstruction is not Lorentz
> covariance; the FS construction is fully Lorentz covariant. The obstruction is
> foliation geometry.

---

## 13. Local Tomonaga-Schwinger States on Comoving Tetrad Slices

### Prompt

If the state were defined only locally around the classical trajectory, then could we
not use the comoving tetrad as a parameterized repretations of the hypersurfaces of
the Tomonaga-Schwinger state?

### Response

Yes, locally you can do something very close to that.

If you restrict attention to a tubular neighborhood around an accelerated classical
worldline, the comoving tetrad can define a local family of spacelike slices, and you
can use those slices as the hypersurfaces `Sigma_tau` on which a Tomonaga-Schwinger
state is represented.

The construction would be:

```text
z^mu(tau)          classical worldline
u^mu(tau)          four-velocity
e_i^mu(tau)        comoving spatial tetrad vectors
Sigma_tau          local rest-space slice at proper time tau
|Psi[Sigma_tau]>   field state represented on that local slice
```

At each proper time `tau`, the spatial tetrad vectors span the local rest space:

```text
v . u(tau) = 0
```

Then nearby spacetime points can be coordinatized as:

```text
x^mu(tau, X^i) = z^mu(tau) + X^i e_i^mu(tau)
```

in flat spacetime, at least locally. This is essentially the Fermi-normal-coordinate
construction, or a related accelerated tetrad coordinate system if the tetrad is not
Fermi-Walker transported.

So in a local region, yes:

> the comoving tetrad gives a parameterized representation of spacelike hypersurface
> patches, and the Tomonaga-Schwinger state could be represented as
> `|Psi[Sigma_tau]>` on those patches.

But the limitations are important.

First, these are generally **local hypersurface patches**, not guaranteed global Cauchy
surfaces. For arbitrary acceleration, the instantaneous rest spaces may intersect if
extended too far. So they may not define a global foliation of all Minkowski
spacetime.

Second, a Tomonaga-Schwinger state is normally defined on a complete spacelike Cauchy
surface. If you define it only in a local tube around the trajectory, you are really
working with a local algebra of observables or a restricted subsystem, not the full
global field state.

Third, the tetrad gives you a family of surfaces, but TS covariance still requires
that physics not depend on choosing that family rather than another. The comoving
tetrad is a convenient observer-adapted representation, not extra physical structure
unless the theory makes it so.

Clean formulation:

> In a tubular neighborhood of an accelerated worldline, a comoving tetrad can define
> a local foliation by instantaneous rest-space slices. One may represent the
> Tomonaga-Schwinger state locally on these slices, using the particle's proper time
> as the foliation parameter. This is a valid observer-adapted representation locally,
> but it does not generally extend to a global foliation, and it should not introduce
> physical dependence on that chosen slicing.

Bridge to Hsu:

- Ordinary TS theory says different foliations should be equivalent.
- The comoving tetrad gives a particular local foliation tied to an accelerated
  observer.
- If a nonlinear state-dependent theory made predictions depend on that tetrad
  foliation, that would be a real physical preferred-slicing effect.

---

## 14. Extending Comoving Tetrad Data to Full Cauchy Foliations

### Prompt

Could we not, using the comoving tetrad frames as starting point, construct arbitrary
extended Cauchy hypersurfaces filling any desired region of spacetime in a way that
preserves proper foliation?

### Response

Yes, often you can. But the important distinction is:

> The comoving tetrad gives you canonical local data along the worldline; extending
> that data into full Cauchy hypersurfaces is an additional choice, not uniquely
> determined by the tetrad.

A reasonable construction is:

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

This gives a local spacelike patch orthogonal to the worldline.

4. Then extend that patch outward into a complete spacelike Cauchy hypersurface:

```text
Sigma_tau
```

5. Choose the extensions smoothly in `tau`, avoiding intersections between leaves.

If this succeeds, you get a proper foliation:

```text
{Sigma_tau}
```

with each leaf anchored to the particle's instantaneous rest frame along the
worldline.

The caveat is that the extension is not automatic. The local orthogonal rest planes
can intersect if extended naively. For arbitrary acceleration, the Fermi-normal
construction has a finite radius of validity. Beyond that tube, you need to "bend" or
"cap off" the hypersurfaces so that they remain spacelike, nonintersecting, and
Cauchy.

So:

> Yes, using the comoving tetrad as boundary/local anchor data, one can often
> construct extended spacelike Cauchy hypersurfaces that fill a desired globally
> hyperbolic region. But the construction requires extra choices away from the
> worldline, and it is constrained by avoiding intersections, caustics, horizons, and
> loss of spacelikeness.

In flat Minkowski spacetime, this is usually flexible. You can often build a smooth
time function `T(x)` such that:

```text
T(z(tau)) = tau
```

and near the worldline its level surfaces have normal aligned with the particle's
four-velocity:

```text
grad_mu T |_{z(tau)} proportional to u_mu(tau)
```

Then the hypersurfaces:

```text
Sigma_tau = { x : T(x) = tau }
```

form the desired foliation, at least over the region where `T` is smooth and has
timelike gradient.

That last condition is the key:

```text
grad_mu T is timelike
```

If the gradient of `T` is timelike, then the level sets `T = constant` are spacelike.
If `T` is also globally well behaved, the leaves do not intersect and can be Cauchy
surfaces.

Precise version:

> Use the comoving tetrad to specify local conditions on a time function near the
> worldline, then extend that time function smoothly to the desired spacetime region
> with timelike gradient everywhere. Its level sets give the extended foliation.

This also gives a clean connection to Tomonaga-Schwinger:

```text
|Psi[Sigma_tau]>
```

where `Sigma_tau` is an observer-adapted Cauchy surface anchored to the accelerated
particle's comoving frame.

But again: the tetrad does not uniquely determine `Sigma_tau` away from the
worldline. It supplies local anchoring data; the global foliation is a chosen
extension.

---

## 15. Returning to Foliation-Preserving Invariance and Path Independence

### Prompt

Yes our dynamics would have to arbitrary in regard to the foliation-preserving
transformations of the extended Cauch manifold, for the physics to be meaningful?

### Response

Yes. That is exactly the right requirement.

If the extended Cauchy hypersurfaces are partly a **choice of representation**, then
the physics must be invariant under transformations that preserve the foliation
structure or, more strongly, under changes of foliation itself.

There are two related invariance requirements.

**1. Foliation-preserving transformations**

Suppose you have built a foliation:

```text
Sigma_tau
```

anchored to the comoving tetrad along the worldline.

Then you can change coordinates within that foliated spacetime without changing the
leaves as physical slices. These are foliation-preserving transformations, roughly:

```text
tau' = f(tau)
X'^i = X'^i(tau, X^j)
```

They relabel the same foliation or move coordinates around within each leaf.

Physics should be invariant under these. Otherwise your predictions would depend on
arbitrary coordinates on the same hypersurfaces.

**2. Foliation-choice independence**

More strongly, the extension from the local comoving tetrad patch to a full Cauchy
hypersurface is not unique. You can choose different global extensions:

```text
Sigma_tau
Sigma_tilde_tau
```

that agree near the worldline but differ far away, or even different foliations
connecting the same initial/final surfaces.

If the extra choice is not physical, then observables localized near the trajectory
should not depend on it.

That is exactly the Tomonaga-Schwinger lesson:

> A meaningful covariant dynamics should not depend on arbitrary choices of spacelike
> slicing.

So for this construction:

> The comoving tetrad may provide physical local observer data along the classical
> trajectory. But the extended Cauchy surfaces away from the trajectory are auxiliary
> structure. The dynamics must be invariant under transformations that preserve the
> foliation description, and ideally independent of the arbitrary extension of the
> foliation away from the local region of interest.

The mathematical condition is again an integrability/path-independence condition:

```text
[delta/delta sigma(x), delta/delta sigma(y)] |Psi[Sigma]> = 0
```

for spacelike-separated local deformations.

If this holds, then changing the foliation away from the worldline does not change
the final physical state, except by the expected unitary equivalence.

If it fails, then the theory has introduced a preferred slicing or a dependence on
the arbitrary extension of the comoving frame. That would make the physics suspect
unless the foliation itself is promoted to a real physical structure.

Clean formulation:

> If the Cauchy foliation is auxiliary, the dynamics must be invariant under
> foliation-preserving coordinate transformations and independent of arbitrary
> foliation extensions. Otherwise the theory's predictions depend on representational
> choices rather than physical data.

---

## 16. User Personal Framing for Section 6 / Possible Paper Thread

### Prompt

super I need in particular to make sure the prompts and responses are preserved
explicitly for this. The conversation we just had will be my personal contribution to
Section 6 of the talk. I have the feeling an original paper idea could come forth from
this, if I pushed it. My experience is the Serret-Frenet equations are greatly
overlooked. Most of my involved involved the "forgotten" issues of accelerated
relativistic motion in particle electrodynamics. I did not even known anyone had
dervied them before and could find no prior so I put them into an appendix in my
disseration and my book with W.C Schieve (Kluwer, 1997). I was certain something
could be done with them, they are so beautiful as descriptions of arbitrary accelerated
world lines. Of course that guarantees nothing, the beauty. Still it has been like a
siren song to me, to return to a another pass at using them.

### Preserved Notes

This final prompt frames the previous discussion as the user's intended personal
contribution to section 6.

Key preserved personal claims:

- The user worked extensively during dissertation research on comoving tetrads along
  arbitrarily accelerated worldlines in otherwise flat spacetimes.
- The user derived spacetime Serret-Frenet equations independently and found little or
  no prior derivation at the time.
- The equations were included in an appendix to the user's dissertation and in the
  user's book with W.C. Schieve, published by Kluwer in 1997.
- The motivating physics context was the overlooked or "forgotten" issues of
  accelerated relativistic motion in particle electrodynamics.
- The user's renewed interest is that the Lorentz-invariant scalars of acceleration,
  torsion, and hypertorsion provide beautiful intrinsic descriptions of arbitrary
  accelerated worldlines.
- The user suspects that, despite beauty not guaranteeing physical significance, this
  may still contain the seed of an original paper idea when connected to local
  foliations, Tomonaga-Schwinger hypersurface dynamics, and path-independence.

Possible paper seed, stated cautiously:

> Use the Lorentz-invariant Frenet-Serret data of an arbitrarily accelerated classical
> worldline to define local observer-adapted tetrad/hypersurface data, then analyze
> the conditions under which these local data can be extended to auxiliary Cauchy
> foliations whose associated Tomonaga-Schwinger dynamics is invariant under
> foliation-preserving transformations and independent of arbitrary extension choices.

Possible section 6 speaker formulation:

> My own way into this question comes from older work on arbitrarily accelerated
> worldlines. In my dissertation, and later in my 1997 book with W.C. Schieve, I
> worked out spacetime Serret-Frenet equations for accelerated relativistic motion:
> acceleration, torsion, and hypertorsion as Lorentz-invariant functions along a
> worldline. Those equations always seemed to me like a beautiful but underused
> language for observer-adapted dynamics. What the Tomonaga-Schwinger discussion
> clarifies is the missing distinction: the comoving tetrad gives canonical local
> observer data, but turning it into a physical evolution requires invariance under
> arbitrary Cauchy-surface extensions and path independence of the resulting
> hypersurface dynamics.

---

## Compact Summary of the Whole Thread

> A continuous Tomonaga-Schwinger foliation is a smooth family of nonintersecting
> spacelike Cauchy hypersurfaces whose local normal displacements define spacetime
> slabs. Leaves within a foliation cannot intersect, but different foliations of the
> same physical system may cross. An arbitrarily accelerated classical worldline
> supplies a natural local comoving tetrad, and the Lorentz-invariant Frenet-Serret
> scalars give an intrinsic description of that local observer frame. This tetrad can
> define local hypersurface patches around the worldline and can often be used as
> anchoring data for extended Cauchy hypersurfaces. But the extension away from the
> worldline is not unique. Therefore, if the foliation is auxiliary, meaningful physics
> requires invariance under foliation-preserving transformations and independence from
> arbitrary foliation extensions. In Tomonaga-Schwinger language, this returns to the
> integrability/path-independence condition.

## Final Clean Formulation

> If the Cauchy foliation is auxiliary, the dynamics must be invariant under
> foliation-preserving coordinate transformations and independent of arbitrary
> foliation extensions. Otherwise the theory's predictions depend on representational
> choices rather than physical data.
