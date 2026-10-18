---
title: "Signal Weighting — Combine Information"
year: 2020
authors: "Richard Grinold; Ronald Kahn"
track: "Portfolio Theory"
topic: "Active Portfolio Management"
summary: "Combine signals using their joint contribution to portfolio returns."
---

## Why?

$$
K\text{ signals}\neq K\text{ independent sources of information}.
$$

A strong signal may add little when it duplicates existing forecasts.

## Who?

Grinold & Kahn — *Advances*, chapter 9, “Signal Weighting.”

## How?

An illustrative static formulation: let columns of $S\in\mathbb R^{N\times K}$ be tradable signal portfolios.

$$
a=S\beta,\qquad
m=S^\top\alpha,\qquad Q=S^\top\Sigma S.
$$

Then:

$$
\max_\beta\quad
\beta^\top m-\frac\gamma2\beta^\top Q\beta.
$$

For $Q\succ0$ and unconstrained coefficients:

$$
\boxed{\beta^*=\frac1\gamma Q^{-1}m}.
$$

With ridge regularization:

$$
\beta_\lambda=(\gamma Q+\lambda I)^{-1}m.
$$

## So what?

$$
\text{Signal weight depends on incremental value, not standalone IC alone}.
$$

This formulation combines portfolios; combining raw forecasts requires their calibration and error dependence instead.

Different decay rates and trading costs require a dynamic extension. The equations above illustrate the principle rather than reproduce the chapter's full model.

**Next:** [Implementation and trading rules]({{ '/notes/2020-active-trading-rules/' | relative_url }}).

## References

Grinold & Kahn, *Advances in Active Portfolio Management* (published 2019; copyright 2020). Selected chapters discussed above. This is a thematic synthesis, not a claim that these ideas originated in 2020.
