---
title: "Heston — Stochastic Variance"
year: 1993
authors: "Steven Heston"
track: "Derivatives"
section: "Volatility models"
summary: "Can changing variance and price–volatility dependence generate smiles tractably?"
---

## Why?

Can changing variance and price–volatility dependence generate smiles tractably?

## Who?

Steven Heston. Heston (1993). [A Closed-Form Solution for Options with Stochastic Volatility with Applications to Bond and Currency Options](https://doi.org/10.1093/rfs/6.2.327).

## How?

Under a chosen $Q$,

$$\begin{aligned}dS_t/S_t&=(r-q)dt+\sqrt{v_t}dW_t^S,\\dv_t&=\kappa(\theta-v_t)dt+\xi\sqrt{v_t}dW_t^v,\\d\langle W^S,W^v\rangle_t&=\rho dt.\end{aligned}$$

$\kappa$ is mean-reversion speed, $\theta$ long-run variance, $\xi$ variance volatility, and $\rho$ shock correlation. Negative $\rho$ supports equity skew. The affine structure yields a tractable characteristic function of $\log S_T$ and European prices by numerical Fourier integration.

## So what?

Variance adds an unhedgeable driver when only stock and cash trade. Risk-neutral variance parameters embed a volatility-risk pricing choice. A few parameters cannot fit every surface. CIR supplies the variance process; local volatility takes a different calibration approach.

**Research connections:** [Previous: Merton — Jump Diffusion]({{ "/notes/1976-merton-jumps/" | relative_url }}) · [Next: Dupire / Derman–Kani — Local Volatility]({{ "/notes/1994-local-volatility/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Heston (1993). [A Closed-Form Solution for Options with Stochastic Volatility with Applications to Bond and Currency Options](https://doi.org/10.1093/rfs/6.2.327).
