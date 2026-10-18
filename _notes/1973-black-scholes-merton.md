---
title: "Black–Scholes–Merton — Dynamic Replication"
year: 1973
authors: "Fischer Black, Myron Scholes & Robert Merton"
track: "Derivatives"
summary: "Dynamic hedging removes the stock’s expected return from option pricing."
---

## Why?

An option depends on a risky stock. Can we value it without estimating the stock’s expected return or the buyer’s risk preferences?

## Who?

Black and Scholes (1973), and Merton (1973), established foundational continuous-time pricing and hedging results.

## How?

For a non-dividend-paying stock in the baseline model:

$$dS_t=\mu S_tdt+\sigma S_tdW_t.$$

Applying Itô’s lemma to $V(t,S)$ and hedging with $\Delta=\partial_SV$ eliminates instantaneous Brownian exposure. Self-financing replication and no arbitrage imply:

$$
\partial_tV+\tfrac12\sigma^2S^2\partial_{SS}V+rS\partial_SV-rV=0.
$$

For a European call, impose $V(T,S)=(S-K)^+$ and suitable boundary conditions.

## So what?

The stock drift $\mu$ disappears. A replicable payoff is priced through the cost of its hedge under the model’s assumptions.

Continuous trading, constant volatility, and frictionless markets are idealizations. Smiles, jumps, and trading costs motivate later models.

**Research connections:** binomial replication, risk-neutral valuation, local volatility, stochastic volatility, and deep hedging.

## References

Black, F. & Scholes, M. (1973). [The Pricing of Options and Corporate Liabilities](https://doi.org/10.1086/260062). *Journal of Political Economy*, 81(3), 637–654.

Merton, R. C. (1973). [Theory of Rational Option Pricing](https://doi.org/10.2307/3003143). *The Bell Journal of Economics and Management Science*, 4(1), 141–183.
