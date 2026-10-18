---
title: "Factor Zoo and Nonlinear Expected Return Prediction"
year: 2020
authors: "Campbell Harvey; Yan Liu; Heqing Zhu; Shihao Gu; Bryan Kelly; Dacheng Xiu"
track: "Asset Pricing & Alpha"
section: "Factor Zoo and Nonlinear Expected Return Prediction"
summary: "Many predictors motivate selection controls, regularization, and nonlinear models."
---

## Why?

Hundreds of candidate predictors create two problems:

$$
\text{Many tests}\rightarrow\text{Selection bias},
\qquad
\text{Many inputs}\rightarrow\text{Estimation error}.
$$

Useful information may also depend on nonlinear interactions. Adding predictors one at a time can miss their joint structure.

## Who?

Harvey, Liu, and Zhu (2016), *… and the Cross-Section of Expected Returns*, examine multiple testing.

Gu, Kelly, and Xiu (2020), *Empirical Asset Pricing via Machine Learning*, compare methods for predicting conditional expected excess returns.

## How?

**Selection:** with $M$ true null hypotheses tested at size $a$,

$$
E[\text{False rejections}]=Ma.
$$

Testing 100 true nulls at 5% yields five false rejections on average. Family-wise error or false-discovery controls address different aspects of this search. Harvey–Liu–Zhu argue for a higher hurdle for new factors; their $t>3$ guidance is contextual, not universal.

**Joint prediction:** replace a small fixed linear specification with

$$
r_{i,t+1}=g_\theta(x_{i,t})+\epsilon_{i,t+1}.
$$

A schematic regularized objective is

$$
\min_\theta\;
\sum_{(i,t)\in\mathrm{Train}}
\big(r_{i,t+1}-g_\theta(x_{i,t})\big)^2
+\lambda\mathcal P(\theta).
$$

Inputs can include firm characteristics, macro information, and industry indicators. Compare penalized regressions, dimension reduction, trees, and neural networks using chronological training, validation, and testing.

Gu–Kelly–Xiu attribute important gains from trees and neural networks to nonlinear interactions.

## So what?

$$
\text{Many candidate signals}
\rightarrow
\text{Regularized joint estimation}
\rightarrow
\text{Out-of-sample forecasts}.
$$

Regularization addresses estimation variance; it does not erase data snooping. Record failed specifications and preserve an untouched test period. Repeatedly consulting it makes it part of model selection.

For portfolio research:

$$
\hat\mu_{i,t}=g_{\hat\theta}(x_{i,t})
\rightarrow\text{Constrained weights}
\rightarrow\text{Net performance}.
$$

Forecast accuracy, economic explanation, and tradable alpha are separate achievements. Evaluate costs, turnover, and capacity alongside predictive performance.

## References

Harvey, C. R., Y. Liu, and H. Zhu (2016). [… and the Cross-Section of Expected Returns](https://doi.org/10.1093/rfs/hhv059). *Review of Financial Studies*, 29(1), 5–68.

Gu, S., B. Kelly, and D. Xiu (2020). [Empirical Asset Pricing via Machine Learning](https://doi.org/10.1093/rfs/hhaa009). *Review of Financial Studies*, 33(5), 2223–2273.
