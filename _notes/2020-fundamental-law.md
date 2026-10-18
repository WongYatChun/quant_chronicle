---
title: "Fundamental Law — Skill, Breadth & Implementation"
year: 2020
authors: "Richard Grinold; Ronald Kahn"
track: "Portfolio Theory"
topic: "Active Portfolio Management"
summary: "Connect forecast skill to achievable active performance."
---

## Why?

A strong forecast is only one ingredient of active performance.

$$
IR=\frac{\mathbb E[r_P-r_B]}{\sqrt{\operatorname{Var}(r_P-r_B)}}.
$$

## Who?

Richard Grinold — *The Fundamental Law of Active Management* (1989). Grinold & Kahn revisit its interpretation in chapters 3–5 of *Advances*.

## How?

The familiar approximation is:

$$
\boxed{IR\approx IC\sqrt{BR}}.
$$

$IC$ measures forecast skill; $BR$ counts independent investment decisions over the measurement period.

Including implementation losses gives the generalized approximation:

$$
\boxed{IR\approx TC\cdot IC\sqrt{BR}}.
$$

$TC$ describes how faithfully the implemented portfolio transfers forecasts into risk-adjusted positions.

## So what?

$$
\text{More securities or more trades}\ \not\Rightarrow\
\text{more independent breadth}.
$$

Correlated signals and overlapping holding periods reduce effective breadth. Constraints and costs can reduce implementation efficiency.

These formulas are organizing approximations, not universal identities: equal skill, independence, horizon conventions, and implementation assumptions matter.

**Next:** [Signal weighting]({{ '/notes/2020-signal-weighting/' | relative_url }}).

## References

Grinold & Kahn, *Advances in Active Portfolio Management* (published 2019; copyright 2020). Selected chapters discussed above. This is a thematic synthesis, not a claim that these ideas originated in 2020.
