---
title: "LIBOR Market Model — Contract Forward Rates"
year: 1997
authors: "Alan Brace, Dariusz Gątarek & Marek Musiela"
track: "Derivatives"
section: "Interest-rate models"
summary: "Can we model finite-period rates used in contracts rather than instantaneous forwards?"
---

## Why?

Can we model finite-period rates used in contracts rather than instantaneous forwards?

## Who?

Alan Brace, Dariusz Gątarek & Marek Musiela. Brace, Gątarek & Musiela (1997). [The Market Model of Interest Rate Dynamics](https://doi.org/10.1111/1467-9965.00028).

## How?

In the original single-curve framework,

$$L_i(t)=\frac1{\delta_i}\left[\frac{P(t,T_i)}{P(t,T_{i+1})}-1\right].$$

Under the $T_{i+1}$-bond forward measure,

$$\boxed{dL_i(t)=L_i(t)\boldsymbol\sigma_i(t)^\top d\mathbf W_t^{i+1}.}$$

Deterministic volatility makes this forward lognormal under its own measure. A caplet paying $\delta_i(L_i(T_i)-K)^+$ at $T_{i+1}$ then has a Black-formula price. Simulating all rates under one common measure requires nonzero, coupled drifts.

## So what?

Connects directly to caplet quotes and models correlation across forward rates. Basic lognormal dynamics exclude negative rates and flexible smiles. This is the historical LIBOR single-curve formulation; collateralized multi-curve and overnight-rate contracts require extensions.

**Research connections:** [Previous: HJM — Forward-Curve Dynamics]({{ "/notes/1992-hjm/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Brace, Gątarek & Musiela (1997). [The Market Model of Interest Rate Dynamics](https://doi.org/10.1111/1467-9965.00028).
