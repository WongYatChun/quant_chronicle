---
title: "Kelly — Growth-Optimal Allocation"
year: 1956
authors: "John L. Kelly Jr."
track: "Portfolio Theory"
topic: "Growth-Optimal Allocation"
summary: "Maximize long-run compounded wealth."
---

## Why?

$$
W_T=W_0\prod_{t=1}^T(1+w^\top r_t).
$$

For i.i.d. returns and integrable log returns, almost surely:

$$
\frac1T\log(W_T/W_0)\longrightarrow
\mathbb E[\log(1+w^\top r)].
$$

## Who?

John L. Kelly Jr. — *A New Interpretation of Information Rate* (1956).

## How?

$$
\boxed{\max_{w\in\mathcal W}\mathbb E[\log(1+w^\top r)]},
\qquad 1+w^\top r>0\ \text{almost surely}.
$$

A bet pays $b$ per unit staked with probability $p$, otherwise losing the stake:

$$
\max_{0\le f<1}p\log(1+bf)+(1-p)\log(1-f),
$$

$$
f^*=\max\left(0,\frac{bp-(1-p)}b\right),\qquad 0<p<1.
$$

## So what?

Under a continuous-time diffusion with excess-return rate $\mu_e$ and covariance rate $\Sigma\succ0$:

$$
g(w)=r_f+w^\top\mu_e-\frac12w^\top\Sigma w,
\qquad
\boxed{w_K=\Sigma^{-1}\mu_e}.
$$

This is MVO with $\gamma=1$ under this model.

Fractional Kelly reduces exposure:

$$
w_c=cw_K,\quad 0<c<1,\qquad
\frac{g(w_c)-r_f}{g(w_K)-r_f}=2c-c^2.
$$

Half Kelly retains $75\%$ of optimal excess log growth at half the volatility in this diffusion model. Growth optimality does not control drawdowns.

**Connection:** [Online portfolio selection]({{ '/notes/1991-online-portfolio-selection/' | relative_url }}) learns without specifying a return distribution.

## References

Kelly (1956), *A New Interpretation of Information Rate*, Bell System Technical Journal.
