---
title: Avellaneda–Stoikov — Optimal Quoting
year: 2008
authors: Marco Avellaneda & Sasha Stoikov
track: Market Microstructure & Execution
section: Market Making
summary: How should quotes balance fill probability, spread revenue, and inventory
  risk?
---

## Why?

How should quotes balance fill probability, spread revenue, and inventory risk?

## Who?

Avellaneda and Stoikov, High-Frequency Trading in a Limit Order Book (2008).

## How?

Assume $dS_t=\sigma dW_t$, exponential fill intensity $\Lambda(\delta)=ae^{-k\delta}$, and exponential utility of terminal marked-to-market wealth. A familiar approximate rule is:

$$r_t=S_t-q_t\gamma\sigma^2(T-t),$$

$$s_t=\gamma\sigma^2(T-t)+\frac2\gamma\log(1+\gamma/k),\qquad B_t=r_t-s_t/2,\quad A_t=r_t+s_t/2.$$

## So what?

Quote center steers inventory; width controls the trade-off between revenue and fills. These are approximate quotes, not a universal exact solution. The baseline omits explicit adverse selection and queue priority and does not force terminal liquidation.

## References

[Avellaneda and Stoikov, High-Frequency Trading in a Limit Order Book (2008).](https://math.nyu.edu/inmemoriam/avellaneda/HighFrequencyTrading.pdf)

