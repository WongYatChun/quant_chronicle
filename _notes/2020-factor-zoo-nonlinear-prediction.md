---
title: "Factor Zoo and Nonlinear Expected Return Prediction"
year: 2020
authors: "Shihao Gu; Bryan Kelly; Dacheng Xiu"
track: "Asset Pricing & Alpha"
section: "Factor Zoo and Nonlinear Expected Return Prediction"
summary: "Many return predictors become inputs to a joint nonlinear expected-return model."
---

## Why?

Empirical research documents many return predictors: valuation, momentum, profitability, investment, liquidity, and volatility. This expanding collection is often called the **factor zoo**, although a predictive characteristic is not automatically a priced risk factor.

How should these predictors be combined? A small additive model can miss nonlinear effects and interactions:

$$
E_t[r_{i,t+1}]=a+\sum_{\ell=1}^{L}b_\ell x_{i,t,\ell}
\quad\longrightarrow\quad
E_t[r_{i,t+1}]=g_\theta(x_{i,t}).
$$

For example, the predictive effect of momentum may depend on liquidity or the market state.

## Who?

Gu, Kelly, and Xiu (2020), *Empirical Asset Pricing via Machine Learning*, systematically compare methods for estimating conditional expected excess returns.

Their contribution is a broad empirical comparison, not the invention of machine learning or return prediction.

## How?

Pool observations across stocks and time:

$$
r_{i,t+1}=g_\theta(x_{i,t})+\epsilon_{i,t+1},
\qquad E_t[\epsilon_{i,t+1}]=0.
$$

Inputs combine firm characteristics, macroeconomic information, and industry indicators. A schematic fitting objective is

$$
\hat\theta=\arg\min_\theta
\sum_{(i,t)\in\mathrm{Train}}
\big[r_{i,t+1}-g_\theta(x_{i,t})\big]^2
+\lambda\mathcal P(\theta).
$$

Compare regularized linear models, dimension reduction, trees, and neural networks. Linear models provide an additive benchmark; trees and networks allow nonlinear responses and interactions.

The paper attributes important predictive gains from trees and neural networks to nonlinear interactions.

$$
\text{Many characteristics}
\rightarrow\text{Joint prediction model}
\rightarrow\hat\mu_{i,t}.
$$

Unlike IPCA, direct prediction does not require expected returns to pass through a low-dimensional latent-factor structure.

## So what?

The research object shifts from evaluating individual anomaly portfolios to estimating their combined conditional information:

$$
\text{Does signal }x_j\text{ predict returns?}
\quad\longrightarrow\quad
\text{What does }x_j\text{ add given the other inputs?}
$$

Forecasts can feed a constrained portfolio optimizer. Predictive success alone does not explain why a premium exists or establish net tradable alpha.

**Consequences for validation:** searching many candidate signals creates multiple-testing concerns; fitting flexible models creates overfitting concerns. These are related but distinct. Use chronological validation and an untouched test period, record the research search, and evaluate costs and turnover. Regularization does not itself correct multiple testing.

**Further reading:** Harvey–Liu–Zhu studies the multiple-testing consequences of the factor zoo. Detailed inference and validation methods belong in a separate research-methods note.

## References

Gu, S., B. Kelly, and D. Xiu (2020). [Empirical Asset Pricing via Machine Learning](https://doi.org/10.1093/rfs/hhaa009). *Review of Financial Studies*, 33(5), 2223–2273.

Harvey, C. R., Y. Liu, and H. Zhu (2016). [… and the Cross-Section of Expected Returns](https://doi.org/10.1093/rfs/hhv059). *Review of Financial Studies*, 29(1), 5–68. Further reading on multiple testing.
