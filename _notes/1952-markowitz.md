---
title: "Markowitz — Mean–Variance Optimization"
year: 1952
authors: "Harry Markowitz"
track: "Portfolio Theory"
summary: "Diversification becomes a problem of portfolio covariance."
---

## Why?

Choosing attractive securities individually does not determine how to combine them. Their joint behavior matters.

## Who?

Harry Markowitz, *Portfolio Selection* (1952).

## How?

A modern utility formulation of the mean–variance framework is:

$$
\max_w\quad w^\top\mu-\frac{\gamma}{2}w^\top\Sigma w,
\qquad \mathbf1^\top w=1.
$$

Here $\mu$ contains expected returns, $\Sigma$ is the covariance matrix, and $\gamma>0$ is risk aversion. Additional constraints can restrict shorting or concentration.

$$
\operatorname{Var}(w^\top R)=\sum_i\sum_jw_iw_j\operatorname{Cov}(R_i,R_j).
$$

The defining insight: risk depends on how assets move **together**.

## So what?

Portfolio selection becomes an optimization problem and produces an efficient frontier. In practice, noisy return and covariance estimates can produce unstable weights.

**Research connections:** Tobin separation, Bayesian portfolio choice, Black–Litterman, regularization, and robust optimization.

## References

Markowitz, H. (1952). [Portfolio Selection](https://doi.org/10.1111/j.1540-6261.1952.tb01525.x). *The Journal of Finance*, 7(1), 77–91.
