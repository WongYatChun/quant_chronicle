---
title: "Robust Portfolio Optimization"
year: 2003
authors: "El Ghaoui, Oks, Oustry; Goldfarb, Iyengar"
track: "Portfolio Theory"
topic: "Estimation & Uncertainty"
summary: "Optimize against plausible errors in expected returns."
---

## Why?

$$
\mu\in\mathcal U
$$

A single estimated return vector understates uncertainty.

## Who?

El Ghaoui, Oks & Oustry (2003); Goldfarb & Iyengar (2003) — foundational robust portfolio formulations.

## How?

With fixed covariance:

$$
\boxed{
\max_{w\in\mathcal W}\min_{\mu\in\mathcal U}
\left(w^\top\mu-\frac\gamma2w^\top\Sigma w\right)
}.
$$

For $\mathcal U=\{\hat\mu+Au:\|u\|_2\le\rho\}$:

$$
\min_{\mu\in\mathcal U}w^\top\mu
=w^\top\hat\mu-\rho\|A^\top w\|_2.
$$

Thus:

$$
\boxed{
\max_{w\in\mathcal W}
w^\top\hat\mu-\frac\gamma2w^\top\Sigma w
-\rho\sqrt{w^\top AA^\top w}
}.
$$

## So what?

Uncertainty sets generate regularization:

$$
\|e\|_2\le\rho\ \Rightarrow\ \rho\|w\|_2,
\qquad
|e_i|\le d_i\ \Rightarrow\ \sum_i d_i|w_i|.
$$

$\Sigma$ describes return risk; $AA^\top$ describes forecast uncertainty.

**Limitation:** an oversized or misspecified set can suppress useful positions.

**Connection:** [Black–Litterman]({{ '/notes/1992-black-litterman/' | relative_url }}) instead combines a prior and probabilistic views.

## References

- Goldfarb & Iyengar (2003), *Robust Portfolio Selection*.
- El Ghaoui, Oks & Oustry (2003), *Worst-Case Value-at-Risk and Robust Portfolio Optimization: A Conic Programming Approach*.
