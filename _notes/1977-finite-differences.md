---
title: "Finite Differences — Pricing on a Grid"
year: 1977
authors: "Numerical-analysis contributors; Michael Brennan & Eduardo Schwartz"
track: "Derivatives"
section: "Numerical & modern methods"
summary: "How can a pricing PDE be solved when no closed form is available?"
---

## Why?

How can a pricing PDE be solved when no closed form is available?

## Who?

Numerical-analysis contributors; Michael Brennan & Eduardo Schwartz. Brennan & Schwartz (1977). [The Valuation of American Put Options](https://doi.org/10.1111/j.1540-6261.1977.tb03321.x).

## How?

For the BSM PDE, replace spatial derivatives on a grid by

$$V_S\approx\frac{V_{i+1}-V_{i-1}}{2\Delta S},\qquad V_{SS}\approx\frac{V_{i+1}-2V_i+V_{i-1}}{(\Delta S)^2}.$$

Start with $V(T,S_i)=H(S_i)$ and solve backward, with boundary conditions. Explicit steps are simple but stability-limited; implicit steps solve linear systems; Crank–Nicolson combines time accuracy with possible oscillations at payoff kinks. American exercise requires solving an obstacle problem with $V\geq h$.

## So what?

Flexible in a few state dimensions and useful for Greeks. Boundary truncation, grid resolution, and payoff discontinuities affect accuracy. A grid with $m$ points in each of $d$ dimensions has roughly $m^d$ nodes.

**Research connections:** [Next: Boyle — Monte Carlo Pricing]({{ "/notes/1977-monte-carlo/" | relative_url }}) · [Derivatives overview]({{ "/derivatives/" | relative_url }})

## References

Brennan & Schwartz (1977). [The Valuation of American Put Options](https://doi.org/10.1111/j.1540-6261.1977.tb03321.x).
