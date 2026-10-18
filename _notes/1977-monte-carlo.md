---
title: "Boyle — Monte Carlo Pricing"
year: 1977
authors: "Phelim Boyle"
track: "Derivatives"
section: "Numerical & modern methods"
summary: "Can a risk-neutral expectation be computed without a high-dimensional state grid?"
---

## Why?

Can a risk-neutral expectation be computed without a high-dimensional state grid?

## Who?

Phelim Boyle. Boyle (1977). [Options: A Monte Carlo Approach](https://doi.org/10.1016/0304-405X(77)90005-8).

## How?

Simulate independent discounted payoffs $Y_m=e^{-rT}H_m$ under $Q$:

$$\boxed{\widehat V_0=\frac1M\sum_{m=1}^M Y_m,\qquad \widehat{\rm SE}=\frac{s_Y}{\sqrt M}.}$$

In BSM,

$$S_T=S_0\exp[(r-q-\sigma^2/2)T+\sigma\sqrt T Z],\quad Z\sim N(0,1).$$

Simulate intermediate observations for path-dependent claims. Antithetic paths and control variates reduce variance. Halving standard error requires four times as many independent paths, absent variance reduction.

## So what?

Natural for baskets and path dependence. The sampling rate does not deteriorate with dimension, but variance and cost can grow. Time discretization and missed barrier crossings introduce bias distinct from sampling error. Early exercise requires conditional expectations.

**Research connections:** [Previous: Finite Differences — Pricing on a Grid]({{ "/notes/1977-finite-differences/" | relative_url }}) · [Next: Longstaff–Schwartz — Regression for Exercise]({{ "/notes/2001-longstaff-schwartz/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Boyle (1977). [Options: A Monte Carlo Approach](https://doi.org/10.1016/0304-405X(77)90005-8).
