# State-Dependent Hamiltonian Nonlinearities

In this discussion, the nonlinearities are mainly of the form:

```text
i hbar d|Psi>/dt = H[Psi] |Psi>
```

or, in Tomonaga-Schwinger form:

```text
i hbar delta_x |Psi> = (H(x) + N_x[Psi]) |Psi>
```

The equation is nonlinear because the generator of evolution depends on the state
being evolved. If `N_x[Psi]` depends on quantities like

```text
<Psi|O(x)|Psi>
```

then the right-hand side is no longer a fixed linear operator acting on `|Psi>`.
The operator changes when `|Psi>` changes.

So the nonlinearities under discussion are nonlinearities arising from
state-dependent Hamiltonian operators.

This is a special class of nonlinear quantum dynamics, not the most general
imaginable kind.

A broader nonlinear Schrodinger equation could include many other forms, for
example:

```text
i dPsi/dt = H Psi + lambda |Psi(x)|^2 Psi(x)
```

or nonlinear dependence on density matrices, histories, stochastic variables,
collapse fields, hidden variables, gravitational self-fields, and other
structures. Some nonlinear theories may be deterministic, some stochastic; some
norm-preserving, some not; some local, some explicitly nonlocal; some formulated
at the wavefunction level, some at the density-matrix level.

The Weinberg/Hsu/Kaplan-Rajendran class has a more specific structure:

```text
state-dependent generator
deterministic evolution
usually norm-preserving
often Hamiltonian-like
designed to reduce to ordinary QM when nonlinear terms vanish
```

That class is natural because it preserves much of the ordinary Schrodinger form.
But it is also exactly why the pathology appears: once the generator depends on
the global state, entangled or spatially separated parts of the state can
influence the local generator.

Slide wording:

> The nonlinearities under discussion are not arbitrary nonlinear equations. They
> are state-dependent Hamiltonian nonlinearities: the evolution remains
> Schrodinger-like, but the Hamiltonian density is allowed to depend on the
> quantum state itself, often through expectation values. This is a controlled but
> still dangerous subclass of nonlinear quantum mechanics.

