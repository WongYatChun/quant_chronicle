---
title: "Markowitz — Mean–Variance Optimization"
year: 1952
authors: "Harry Markowitz"
track: "Portfolio Theory"
topic: "Mean–Variance Optimization"
summary: "Choose holdings using expected returns and covariance."
---

## Why?

$$
\mu_p=w^\top\mu,\qquad \sigma_p^2=w^\top\Sigma w.
$$

Individual asset quality does not determine portfolio quality.

## Who?

Harry Markowitz — *Portfolio Selection* (1952). William Sharpe — *Mutual Fund Performance* (1966).

## How?

A modern mean–variance formulation:

$$
\boxed{\max_{w\in\mathcal W}\ w^\top\mu-\frac\gamma2w^\top\Sigma w},
\qquad \gamma>0.
$$

For a fully invested portfolio, $\mathbf1^\top w=1$. Varying $\gamma$ traces the efficient frontier.

With cash at $r_f$, let $\mu_e=\mu-r_f\mathbf1$. Unconstrained risky exposures satisfy:

$$
x^*=\frac1\gamma\Sigma^{-1}\mu_e.
$$

The tangency portfolio maximizes the Sharpe ratio:

$$
SR(w)=\frac{w^\top\mu_e}{\sqrt{w^\top\Sigma w}},
\qquad
w_T=\frac{\Sigma^{-1}\mu_e}{\mathbf1^\top\Sigma^{-1}\mu_e}.
$$

Assume $\Sigma\succ0$ and a positive normalization denominator.

## So what?

$$
\sigma_p^2=\sum_iw_i^2\sigma_i^2+
2\sum_{i<j}w_iw_j\rho_{ij}\sigma_i\sigma_j.
$$

**Diversification depends on covariance.** Positive leverage preserves Sharpe before financing frictions:

$$
SR(ax)=SR(x),\qquad a>0.
$$

Forecast error is amplified by inverse covariance:

$$
\Delta x^*=\frac1\gamma\Sigma^{-1}\Delta\mu.
$$

**Connections:** [Estimation risk]({{ '/notes/1986-estimation-regularization/' | relative_url }}) · [Kelly]({{ '/notes/1956-kelly/' | relative_url }}).

## References

- Markowitz (1952), [Portfolio Selection](https://doi.org/10.1111/j.1540-6261.1952.tb01525.x).
- Sharpe (1966), *Mutual Fund Performance*.
