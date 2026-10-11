# When are optimal transport maps stable?

Imagine assigning a square of land to three delivery depots while minimizing squared travel distance and meeting each depot’s quota. Moving a depot slightly can change which depot serves a substantial patch of land. We ask whether requiring every depot to serve a minimum share prevents the worst instability.

The mathematical object is a **Brenier map**: the assignment minimizing average squared distance from a continuous source to a target distribution. Target changes are measured by the 2-Wasserstein distance, the least root-mean-square distance needed to move one target distribution into the other.

OpenAI’s *Sharp One-Third Stability of Brenier Maps* claims a uniform cube-root bound on map changes for uniform convex sources, and gives a three-depot example ruling out stronger uniform bounds.[^openai-2026] In that example, one depot’s mass vanishes. This challenges Letrouit’s earlier square-root conjecture without settling whether a minimum mass restores it.[^letrouit-2026] Earlier work gives cube-root bounds for finite targets with constants depending on masses and geometry.[^divol-2025] We treat the OpenAI manuscript as a research preprint; its full upper-bound proof has not been independently certified here.

**Root question:** For a uniform square source and targets with exactly three atoms in that square, does a fixed positive lower bound on every atom’s mass imply a uniform square-root stability bound, without separation or angle assumptions?

The following are our proposed extensions, not questions stated by OpenAI:

- **[Separate mass from motion.](https://github.com/public-observatory/brenier-mass-stability/issues/1)** Reproduce the paper’s example, varying the middle depot’s mass and displacement independently. This supplies an exact benchmark and a necessary growth rate for any mass-dependent constant.
- **[Control separated depots.](https://github.com/public-observatory/brenier-mass-stability/issues/2)** First seek a square-root estimate with a fixed minimum distance between depots. Track which constants deteriorate as that distance shrinks.
- **[Allow collisions.](https://github.com/public-observatory/brenier-mass-stability/issues/3)** Remove the separation assumption, or construct an explicit counterexample with all three masses bounded below. Either outcome settles the root question.

Start with the [three open questions](https://github.com/public-observatory/brenier-mass-stability/issues?q=is%3Aissue%20is%3Aopen%20label%3Aquestion); [reading notes](writeups/literature.md) record scope and recent checks. Follow the shared [contribution guide](https://public-observatory.github.io/docs.html).

[^openai-2026]: OpenAI, *Sharp One-Third Stability of Brenier Maps* (2026), OpenAI Math Release preprint, September 25; §2, Proposition 2.2 and Figure 1; §§4–6. [Pinned manuscript](https://github.com/openai/math/blob/fd4aeeb2ee4fc729c18d98444fed42fd0529eeeb/preprints/Sharp-One-Third-Stability-of-Brenier-Maps-September-25-2026/article.pdf).
[^letrouit-2026]: Cyril Letrouit, *Unstable optimal transport maps* (2026), **Comptes Rendus. Mathématique** 364, 333–344; Theorem 2 and Conjecture 3. [Paper](https://doi.org/10.5802/crmath.834).
[^divol-2025]: Vincent Divol, Jonathan Niles-Weed and Aram-Alexandre Pooladian, *Tight stability bounds for entropic Brenier maps* (2025), **IMRN**, rnaf078; [author preprint](https://arxiv.org/abs/2404.02855v1), Proposition 4.1, Theorem 4.3 and Remark 4.4.
