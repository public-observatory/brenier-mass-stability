# Proposed issues — unpublished

These drafts use the inherited Problem form: a title, Statement, Why it matters, and Further details. All three have label `question`. The letters are local draft identifiers, not GitHub issue numbers. They propose work; no question is marked answered.

Throughout, the source ρ is uniform probability on the square K := [−1,1]². Targets lie in K. Write Tμ for the quadratic optimal map from ρ to μ, E(μ,ν) := ‖Tμ − Tν‖L²(ρ), and W₂ for the 2-Wasserstein distance. For 0 < m < 1/3, let A₃(m) consist of probability measures with exactly three distinct atoms, each of mass at least m. The root question is whether E(μ,ν) ≤ C(m) W₂(μ,ν)^(1/2) holds for every μ,ν in A₃(m). The two mass vectors may differ. No matching of atom labels is assumed.

## Draft A: Separate the mass and displacement in the three-atom example

### Statement

What exact map-error and target-distance formulas hold when the central mass and tilt in OpenAI’s three-atom example vary independently, and what lower bound do they impose on C(m)?

### Why it matters

The paper ties the tilt to the disappearing mass. Separating them distinguishes instability at a fixed mass from deterioration as that mass tends to zero, giving the other problems an exact benchmark.

### Further details

Use OpenAI §2, Proposition 2.2, equations (2.1)–(2.5), and Figure 1. Set u(x) := max{−x₁,x₁,a} and v(x) := max{−x₁,x₁,a+b x₂}, with 0 < a < 1/2 and 0 < b ≤ a/2. Let μ and ν be the laws of their gradients under ρ. The coordinate vectors are e₁ := (1,0) and e₂ := (0,1).

Independently derive the predicted laws μ = ((1−a)/2)(δ₋ₑ₁+δₑ₁)+aδ₀ and ν = ((1−a)/2)(δ₋ₑ₁+δₑ₁)+aδᵦₑ₂. Check the formulas W₂² = ab² and E² = b/2+ab². Prove optimality of the gradients using the convex supporting inequality, and prove optimality of the target coupling using the second-coordinate lower bound. A plot alone is insufficient.

The proposed consequence to check is E/W₂^(1/2) = a^(−1/4)√(1/2+ab). Taking a = m < 1/3 gives the necessary order C(m) ≳ m^(−1/4). This is a lower bound from one family, not a proof that this rate suffices for all targets. At fixed a, b → 0 also rules out an exponent greater than 1/2 for this class.

Deliver a short derivation and, optionally, a polygon-integration check. Integrate intersections of the two cell partitions; a source grid can miss the thin regions that switch depots. Record discrepancies with their parameter values. This task is independent of the full uniform upper-bound proof in OpenAI §§3–6.

## Draft B: Prove a square-root bound for separated sites

### Statement

For μ,ν in A₃(m) whose within-target pairwise site distances are at least s > 0, is E(μ,ν) ≤ C(m,s) W₂(μ,ν)^(1/2) uniformly valid without an angle bound?

### Why it matters

This isolates changes of cell boundaries from collisions. An explicit separated-site estimate would identify precisely what must be controlled to answer the root question.

### Further details

Fix m and s; allow different masses and site locations in the two targets. Collinear triples are included. OpenAI §3 gives face-integral formulas for mass and moment variations and the weighted graph Laplacian of the cells. Divol–Niles-Weed–Pooladian, Proposition 4.1 and Theorem 4.3, provide a cube-root comparison with additional geometric dependence, not the square-root conclusion requested here.

Begin near one fixed separated configuration. Use W₂-smallness and the mass floor to justify a local correspondence between nearby sites, rather than assuming that an optimal coupling preserves labels. Estimate cell reassignment and account for mass changes. Then determine whether local constants can be made uniform across separated configurations, including collinear limits and changes in which cells share an edge.

Do not infer a mass floor for individual entries of a target coupling from a mass floor for its marginals: splitting can produce arbitrarily small entries. If the argument needs an angle or cell-interface hypothesis, state the restricted theorem and exhibit the step that requires it. Such a result is useful partial progress, but does not close this question.

Success is a proof with explicit parameter dependence, or a family violating the bound at fixed m and s. For a numerical candidate, provide sites, masses, optimal-transport certificates or error bounds, and a sequence tending to the claimed singular limit. Draft A supplies a check on the required dependence on m.

## Draft C: Decide whether a mass floor alone is sufficient

### Statement

Does a finite C(m) give E(μ,ν) ≤ C(m) W₂(μ,ν)^(1/2) for all μ,ν in A₃(m), with no minimum site separation?

### Why it matters

This is the root question: it decides whether a depot serving very little mass is essential to losing square-root stability, or whether nearly coincident sites provide another mechanism.

### Further details

Use Draft B if available, but a counterexample can be sought independently. Analyze sequences in which two sites merge or all three approach one another, allowing independent mass changes. Every member of a proposed sequence must still have three distinct atoms and the same fixed mass floor m. Distances between sites can tend to zero; target support and source remain fixed.

A possible proof strategy groups nearly coincident atoms, estimates the coarser assignment, then bounds the cost of resolving each group. Track both the mass reassigned and the distance between assigned sites: a large change in a cell label need not mean a large map error when its sites are close. Continuity and compactness alone yield no specified Hölder exponent.

A proof should track C(m) sufficiently to compare with Draft A’s proposed m^(−1/4) lower bound; matching that dependence is a further goal, not required to settle existence. A negative answer requires E/W₂^(1/2) → ∞ at one fixed m > 0, not merely as m → 0. Finite numerical ratios are exploratory evidence only. Record a precise obstruction even if it leaves the best replacement exponent unresolved.
