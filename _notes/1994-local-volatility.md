---
title: "Dupire / Derman–Kani — Local Volatility"
year: 1994
authors: "Bruno Dupire; Emanuel Derman & Iraj Kani"
track: "Derivatives"
section: "Volatility models"
summary: "Can a diffusion reproduce the entire observed European option surface?"
---

## Why?

Can a diffusion reproduce the entire observed European option surface?

## Who?

Bruno Dupire; Emanuel Derman & Iraj Kani. Dupire (1994). Pricing with a Smile. *Risk*.

## How?

Specify

$$dS_t=(r-q)S_tdt+\sigma_{\rm loc}(t,S_t)S_tdW_t^Q.$$

For constant rates and dividend yield, the time-zero call surface gives

$$\boxed{\sigma_{\rm loc}^2(T,K)=\frac{2[\partial_TC+(r-q)K\partial_KC+qC]}{K^2\partial_{KK}C}.}$$

Local volatility is a function of time and spot, not Black–Scholes implied volatility. There is one Brownian driver and no independent volatility shock.

## So what?

Under regularity, a smooth arbitrage-free continuum of vanilla prices can be matched exactly. Quote noise makes derivatives unstable. Terminal marginals do not fix joint path dynamics: exotic values and future smile behavior can differ even when vanilla prices agree.

**Research connections:** [Previous: Heston — Stochastic Variance]({{ "/notes/1993-heston/" | relative_url }}) · [Next: SABR — A Tractable Smile]({{ "/notes/2002-sabr/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Dupire (1994). Pricing with a Smile. *Risk*.

Derman & Kani (1994). Riding on a Smile. *Risk*.
