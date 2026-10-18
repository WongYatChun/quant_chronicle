---
title: "Risk-Neutral Valuation — Measures & Numeraires"
year: 1979
authors: "Stephen Ross, John Cox, Michael Harrison, David Kreps & Stanley Pliska"
track: "Derivatives"
section: "Foundations"
summary: "Can replication be expressed as a general discounted-expectation rule?"
---

## Why?

Can replication be expressed as a general discounted-expectation rule?

## Who?

Stephen Ross, John Cox, Michael Harrison, David Kreps & Stanley Pliska. Cox & Ross (1976). The Valuation of Options for Alternative Stochastic Processes.

## How?

With money-market account $B_t=\exp(\int_0^t r_sds)$, a replicable claim satisfies

$$\boxed{V_t=B_tE_t^Q[H/B_T].}$$

Under suitable integrability, discounted traded values are martingales under $Q$. In BSM, $dS_t=rS_tdt+\sigma S_tdW_t^Q$: physical drift is replaced by the pricing drift.

More generally, for a strictly positive traded numeraire $N$ and its associated measure,

$$V_t=N_tE_t^{Q^N}[H/N_T].$$

Choosing $N_t=P(t,T)$ gives $V_t=P(t,T)E_t^{Q^T}[H]$. This is useful for rate options. The numeraire identity is a later general formulation, not an attribution to a single 1979 paper.

## So what?

Risk-neutral probabilities are pricing weights, not investor beliefs. In finite models, no arbitrage corresponds to an equivalent martingale measure and completeness to uniqueness. Continuous-time results require stronger technical conditions, generally involving equivalent local martingale measures. Incomplete markets need additional choices for unreplicable claims.

**Research connections:** [Previous: Cox–Ross–Rubinstein — Binomial Replication]({{ "/notes/1979-binomial/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Cox & Ross (1976). The Valuation of Options for Alternative Stochastic Processes.

Harrison & Kreps (1979). Martingales and Arbitrage in Multiperiod Securities Markets.

Harrison & Pliska (1981). Martingales and Stochastic Integrals in the Theory of Continuous Trading.

Geman, El Karoui & Rochet (1995). Changes of Numéraire, Changes of Probability Measure and Option Pricing.
