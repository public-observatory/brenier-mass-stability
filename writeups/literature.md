# Reading notes and scope

Reviewed on October 10, 2026. This is a brief literature review, not a claim of exhaustive coverage or novelty. The root question is proposed here. It is not an explicit open problem from the selected OpenAI paper.

## Selected paper

OpenAI, *Sharp One-Third Stability of Brenier Maps*, September 25, 2026, OpenAI Math Release preprint, result family 374. [Pinned full text](https://github.com/openai/math/blob/fd4aeeb2ee4fc729c18d98444fed42fd0529eeeb/preprints/Sharp-One-Third-Stability-of-Brenier-Maps-September-25-2026/article.pdf). Read all six sections and references (18 pages), including Figure 1 on page 5. There are no appendices.

Theorem 1.1 claims a target-uniform W₂^(1/3) upper bound for a uniform probability source on any compact convex body with interior in dimension at least two. Its constant may depend on that body and a fixed compact target container, but not on atom count, masses or separation. Proposition 2.2 gives a three-atom example on a fixed cube with a vanishing central mass. Its proof computes target distances and source-cell reassignment explicitly.

The upper-bound argument passes from prescribed cell masses (§3), through a uniform moment inequality (§4) and a Lipschitz estimate for potentials (§5), to gradient interpolation and finite-target approximation (§6). Reading this argument is not independent certification of its correctness. The agenda can begin from §2 without assuming all these steps. No Lean verification was run and no formal-verification claim is made.

The example moves the central site by a/2 while its mass is a. Its other sites stay separated from it. Thus fixed atom count and site separation do not by themselves remove the example; a mass floor is a meaningful additional condition. It does not establish that the mass floor alone suffices. [Question 1](https://github.com/public-observatory/brenier-mass-stability/issues/1)’s independent-parameter calculation is our proposed extension of the paper’s calculation, not a claimed new theorem.

## Earlier literature

- Sivaraman Balakrishnan, Tudor Manole and Larry Wasserman, *Statistical Inference for Optimal Transport Maps: Recent Advances and Perspectives* (2025), survey preprint [arXiv:2506.19025v1](https://arxiv.org/abs/2506.19025v1), §4.2 and Theorem 3. Read for the role of stability in estimating maps. Its smooth, strongly convex potential assumptions differ from the piecewise-affine potentials used here.
- Cyril Letrouit, *Unstable optimal transport maps* (2026), **Comptes Rendus. Mathématique** 364, 333–344, [doi:10.5802/crmath.834](https://doi.org/10.5802/crmath.834), §§1.1–1.3, Theorem 2 and Conjecture 3. The published nonconvex-source obstruction and convex-source square-root conjecture provide context. The older conjecture is not presented as still intact after the selected preprint.
- Vincent Divol, Jonathan Niles-Weed and Aram-Alexandre Pooladian, *Tight stability bounds for entropic Brenier maps* (2025), **International Mathematics Research Notices**, rnaf078, [doi:10.1093/imrn/rnaf078](https://doi.org/10.1093/imrn/rnaf078). Inspected the [April 3, 2024 author preprint](https://arxiv.org/abs/2404.02855v1), §4, Proposition 4.1, Theorem 4.3 and Remark 4.4. Its unregularized cube-root bound has constants depending on minimum mass, site separation and angular geometry. The fixed-site total-variation comparison in Remark 4.4 does not directly control moving-site perturbations. Section numbers here refer to v1, not an unchecked publisher version.

## Recent checks

- Yuanlong Ruan, *Sharp conditioning and quantitative stability of optimal transport* (October 6, 2026), research preprint [arXiv:2610.07577v1](https://arxiv.org/abs/2610.07577v1), introduction and §12, especially Theorem 8. The compact-source/compact-target estimate is stated using W₁, with exponent 1/4 for bounded source densities. That statement does not imply the proposed mass-floor W₂ square-root bound.
- Songbo Wang and Xiaozhen Wang, *Quantitative stability of optimal transport via regularization* (October 7, 2026), research preprint [arXiv:2610.09640v1](https://arxiv.org/abs/2610.09640v1), §1, Theorem 1 and Proposition 4. Its W₂ bound gives exponent 1/4 for BV source densities and permits an unrestricted second target. The sharpness examples concern a broader source class than a fixed uniform square. These statements do not settle the finite-target mass-floor question.

Targeted searches for minimum-mass and moving-site square-root estimates did not identify a theorem resolving the exact class A₃(m). This is a provisional assessment: contributors should compare any proposed result with existing semi-discrete stability theorems before claiming novelty.
