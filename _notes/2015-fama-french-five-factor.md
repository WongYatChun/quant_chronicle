---
title: "Fama–French — Five Factors"
year: 2015
authors: "Eugene Fama; Kenneth French"
track: "Asset Pricing & Alpha"
section: "Empirical Factors"
summary: "Profitability and investment expand empirical attribution."
---

## Why?

FF3 leaves return patterns associated with profitability and investment unexplained.

## Who?

Fama and French, *A Five-Factor Asset Pricing Model* (2015).

## How?

Add two portfolio spreads:

$$
RMW=\text{Robust profitability}-\text{Weak profitability},
$$

$$
CMA=\text{Conservative investment}-\text{Aggressive investment}.
$$

Then

$$
R_{i,t}-R_{f,t}
=\alpha_i+\beta_iMKT_t+s_iSMB_t+h_iHML_t
+r_iRMW_t+c_iCMA_t+\epsilon_{i,t}.
$$

The pricing hypothesis remains $\alpha_i=0$.

A valuation identity motivates the additional characteristics:

$$
M_t=\sum_{\tau=1}^{\infty}
\frac{E_t[\mathrm{Earnings}_{t+\tau}-\Delta B_{t+\tau}]}{(1+\rho)^\tau}.
$$

Here $B$ is book equity and $\rho$ is an implied discount rate. Holding other quantities fixed, higher expected earnings imply a higher discount rate; higher expected investment implies a lower one. This motivates the factors without uniquely deriving their empirical construction.

## So what?

Profitability and investment become standard attribution exposures. In the paper's examined US sample, HML is redundant for explaining average returns given the other four factors.

The model still struggles with some portfolios, notably small stocks with weak profitability and aggressive investment.

$$
FF5=FF3+RMW+CMA,\qquad MOM\notin FF5.
$$

**Research connection:** IPCA estimates latent factors and changing exposures instead of fixing a small named factor list.

## References

Fama, E. F., and K. R. French (2015). [A Five-Factor Asset Pricing Model](https://doi.org/10.1016/j.jfineco.2014.10.010). *Journal of Financial Economics*, 116(1), 1–22.
