---
title: "Risk Budgeting & Risk Parity"
year: 2010
authors: "Edward Qian; Maillard, Roncalli, Teiletche"
track: "Portfolio Theory"
topic: "Risk-Based Allocation"
summary: "Allocate risk contributions rather than capital equally."
---

## Why?

$$
w_i=1/N\quad\nRightarrow\quad RC_i=RC_j.
$$

Equal capital is not equal risk.

## Who?

Edward Qian (2005) — risk parity; Maillard, Roncalli & Teïletche (2010) — equal risk contribution analysis. Bridgewater All Weather (1996) is a practical precursor.

## How?

$$
\sigma_p=\sqrt{w^\top\Sigma w},
\qquad
RC_i=w_i\frac{\partial\sigma_p}{\partial w_i}
=\frac{w_i(\Sigma w)_i}{\sigma_p}.
$$

$$
\sum_iRC_i=\sigma_p.
$$

For budgets $b_i>0$, $\sum_i b_i=1$:

$$
\boxed{
RC_i=b_i\sigma_p
\iff w_i(\Sigma w)_i=b_iw^\top\Sigma w
}.
$$

With $\Sigma\succ0$, solve:

$$
x^*=\arg\min_{x>0}
\left[\frac12x^\top\Sigma x-\sum_i b_i\log x_i\right],
\qquad w=\frac{x^*}{\mathbf1^\top x^*}.
$$

## So what?

For uncorrelated assets:

$$
w_i\propto\frac{\sqrt{b_i}}{\sigma_i}.
$$

Equal risk budgets imply inverse-volatility weights in this case.

**Limitation:** equal asset risk contributions need not diversify economic factors or maximize Sharpe.

Hierarchical Risk Parity (López de Prado, 2016) uses clustering and recursive allocation; it is a related approach, not an exact equal-risk-contribution solver.

## References

- Qian (2005), *Risk Parity Portfolios*.
- Maillard, Roncalli & Teïletche (2010), *The Properties of Equally Weighted Risk Contribution Portfolios*.
- López de Prado (2016), *Building Diversified Portfolios that Outperform Out of Sample*.
