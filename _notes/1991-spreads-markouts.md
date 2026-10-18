---
title: Spreads & Markouts — Measuring Adverse Selection
year: 1991
authors: Measurement note; Lee & Ready for trade signing
track: Market Microstructure & Execution
section: Information from Trading Costs
summary: How much of the paid spread survives subsequent price adjustment?
---

## Why?

How much of the paid spread survives subsequent price adjustment?

## Who?

This is a synthesis of standard measurements, not a single invention. Lee and Ready (1991) provide an influential trade-signing method.

## How?

Let $\epsilon=+1$ for buyer-initiated trades and $-1$ for seller-initiated trades; $P$ is execution price, $m_t$ the pre-trade midpoint. Define dollar-per-share, full-spread measures:

$$ES=2\epsilon(P-m_t),\quad RS_h=2\epsilon(P-m_{t+h}),\quad PI_h=2\epsilon(m_{t+h}-m_t).$$

$$ES=RS_h+PI_h.$$

## So what?

A liquidity supplier’s gross markout per share is RS/2. It is not net profit. The horizon, trade sign, quote timestamp, and fee treatment must be specified. PI is a signed price response, not automatically a causal adverse-selection estimate. The year labels the trade-signing reference.

## References

[This is a synthesis of standard measurements, not a single invention. Lee and Ready (1991) provide an influential trade-signing method.](https://doi.org/10.1111/j.1540-6261.1991.tb02683.x)

