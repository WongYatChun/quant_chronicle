---
title: "Exotic Derivatives — Paths, Dependence & Exercise"
year: 1990
authors: "Multiple academic and industry contributors"
track: "Derivatives"
section: "Exotic derivatives"
summary: "How can contingent claims meet needs beyond a terminal single-asset payoff?"
---

## Why?

How can contingent claims meet needs beyond a terminal single-asset payoff?

## Who?

Multiple academic and industry contributors. Garman (1976). The Pricing of Supertanker Options. *Journal of Financial Economics*.

## How?

This is a thematic entry covering developments across decades; 1990 is an organizing marker, not an invention date.

| Structure | Example | Main risk |
|---|---|---|
| Asian | $(T^{-1}\int_0^T S_tdt-K)^+$ | Path average |
| Barrier | $(S_T-K)^+\mathbf1_{\{\max_{t\leq T}S_t<B\}}$ | Barrier crossing |
| Lookback | $S_T-\min_{t\leq T}S_t$ | Path extremes |
| Basket | $(\sum_i a_iS_{i,T}-K)^+$ | Cross-asset dependence |
| Quanto | Fixed-FX conversion of foreign payoff | Equity–FX dependence |
| Bermudan | Exercise on selected dates | Continuation value |
| Autocallable | Conditional early redemption | Path and observation rules |

For FX $X$ quoted domestic per foreign, the domestic-measure drift of foreign equity is, in a lognormal setup,

$$\mu_S^{Q_d}=r_f-q-\rho\sigma_S\sigma_X.$$

For Bermudan exercise,

$$V_j=\max\{h_j,E_j^Q[e^{-\int_{t_j}^{t_{j+1}}r_sds}V_{j+1}]\}.$$

## So what?

Vanilla surfaces identify terminal marginals, not full path or cross-asset dependence. Models agreeing on vanilla prices can disagree on exotic values. Monitoring conventions and exercise rights are part of the payoff. Numerical methods become central.

**Research connections:** [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Garman (1976). The Pricing of Supertanker Options. *Journal of Financial Economics*.

Goldman, Sosin & Gatto (1979). Path Dependent Options: Buy at the Low, Sell at the High. *Journal of Finance*.

Geman, El Karoui & Rochet (1995). Changes of Numéraire, Changes of Probability Measure and Option Pricing.
