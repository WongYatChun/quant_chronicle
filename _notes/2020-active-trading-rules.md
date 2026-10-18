---
title: "Implementation — Alpha Decay & Trading Rules"
year: 2020
authors: "Richard Grinold; Ronald Kahn"
track: "Portfolio Theory"
topic: "Active Portfolio Management"
summary: "Translate changing forecasts into cost-aware position adjustments."
---

## Why?

The frictionless target ignores current holdings and the lifetime of alpha.

$$
\text{Forecast}\rightarrow\text{Desired position}\rightarrow\text{Actual position}.
$$

## Who?

Grinold & Kahn — *Advances*, chapters 7–11: implementation efficiency, dynamic analysis, signal weighting, and linear/nonlinear trading rules.

## How?

A simple one-asset illustration, with pre-trade position $a_0$:

$$
\max_a\quad
\alpha a-\frac\gamma2\sigma^2a^2-\frac\kappa2(a-a_0)^2.
$$

$$
\boxed{
a^*=\frac{\alpha+\kappa a_0}{\gamma\sigma^2+\kappa}
=(1-\eta)a_0+\eta a_{\rm target}
},
$$

$$
a_{\rm target}=\frac{\alpha}{\gamma\sigma^2},
\qquad
\eta=\frac{\gamma\sigma^2}{\gamma\sigma^2+\kappa}.
$$

Proportional cost instead creates a no-trade region:

$$
C(a-a_0)=c|a-a_0|,
\qquad
\boxed{|\alpha-\gamma\sigma^2a_0|\le c}.
$$

For persistent forecasts, optimize a sequence:

$$
\max_{\{a_t\}}
\mathbb E_0\sum_{t=0}^{T-1}
\left[
a_t^\top\alpha_t-\frac\gamma2a_t^\top\Sigma_ta_t
-C_t(a_t-\bar a_t)
\right].
$$

## So what?

$$
\text{Optimal trade}\neq\text{immediate move to the frictionless target}.
$$

Signal persistence, costs, and current positions jointly determine trading. The static examples illustrate mechanisms; they are not the book's full dynamic solution.

Portfolio construction chooses the desired adjustment; execution chooses how to execute it.

**Next:** [Attribution]({{ '/notes/2020-active-attribution/' | relative_url }}).

## References

Grinold & Kahn, *Advances in Active Portfolio Management* (published 2019; copyright 2020). Selected chapters discussed above. This is a thematic synthesis, not a claim that these ideas originated in 2020.
