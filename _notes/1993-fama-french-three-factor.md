---
title: "Fama–French — Three Factors"
year: 1993
authors: "Eugene Fama; Kenneth French"
track: "Asset Pricing & Alpha"
section: "Empirical Factors"
summary: "Size and value extend the market-only benchmark."
---

## Why?

Market beta alone leaves systematic average-return patterns associated with size and book-to-market.

## Who?

Fama and French: *The Cross-Section of Expected Stock Returns* (1992), followed by *Common Risk Factors in the Returns on Stocks and Bonds* (1993).

## How?

Construct traded factor spreads from joint size and book-to-market sorts. Schematically:

$$
SMB=\text{Small}-\text{Big},\qquad
HML=\text{High book-to-market}-\text{Low book-to-market}.
$$

Estimate

$$
R_{i,t}-R_{f,t}
=\alpha_i+\beta_iMKT_t+s_iSMB_t+h_iHML_t+\epsilon_{i,t}.
$$

The pricing hypothesis is

$$
\alpha_i=0
\quad\Rightarrow\quad
E[R_i-R_f]=\beta_iE[MKT]+s_iE[SMB]+h_iE[HML].
$$

A characteristic and a loading are distinct:

$$
\text{Book-to-market}_i\neq
\frac{\operatorname{Cov}(R_i,HML)}{\operatorname{Var}(HML)}.
$$

The expression on the right is a univariate exposure; the regression above estimates partial exposures jointly.

## So what?

A strategy's CAPM alpha can become exposure to size or value under FF3. The benchmark changes what counts as unexplained performance.

Statistical explanatory power alone does not establish whether the premia compensate for economic risk or reflect mispricing.

**Research connections:** Momentum challenges FF3; FF5 adds profitability and investment.

## References

Fama, E. F., and K. R. French (1992). *The Cross-Section of Expected Stock Returns*. *Journal of Finance*, 47(2), 427–465.

Fama, E. F., and K. R. French (1993). [Common Risk Factors in the Returns on Stocks and Bonds](https://doi.org/10.1016/0304-405X(93)90023-5). *Journal of Financial Economics*, 33(1), 3–56.
