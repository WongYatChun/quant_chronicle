---
title: "Merton — Jump Diffusion"
year: 1976
authors: "Robert Merton"
track: "Derivatives"
section: "Volatility models"
summary: "Can sudden price moves be included without abandoning tractable option valuation?"
---

## Why?

Can sudden price moves be included without abandoning tractable option valuation?

## Who?

Robert Merton. Merton (1976). [Option Pricing When Underlying Stock Returns Are Discontinuous](https://doi.org/10.1016/0304-405X(76)90022-2).

## How?

Under a selected $Q$, without dividends,

$$\frac{dS_t}{S_{t^-}}=(r-\lambda\kappa_J)dt+\sigma dW_t+(J-1)dN_t,$$

$$\log J\sim N(m,\delta^2),\qquad \kappa_J=E^Q[J-1]=e^{m+\delta^2/2}-1.$$

$N$ has intensity $\lambda$; the compensator keeps expected return at $r$. Conditional on $N_T=n$, log price is normal with variance $\sigma^2T+n\delta^2$. Thus

$$C_0=e^{-rT}\sum_{n\geq0}\frac{e^{-\lambda T}(\lambda T)^n}{n!}E^Q[(S_T-K)^+\mid N_T=n].$$

## So what?

Adds tails and short-dated smile effects. Stock and cash cannot hedge all jump outcomes. Merton’s original argument assumes diversifiable jump risk earns no premium; more generally risk-neutral jump parameters require calibration or additional assumptions.

**Research connections:** [Next: Heston — Stochastic Variance]({{ "/notes/1993-heston/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Merton (1976). [Option Pricing When Underlying Stock Returns Are Discontinuous](https://doi.org/10.1016/0304-405X(76)90022-2).
