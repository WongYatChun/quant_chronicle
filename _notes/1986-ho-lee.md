---
title: "Ho–Lee — Fit the Initial Curve"
year: 1986
authors: "Thomas Ho & Sang Bin Lee"
track: "Derivatives"
section: "Interest-rate models"
summary: "Can today’s observed bond curve be an exact input to an arbitrage-free model?"
---

## Why?

Can today’s observed bond curve be an exact input to an arbitrage-free model?

## Who?

Thomas Ho & Sang Bin Lee. Ho & Lee (1986). [Term Structure Movements and Pricing Interest Rate Contingent Claims](https://doi.org/10.1111/j.1540-6261.1986.tb02528.x).

## How?

The original model is a binomial term-structure tree. Its continuous-time counterpart is

$$dr_t=\theta(t)dt+\sigma dW_t^Q.$$

Let $f(0,T)=-\partial_T\log P^{\rm mkt}(0,T)$. With constant $\sigma$ and $r_0=f(0,0)$,

$$\boxed{\theta(t)=\partial_t f(0,t)+\sigma^2t}$$

ensures exact initial-curve fit. Conditional variance is $\sigma^2(T-t)$; no mean reversion restrains it.

## So what?

Separates today’s curve from assumptions about future dynamics. Curve fit determines drift once volatility is chosen, not volatility itself. Hull–White adds mean reversion.

**Research connections:** [Previous: CIR — Nonnegative Short Rates]({{ "/notes/1985-cir/" | relative_url }}) · [Next: Hull–White — Curve Fit with Mean Reversion]({{ "/notes/1990-hull-white/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Ho & Lee (1986). [Term Structure Movements and Pricing Interest Rate Contingent Claims](https://doi.org/10.1111/j.1540-6261.1986.tb02528.x).
