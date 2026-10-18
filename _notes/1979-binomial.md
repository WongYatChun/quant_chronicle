---
title: "Cox–Ross–Rubinstein — Binomial Replication"
year: 1979
authors: "John Cox, Stephen Ross & Mark Rubinstein"
track: "Derivatives"
section: "Foundations"
summary: "Can replication be understood with two price moves and extended to early exercise?"
---

## Why?

Can replication be understood with two price moves and extended to early exercise?

## Who?

John Cox, Stephen Ross & Mark Rubinstein. Cox, Ross & Rubinstein (1979). [Option Pricing: A Simplified Approach](https://doi.org/10.1016/0304-405X(79)90015-1).

## How?

One step gives stock prices $uS,dS$, option values $V_u,V_d$, and cash growth $R=e^{r\Delta t}$. Replication solves

$$\Delta uS+Rb=V_u,\qquad\Delta dS+Rb=V_d.$$

$$\Delta=\frac{V_u-V_d}{S(u-d)},\qquad V=\frac{qV_u+(1-q)V_d}{R},\quad q=\frac{R-d}{u-d}.$$

No arbitrage requires $d<R<u$. Actual up-move probability is absent. Work backward through a tree; at exercise dates take the maximum of exercise and continuation values. With $u=e^{\sigma\sqrt{\Delta t}},d=1/u$, European prices converge to BSM as the mesh shrinks.

## So what?

Makes replication and early exercise computational. A finite tree introduces discretization error; the pricing probability comes from replication, not a forecast.

**Research connections:** [Previous: Black–Scholes–Merton — Replication, Greeks & Hedging]({{ "/notes/1973-black-scholes-merton/" | relative_url }}) · [Next: Risk-Neutral Valuation — Measures & Numeraires]({{ "/notes/1979-risk-neutral-valuation/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Cox, Ross & Rubinstein (1979). [Option Pricing: A Simplified Approach](https://doi.org/10.1016/0304-405X(79)90015-1).
