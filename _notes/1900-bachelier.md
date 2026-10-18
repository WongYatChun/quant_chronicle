---
title: "Bachelier — Normal Price Dynamics"
year: 1900
authors: "Louis Bachelier"
track: "Derivatives"
section: "Foundations"
summary: "How can random price changes be modeled and an option payoff valued?"
---

## Why?

How can random price changes be modeled and an option payoff valued?

## Who?

Louis Bachelier. Bachelier (1900). [Théorie de la spéculation](https://doi.org/10.24033/asens.476).

## How?

In modern notation, the zero-drift, zero-rate normal model is

$$dS_t=\sigma\,dW_t,\qquad S_T=S_0+\sigma\sqrt T Z,\quad Z\sim N(0,1).$$

Here $\sigma$ is absolute price volatility. A call has value

$$C_0=E[(S_T-K)^+]=(S_0-K)\Phi(d)+\sigma\sqrt T\phi(d),\qquad d=\frac{S_0-K}{\sigma\sqrt T}.$$

This follows by integrating the positive payoff against the normal density. At the money, $C_0=\sigma\sqrt{T/(2\pi)}$.

## So what?

An early mathematical option-valuation framework. Prices can be negative. The fair-game assumption is not the later dynamic-replication justification for choosing a pricing distribution.

**Research connections:** [Next: Black–Scholes–Merton — Replication, Greeks & Hedging]({{ "/notes/1973-black-scholes-merton/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Bachelier (1900). [Théorie de la spéculation](https://doi.org/10.24033/asens.476).
