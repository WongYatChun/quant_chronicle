---
title: "Deep Hedging — Learn the Trading Policy"
year: 2019
authors: "Hans Bühler, Lukas Gonon, Josef Teichmann & Ben Wood"
track: "Derivatives"
section: "Numerical & modern methods"
summary: "Can a hedging policy be optimized directly under costs, constraints, and incomplete markets?"
---

## Why?

Can a hedging policy be optimized directly under costs, constraints, and incomplete markets?

## Who?

Hans Bühler, Lukas Gonon, Josef Teichmann & Ben Wood. Bühler, Gonon, Teichmann & Wood (2019; preprint 2018). [Deep Hedging](https://arxiv.org/abs/1802.03042).

## How?

Use discounted prices and cash flows. For premium $p$, payoff $H$, holdings $\delta_j$, and trading costs $c_j$, terminal profit is

$$\Pi=p-H+\sum_{j=0}^{n-1}\delta_j^\top(S_{j+1}-S_j)-\sum_{j=0}^{n-1}c_j(\delta_j-\delta_{j-1}).$$

Specify $\delta_j=\pi_\theta(X_j,\delta_{j-1})$ using information available at $j$, then train

$$\boxed{\theta^*=\arg\min_\theta\rho(-\Pi).}$$

For example $\rho(L)=\gamma^{-1}\log E[e^{\gamma L}]$. Holdings enter the policy because changing them incurs costs. Liquidation costs must be added when required by the settlement convention.

## So what?

Learns the balance between residual hedge risk and costs. Results depend on the objective, constraints, and training distribution; evaluation needs independent paths and stress scenarios. It does not select a unique option price without a rule such as utility indifference.

**Research connections:** [Previous: XVA — Default, Collateral & Funding]({{ "/notes/2011-xva/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Bühler, Gonon, Teichmann & Wood (2019; preprint 2018). [Deep Hedging](https://arxiv.org/abs/1802.03042).
