---
title: "Black–Scholes–Merton — Replication, Greeks & Hedging"
year: 1973
authors: "Fischer Black, Myron Scholes & Robert Merton"
track: "Derivatives"
section: "Foundations"
summary: "Can an option be priced and hedged without estimating the stock’s expected return?"
---

## Why?

Can an option be priced and hedged without estimating the stock’s expected return?

## Who?

Fischer Black, Myron Scholes & Robert Merton. Black & Scholes (1973). [The Pricing of Options and Corporate Liabilities](https://doi.org/10.1086/260062).

## How?

### Replication and the PDE

Assume no dividends, constant $r,\sigma$, frictionless continuous trading, and a self-financing strategy:

$$dS=\mu S\,dt+\sigma S\,dW,\qquad dB=rB\,dt.$$

Itô’s lemma gives

$$dV=(V_t+\mu SV_S+\tfrac12\sigma^2S^2V_{SS})dt+\sigma SV_SdW.$$

Against one short option, hold $\Delta=V_S$ shares. Its instantaneous gain is $\Delta dS-dV$: both Brownian risk and $\mu$ cancel. No arbitrage requires

$$\Delta dS-dV=r(\Delta S-V)dt,$$

hence

$$\boxed{V_t+\tfrac12\sigma^2S^2V_{SS}+rSV_S-rV=0.}$$

### European call

For $\tau=T-t$ and terminal payoff $(S-K)^+$:

$$C=S\Phi(d_1)-Ke^{-r\tau}\Phi(d_2),$$

$$d_1=\frac{\log(S/K)+(r+\sigma^2/2)\tau}{\sigma\sqrt\tau},\qquad d_2=d_1-\sigma\sqrt\tau.$$

$\Phi$ and $\phi$ denote the standard normal CDF and density.

### First-order Greeks

All sensitivities below hold the other inputs fixed. Volatility is in decimal units, rates are continuously compounded, and $t$ is calendar time.

| Greek | Definition | European call | Meaning |
|---|---|---|---|
| Delta | $V_S$ | $\Phi(d_1)$ | Spot exposure |
| Vega | $V_\sigma$ | $S\phi(d_1)\sqrt\tau$ | Volatility exposure |
| Theta | $V_t$ | $-S\phi(d_1)\sigma/(2\sqrt\tau)-rKe^{-r\tau}\Phi(d_2)$ | Calendar-time decay |
| Rho | $V_r$ | $K\tau e^{-r\tau}\Phi(d_2)$ | Rate exposure |

For a one-volatility-point move use $0.01\times\mathrm{Vega}$; for one rate basis point use $10^{-4}\times\mathrm{Rho}$. Theta here is per year.

### Main second-order Greeks

| Greek | Definition | European call | Meaning |
|---|---|---|---|
| Gamma | $V_{SS}$ | $\phi(d_1)/(S\sigma\sqrt\tau)$ | Delta changes with spot |
| Vanna | $V_{S\sigma}$ | $-\phi(d_1)d_2/\sigma$ | Delta changes with volatility |
| Volga / Vomma | $V_{\sigma\sigma}$ | $\mathrm{Vega}\,d_1d_2/\sigma$ | Vega changes with volatility |
| Charm | $V_{St}$ | $-\phi(d_1)[2r\tau-d_2\sigma\sqrt\tau]/(2\tau\sigma\sqrt\tau)$ | Delta changes with calendar time |

Charm defined using time-to-expiry has the opposite sign. These are selected second derivatives, not the full Hessian of the pricing function.

For small spot and implied-volatility changes, fixed rates, and retaining leading time and quadratic spot/volatility terms:

$$\begin{aligned}\Delta V\approx{}&\Theta\Delta t+\Delta\,\Delta S+\mathrm{Vega}\,\Delta\sigma\\&+\tfrac12\Gamma(\Delta S)^2+\mathrm{Vanna}\,\Delta S\Delta\sigma+\tfrac12\mathrm{Volga}(\Delta\sigma)^2.\end{aligned}$$

Here the standalone $\Delta$ is the Greek; $\Delta S$ is a price change. Higher time terms are omitted. The hedge ratio changes as

$$\Delta(\mathrm{Delta})\approx\Gamma\Delta S+\mathrm{Vanna}\Delta\sigma+\mathrm{Charm}\Delta t.$$

BSM dynamics assume constant volatility. Vega, vanna, and volga describe sensitivity of its pricing formula to changes in the volatility input, including market-implied volatility.

### Delta-hedged P&L

A short option is hedged with $+\Delta$ shares and a financing account. Delta removes first-order spot exposure, not every source of risk.

Conversely, a long option hedged with $-\Delta$ shares, including cash financing, has the local approximation

$$d\Pi\approx\tfrac12\Gamma S^2(\sigma_{\mathrm{realized}}^2-\sigma_{\mathrm{model}}^2)dt.$$

This uses continuous spot paths and a fixed pricing-volatility input. Gamma varies through time, so cumulative P&L is gamma-weighted variance exposure. Jumps, discrete hedging, volatility repricing, and costs add other terms.

## So what?

Replication removes expected stock return and investor preferences from the price. Greeks translate valuation into risk exposures and hedge adjustments. Continuous rebalancing is idealized: jump risk, volatility changes, and costs motivate richer models and deep hedging.

**Research connections:** [Previous: Bachelier — Normal Price Dynamics]({{ "/notes/1900-bachelier/" | relative_url }}) · [Next: Cox–Ross–Rubinstein — Binomial Replication]({{ "/notes/1979-binomial/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Black & Scholes (1973). [The Pricing of Options and Corporate Liabilities](https://doi.org/10.1086/260062).

Merton (1973). [Theory of Rational Option Pricing](https://doi.org/10.2307/3003143).
