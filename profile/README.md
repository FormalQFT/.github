# FormalQFT

Formalization of Quantum Field Theory in [Lean 4](https://lean-lang.org/) with [Mathlib](https://github.com/leanprover-community/mathlib4).

## Projects

### [OSforGFF](https://github.com/FormalQFT/OSforGFF)

Formalization of the Osterwalder-Schrader axioms for the Gaussian free field in d=4. Proves that the lattice-regularized GFF satisfies reflection positivity, Euclidean invariance, and the other OS axioms, providing a rigorous non-perturbative construction of the free scalar field as a Euclidean QFT.

### [GFF4D](https://github.com/FormalQFT/GFF4D)

Lean 4 formalization of the Gaussian free field in four dimensions. The `main` branch constructs the GFF as a Gaussian measure on distributions and establishes its basic properties. The `bochner` branch develops an alternative construction via Bochner's theorem and characteristic functionals.

### [pphi2](https://github.com/FormalQFT/pphi2)

Construction of the P(phi)_2 quantum field theory in Lean 4 — an interacting scalar field in two spacetime dimensions. This is a key test case for rigorous QFT, following the constructive approach of Glimm-Jaffe and Simon where non-Gaussian measures are built via exponential tilting of the free field.

### [gaussian-field](https://github.com/FormalQFT/gaussian-field)

A general-purpose Lean 4 library for constructing centered Gaussian probability measures on duals of nuclear Frechet spaces. Given a nuclear Frechet space E and a continuous linear map T : E -> H into a separable Hilbert space, constructs the measure on the weak dual E' with characteristic functional exp(-||T(f)||^2/2). Application-agnostic foundation for the GFF, stochastic PDEs, and infinite-dimensional probability.

### [bochner](https://github.com/FormalQFT/bochner)

Formal proofs of Bochner's theorem and Minlos' theorem in Lean 4 — the two foundational results characterizing when a function(al) is the Fourier transform of a probability measure. Bochner's theorem (finite-dimensional, fully proved with 0 sorries) uses Gaussian regularization and Prokhorov's theorem. Minlos' theorem extends this to nuclear spaces, providing the key tool for constructing measures on infinite-dimensional spaces.

### [stochasticpde-itocalculus](https://github.com/FormalQFT/stochasticpde-itocalculus)

Complete, sorry-free formalization of the Ito formula in Lean 4 (~24k lines). Builds stochastic integrals as L^2 limits of simple process integrals, proves the Ito isometry, Kolmogorov-Chentsov continuous modification theorem, quadratic variation convergence, and the full Ito formula: the remainder M_t = f(t,X_t) - f(0,X_0) - integral of the Ito drift is a martingale.
