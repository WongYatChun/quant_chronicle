---
title: Hasbrouck — Trade Informativeness
year: 1991
authors: Joel Hasbrouck
track: Market Microstructure & Execution
section: Information from Trading Costs
summary: How much does an unexpected trade change prices after all lagged responses?
---

## Why?

How much does an unexpected trade change prices after all lagged responses?

## Who?

Hasbrouck, Measuring the Information Content of Stock Trades (1991).

## How?

A simplified VAR jointly models midpoint changes and signed flow:

$$z_t=(\Delta m_t,x_t)^\top,\qquad z_t=\sum_{k=1}^pA_kz_{t-k}+u_t.$$

With a trade shock identified using timing restrictions, let $\psi_h$ be its response in $\Delta m_{t+h}$. Then $I(H)=\sum_{h=0}^H\psi_h$ measures cumulative price response.

## So what?

The long-run response of a trade innovation is an information measure under the identification assumptions. It separates predictable trading activity from surprises; persistent response alone does not prove mechanical causality.

## References

[Hasbrouck, Measuring the Information Content of Stock Trades (1991).](https://doi.org/10.1111/j.1540-6261.1991.tb03749.x)

