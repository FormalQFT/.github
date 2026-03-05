# FormalQFT

Formalization of Quantum Field Theory in [Lean 4](https://lean-lang.org/) with [Mathlib](https://github.com/leanprover-community/mathlib4).

## Projects

### [OSreconstruction](https://github.com/FormalQFT/OSreconstruction)

Formalization of the Osterwalder-Schrader reconstruction theorem — the mathematical bridge between Euclidean and relativistic QFT. Includes supporting infrastructure in von Neumann algebra theory (Tomita-Takesaki modular theory, KMS condition, Stone's theorem), several complex variables (tube domains, Hartogs' theorem, Bochner tube theorem, edge-of-the-wedge), complex Lie groups (Bargmann-Hall-Wightman theorem), and the full Wightman axioms with GNS construction and analytic continuation.

### [Phi4](https://github.com/FormalQFT/Phi4)

Formal construction of the phi^4_2 Euclidean quantum field theory in Lean 4 (0 sorries, 0 axioms). Follows the Glimm-Jaffe program: finite-volume construction with Nelson-Symanzik estimates, infinite-volume limit, verification of the Osterwalder-Schrader axioms (with explicit weak-coupling handling for OS4), and reconstruction of the corresponding Wightman theory. Includes formalized Feynman graph combinatorics, Bessel function estimates, and Green function infrastructure.

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

## Future Projects

- **FormalQFT meta-repo** — A unified Lean package that combines all QFT repositories into a single importable library. Will verify cross-repo compatibility and provide a one-line `require FormalQFT` for downstream users.

- **Automated Lean/Mathlib updater** — Org-wide CI infrastructure to track stable Lean 4 releases, find matching Mathlib commits, and automatically create PRs updating each repository. Keeps the entire org on a consistent, tested toolchain.
