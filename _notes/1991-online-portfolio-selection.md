---
title: "Online Portfolio Selection"
year: 1991
authors: "Thomas Cover; Helmbold, Schapire, Singer, Warmuth"
track: "Portfolio Theory"
topic: "Learning to Allocate"
summary: "Learn sequentially against a hindsight wealth benchmark."
---

## Why?

$$
\text{Allocate}\rightarrow\text{Observe}\rightarrow\text{Update}.
$$

Can allocation succeed without a specified return distribution?

## Who?

Cover (1991) — *Universal Portfolios*; Helmbold, Schapire, Singer & Warmuth (1998) — multiplicative portfolio updates.

## How?

Choose $b_t\in\Delta_N$ before observing gross returns $x_t>0$:

$$
\Delta_N=\{b\ge0:\mathbf1^\top b=1\},
\qquad W_T=W_0\prod_{t=1}^T b_t^\top x_t.
$$

Regret against the best constant rebalanced portfolio:

$$
\boxed{
R_T=\max_{b\in\Delta_N}\sum_{t=1}^T\log(b^\top x_t)
-\sum_{t=1}^T\log(b_t^\top x_t)
}.
$$

Exponentiated Gradient, initialized with positive weights:

$$
\boxed{
b_{i,t+1}=
\frac{b_{i,t}\exp(\eta x_{i,t}/(b_t^\top x_t))}
{\sum_jb_{j,t}\exp(\eta x_{j,t}/(b_t^\top x_t))}
}.
$$

## So what?

With suitable algorithms, learning rates, and assumptions:

$$
R_T/T\to0.
$$

This matches the benchmark's average log growth asymptotically; it does not imply positive returns or equal terminal wealth.

**Limitation:** rebalancing costs can invalidate frictionless guarantees. Fixed-rate EG does not automatically give vanishing regret.

**Connections:** [Kelly]({{ '/notes/1956-kelly/' | relative_url }}) uses expected log wealth; [end-to-end learning]({{ '/notes/2019-end-to-end-allocation/' | relative_url }}) trains a parameterized allocation pipeline.

## References

- Cover (1991), *Universal Portfolios*.
- Helmbold et al. (1998), *On-Line Portfolio Selection Using Multiplicative Updates*.
