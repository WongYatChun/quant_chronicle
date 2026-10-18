---
title: "Estimation Risk & Regularization"
year: 1986
authors: "Bawa, Brown, Klein; Jorion; Ledoit, Wolf"
track: "Portfolio Theory"
topic: "Estimation & Uncertainty"
summary: "Stabilize forecasts, covariance estimates, and portfolio weights."
---

## Why?

$$
w^*=\frac1\gamma\Sigma^{-1}\mu_e
\quad\longrightarrow\quad
\hat w=\frac1\gamma\hat\Sigma^{-1}\hat\mu_e.
$$

Optimization can amplify sampling noise.

## Who?

Bawa, Brown & Klein (1979) — estimation risk; Jorion (1986) — Bayes–Stein portfolio estimation; Ledoit & Wolf (2004) — covariance shrinkage.

## How?

Shrink means and covariance toward structured targets:

$$
\tilde\mu=(1-\delta)\hat\mu+\delta\mu_0,
\qquad
\tilde\Sigma=(1-\alpha)\hat\Sigma+\alpha F.
$$

Regularize holdings directly:

$$
\boxed{
\max_{w\in\mathcal W}
w^\top\tilde\mu-\frac\gamma2w^\top\tilde\Sigma w
-\lambda_1\|w\|_1-\frac{\lambda_2}{2}\|w\|_2^2
}.
$$

For unconstrained weights and $\lambda_1=0$:

$$
w^*=(\gamma\tilde\Sigma+\lambda_2I)^{-1}\tilde\mu.
$$

Bounds $l\le w\le u$ also limit extreme allocations.

## So what?

For known $\Sigma$ and unconstrained MVO, $\hat\mu_e=\mu_e+\varepsilon$ implies:

$$
\boxed{
U(w^*)-U(\hat w)=
\frac1{2\gamma}\varepsilon^\top\Sigma^{-1}\varepsilon
}.
$$

Prediction errors matter in the geometry of portfolio risk.

For long-only, fully invested weights:

$$
\|w\|_1=\mathbf1^\top w=1.
$$

An L1 weight penalty is then constant; it does **not** induce sparsity.

**Next:** [Robust optimization]({{ '/notes/2003-robust-optimization/' | relative_url }}) derives penalties from forecast uncertainty sets.

## References

- Bawa, Brown & Klein (1979), *Estimation Risk and Optimal Portfolio Choice*.
- Jorion (1986), *Bayes–Stein Estimation for Portfolio Analysis*.
- Ledoit & Wolf (2004), *Honey, I Shrunk the Sample Covariance Matrix*.
