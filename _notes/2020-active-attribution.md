---
title: "Portfolio Analysis & Attribution"
year: 2020
authors: "Richard Grinold; Ronald Kahn"
track: "Portfolio Theory"
topic: "Active Portfolio Management"
summary: "Explain returns through exposures, residuals, and implementation."
---

## Why?

$$
\text{Positive active return}\ \not\Rightarrow\
\text{successful stock-selection forecasts}.
$$

Returns can come from intended signals, incidental factors, or implementation.

## Who?

Grinold & Kahn — *Advances*, chapters 13–14: attribution and portfolio description.

## How?

For beginning-of-period active weights $a_t=w_{P,t}-w_{B,t}$ and a factor return model:

$$
r_{t+1}=B_tf_{t+1}+\epsilon_{t+1},
$$

$$
\boxed{
r^{\rm active}_{t+1}
=a_t^\top B_tf_{t+1}
+a_t^\top\epsilon_{t+1}
}.
$$

Net performance also deducts incremental costs:

$$
r^{\rm active,net}_{t+1}
=r^{\rm active}_{t+1}-C_t.
$$

For an explicit signal decomposition $a_t=\sum_k a_t^{(k)}$:

$$
r^{\rm active}_{t+1}
=\sum_k(a_t^{(k)})^\top r_{t+1}.
$$

## So what?

Separate intended exposure from incidental bets and implementation losses.

$$
\text{Return attribution}\neq\text{causal explanation}.
$$

Factor results depend on the chosen model. Signal attribution depends on the holdings decomposition; correlated signals and shared costs prevent a unique allocation without conventions.

The equations are a simple holdings-based illustration. Multi-period linking requires additional treatment.

## References

Grinold & Kahn, *Advances in Active Portfolio Management* (published 2019; copyright 2020). Selected chapters discussed above. This is a thematic synthesis, not a claim that these ideas originated in 2020.
