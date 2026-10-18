---
title: "Hull–White — Curve Fit with Mean Reversion"
year: 1990
authors: "John Hull & Alan White"
track: "Derivatives"
section: "Interest-rate models"
summary: "Can exact initial-curve fit coexist with Vasicek-style mean reversion?"
---

## Why?

Can exact initial-curve fit coexist with Vasicek-style mean reversion?

## Who?

John Hull & Alan White. Hull & White (1990). [Pricing Interest-Rate-Derivative Securities](https://doi.org/10.1093/rfs/3.4.573).

## How?

Under $Q$, with constant $a,\sigma$,

$$dr_t=[\theta(t)-ar_t]dt+\sigma dW_t,$$

$$\theta(t)=\partial_t f(0,t)+af(0,t)+\frac{\sigma^2}{2a}(1-e^{-2at}).$$

Equivalently $r_t=x_t+\phi(t)$, with $dx_t=-ax_tdt+\sigma dW_t$ and a deterministic curve-fitting shift. Bond prices remain affine, and

$$\operatorname{Var}_t^Q(r_T)=\frac{\sigma^2}{2a}(1-e^{-2a(T-t)}).$$

## So what?

Fits today’s curve, retains tractable bond options, and supports trees for early exercise. Option quotes help calibrate volatility and mean reversion. Gaussian negative rates remain possible; a single factor restricts curve dynamics.

**Research connections:** [Previous: Ho–Lee — Fit the Initial Curve]({{ "/notes/1986-ho-lee/" | relative_url }}) · [Next: HJM — Forward-Curve Dynamics]({{ "/notes/1992-hjm/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Hull & White (1990). [Pricing Interest-Rate-Derivative Securities](https://doi.org/10.1093/rfs/3.4.573).
