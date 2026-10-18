---
title: "Vasicek — Gaussian Mean Reversion"
year: 1977
authors: "Oldřich Vasicek"
track: "Derivatives"
section: "Interest-rate models"
summary: "Can a stochastic short rate generate a tractable term structure?"
---

## Why?

Can a stochastic short rate generate a tractable term structure?

## Who?

Oldřich Vasicek. Vasicek (1977). [An Equilibrium Characterization of the Term Structure](https://doi.org/10.1016/0304-405X(77)90016-2).

## How?

Under $Q$,

$$dr_t=\kappa(\theta-r_t)dt+\sigma dW_t,$$

$$E_t^Q[r_T]=\theta+(r_t-\theta)e^{-\kappa\tau},\quad\operatorname{Var}_t^Q(r_T)=\frac{\sigma^2}{2\kappa}(1-e^{-2\kappa\tau}).$$

Gaussian integrated rates imply

$$P(t,T)=E_t^Q[e^{-\int_t^T r_sds}]=A(t,T)e^{-B(t,T)r_t},\quad B=\frac{1-e^{-\kappa\tau}}{\kappa}.$$

$\theta$ here is a risk-neutral long-run level, not necessarily a physical forecast.

## So what?

Mean reversion and affine bond prices make valuation tractable. Gaussian rates can be negative. One factor restricts curve movements, and constant parameters cannot generally match an arbitrary initial curve.

**Research connections:** [Next: CIR — Nonnegative Short Rates]({{ "/notes/1985-cir/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Vasicek (1977). [An Equilibrium Characterization of the Term Structure](https://doi.org/10.1016/0304-405X(77)90016-2).
