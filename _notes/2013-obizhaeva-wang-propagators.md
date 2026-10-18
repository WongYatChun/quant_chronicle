---
title: Obizhaeva–Wang & Propagators — Transient Impact
year: 2013
authors: Anna Obizhaeva & Jiang Wang; Bouchaud and coauthors
track: Market Microstructure & Execution
section: Optimal Execution
summary: How should trading adapt to gradual liquidity recovery?
---

## Why?

How should trading adapt to gradual liquidity recovery?

## Who?

OW: 2005 working paper, 2013 publication. Bouchaud et al. (2004) develop empirical propagator models; Gatheral (2010) studies consistency restrictions.

## How?

In a simplified linear OW model, cumulative purchases $X$ displace prices by $D$:

$$dD_t=-\rho D_tdt+\eta dX_t.$$

For a recovered book and risk-neutral purchase of $Q$ shares by $T$, endpoint blocks are $Q/(2+\rho T)$ each and the interior rate is $\rho Q/(2+\rho T)$. A general propagator replaces exponential recovery:

$$D_t=\int_0^tG(t-s)v_sds.$$

## So what?

Recovery speed determines scheduling. The observed response to a trade also includes correlated future flow, so it differs from the propagator. In linear models, a positive-semidefinite symmetric kernel ensures nonnegative quadratic impact cost; admissible round trips should not generate negative expected costs. This is a combined note on related but distinct models.

## References

[OW: 2005 working paper, 2013 publication. Bouchaud et al. (2004) develop empirical propagator models; Gatheral (2010) studies consistency restrictions.](https://web.mit.edu/wangj/www/pap/ObizhaevaWang13.pdf)

Additional references: [Bouchaud et al.](https://arxiv.org/abs/cond-mat/0307332); [Gatheral](https://doi.org/10.1080/14697680903373692).
