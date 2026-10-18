---
title: "Longstaff–Schwartz — Regression for Exercise"
year: 2001
authors: "Francis Longstaff & Eduardo Schwartz"
track: "Derivatives"
section: "Numerical & modern methods"
summary: "How can continuation values for early exercise be estimated from simulated paths?"
---

## Why?

How can continuation values for early exercise be estimated from simulated paths?

## Who?

Francis Longstaff & Eduardo Schwartz. Longstaff & Schwartz (2001). [Valuing American Options by Simulation: A Simple Least-Squares Approach](https://doi.org/10.1093/rfs/14.1.113).

## How?

Work backward through exercise dates. Regress discounted future policy cash flows $Y_j$ on basis functions of the current sufficient state:

$$\widehat\beta_j=\arg\min_\beta\sum_{m\in\mathcal I_j}[Y_j^{(m)}-\beta^\top\phi(X_j^{(m)})]^2.$$

Typically $\mathcal I_j$ contains in-the-money paths. Set

$$\widehat C_j(x)=\widehat\beta_j^\top\phi(x),\qquad\text{exercise if }h(x)\geq\widehat C_j(x).$$

If exercise occurs, replace the path’s later cash flow with the immediate payoff. Otherwise retain its later cash flow.

## So what?

Converts optimal stopping into backward supervised regressions. State selection and regression quality matter. Evaluate the learned policy on independent paths: its true expected payoff is a lower bound on the optimal stopping value, while a finite estimate has sampling error.

**Research connections:** [Previous: Boyle — Monte Carlo Pricing]({{ "/notes/1977-monte-carlo/" | relative_url }}) · [Next: XVA — Default, Collateral & Funding]({{ "/notes/2011-xva/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Longstaff & Schwartz (2001). [Valuing American Options by Simulation: A Simple Least-Squares Approach](https://doi.org/10.1093/rfs/14.1.113).
