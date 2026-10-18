---
title: "Rough Volatility — Irregular Variance Dynamics"
year: 2016
authors: "Jim Gatheral, Thibault Jaisson, Mathieu Rosenbaum; Christian Bayer & Peter Friz"
track: "Derivatives"
section: "Volatility models"
summary: "Can rougher volatility dynamics explain irregular volatility and steep short-maturity skew?"
---

## Why?

Can rougher volatility dynamics explain irregular volatility and steep short-maturity skew?

## Who?

Jim Gatheral, Thibault Jaisson, Mathieu Rosenbaum; Christian Bayer & Peter Friz. Bayer, Friz & Gatheral (2016). [Pricing under Rough Volatility](https://doi.org/10.1080/14697688.2015.1099717).

## How?

Local increments scale approximately as $|\Delta t|^H$ with $0<H<1/2$, rather than Brownian scaling $|\Delta t|^{1/2}$. In rough Bergomi,

$$X_t=\sqrt{2H}\int_0^t(t-s)^{H-1/2}dB_s,$$

$$v_t=\xi_0(t)\exp(\eta X_t-\tfrac12\eta^2t^{2H}),\qquad dS_t/S_t=(r-q)dt+\sqrt{v_t}dW_t.$$

$\xi_0(t)=E^Q[v_t]$ is the initial forward variance curve; price and volatility shocks have correlation $\rho$. Typically short-maturity ATM skew scales as $T^{H-1/2}$.

## So what?

Makes volatility history matter and supports steep short-end skew. General dynamics are not finite-dimensional Markov, increasing simulation cost. Empirical estimates of roughness are sensitive to volatility measurement noise.

**Research connections:** [Previous: SABR — A Tractable Smile]({{ "/notes/2002-sabr/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Bayer, Friz & Gatheral (2016). [Pricing under Rough Volatility](https://doi.org/10.1080/14697688.2015.1099717).

Gatheral, Jaisson & Rosenbaum (2018; preprint 2014). [Volatility Is Rough](https://arxiv.org/abs/1410.3394).
