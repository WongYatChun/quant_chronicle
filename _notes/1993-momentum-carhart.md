---
title: "Momentum & Carhart — Prediction and Attribution"
year: 1993
authors: "Narasimhan Jegadeesh; Sheridan Titman; Mark Carhart"
track: "Asset Pricing & Alpha"
section: "Empirical Factors"
summary: "Past winners become a signal and then a performance benchmark."
---

## Why?

Does past relative performance predict future returns? If so, does a successful fund earn independent alpha or simply hold recent winners?

## Who?

Jegadeesh and Titman (1993) document intermediate-horizon momentum. Carhart (1997) incorporates momentum into mutual-fund performance attribution.

## How?

Rank stocks on cumulative past returns:

$$
s_{i,t}=\prod_{j=1}^{J}(1+r_{i,t-j})-1.
$$

Buy winners and sell losers:

$$
MOM_{t+1}=R^{W}_{t+1}-R^{L}_{t+1}.
$$

The original study considers 3–12 month formation and holding horizons. A common later convention uses months $t-12$ through $t-2$, skipping the latest month.

Carhart adds a momentum factor to FF3:

$$
R_{p,t}-R_{f,t}
=\alpha_p+\beta_pMKT_t+s_pSMB_t+h_pHML_t+m_pMOM_t+\epsilon_{p,t}.
$$

## So what?

Momentum links a predictive characteristic to a traded portfolio and then to a benchmark:

$$
\text{Past returns}\rightarrow\text{Signal}\rightarrow\text{Factor exposure}.
$$

$$
\alpha^{CAPM}\neq\alpha^{FF3}\neq\alpha^{Carhart}
\quad\text{in general}.
$$

Carhart finds that common factors and expenses explain much of fund-performance persistence. Positive estimated alpha alone does not establish skill; zero alpha does not imply that inexpensive factor exposure lacks investment value.

**Research connection:** FF5 extends FF3 with two different factors; momentum remains outside FF5.

## References

Jegadeesh, N., and S. Titman (1993). [Returns to Buying Winners and Selling Losers: Implications for Stock Market Efficiency](https://doi.org/10.1111/j.1540-6261.1993.tb04702.x). *Journal of Finance*, 48(1), 65–91.

Carhart, M. M. (1997). [On Persistence in Mutual Fund Performance](https://doi.org/10.1111/j.1540-6261.1997.tb03808.x). *Journal of Finance*, 52(1), 57–82.
