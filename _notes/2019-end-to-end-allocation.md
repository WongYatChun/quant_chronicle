---
title: "Decision-Focused / End-to-End Learning"
year: 2019
authors: "Moody, Saffell; Amos, Kolter; Agrawal et al."
track: "Portfolio Theory"
topic: "Learning to Allocate"
summary: "Train predictive inputs against downstream portfolio utility."
---

## Why?

$$
\boxed{\min_\theta\text{ forecast error}
\ \not\equiv\ \max_\theta\text{ portfolio utility}}.
$$

Risk, costs, and constraints determine which errors matter.

## Who?

Moody & Saffell (2001) — direct trading optimization; Amos & Kolter (2017) — differentiable QP layers; Agrawal et al. (2019) — differentiable convex optimization layers. These are related foundations.

## How?

$$
\hat\mu_t=f_\theta(X_t),
$$

$$
w_t(\theta)=\arg\max_{w\in\mathcal W_t}
\left[
w^\top\hat\mu_t-\frac\gamma2w^\top\Sigma_tw
-C_t(w-\bar w_t)
\right].
$$

$\bar w_t$ is the portfolio before trading. Train on realized outcomes:

$$
\boxed{
\max_\theta\sum_t
\left[
w_t^\top r_{t+1}
-\frac\gamma2w_t^\top\Sigma_tw_t
-C_t(w_t-\bar w_t)
\right]
}.
$$

For a single decision, where differentiable:

$$
\frac{dU}{d\theta}
=\frac{\partial U}{\partial w}
\frac{\partial w}{\partial\hat\mu}
\frac{\partial\hat\mu}{\partial\theta}.
$$

Sequential training must also account for dependence through previous holdings.

## So what?

$$
\hat\mu_t\ \text{can be a decision score rather than }\
\mathbb E_t[r_{t+1}].
$$

Online learning and end-to-end learning are complementary axes: **when** the model updates versus **what** objective trains it.

**Limitation:** models can exploit misspecified costs and risk. Evaluate out-of-sample net portfolio performance.

## References

- Moody & Saffell (2001), *Learning to Trade via Direct Reinforcement*.
- Amos & Kolter (2017), *OptNet: Differentiable Optimization as a Layer in Neural Networks*.
- Agrawal et al. (2019), *Differentiable Convex Optimization Layers*.
