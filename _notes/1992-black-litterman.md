---
title: "Black–Litterman — Priors & Views"
year: 1992
authors: "Fischer Black; Robert Litterman"
track: "Portfolio Theory"
topic: "Black–Litterman"
summary: "Update equilibrium returns using views and their confidence."
---

## Why?

Start from a benchmark; deviate when views justify it.

$$
\text{Prior}+\text{Views}\longrightarrow\text{Posterior returns}.
$$

## Who?

Fischer Black & Robert Litterman — *Global Portfolio Optimization* (1992).

## How?

Reverse MVO for equilibrium excess returns:

$$
\pi=\delta\Sigma w_{\rm mkt}.
$$

Specify independent Gaussian prior and view errors:

$$
\mu\sim N(\pi,\tau\Sigma),
\qquad
q=P\mu+\epsilon,\quad\epsilon\sim N(0,\Omega).
$$

A relative view, “A outperforms B by $2\%$”:

$$
P=\begin{bmatrix}1&-1&0\end{bmatrix},
\qquad q=0.02.
$$

$$
\boxed{
\mu_{BL}=\pi+\tau\Sigma P^\top
(P\tau\Sigma P^\top+\Omega)^{-1}(q-P\pi)
}.
$$

## So what?

Using $\Sigma$ as the risk matrix and unconstrained risky exposures:

$$
w_{BL}=\frac1\delta\Sigma^{-1}\mu_{BL},
$$

$$
\boxed{
w_{BL}=w_{\rm mkt}+
\frac\tau\delta P^\top
(P\tau\Sigma P^\top+\Omega)^{-1}(q-P\pi)
}.
$$

Cash absorbs any remaining budget. Additional constraints change this closed form.

$$
\Omega=k\Omega_0,\ k\to\infty
\quad\Rightarrow\quad w_{BL}\to w_{\rm mkt}.
$$

**Limitation:** results depend on the anchor and confidence calibration. Posterior predictive covariance is a separate modeling choice.

## References

Black & Litterman (1992), *Global Portfolio Optimization*, Financial Analysts Journal.
