---
title: Almgren–Chriss — Execution Cost versus Risk
year: 2001
authors: Robert Almgren & Neil Chriss
track: Market Microstructure & Execution
section: Optimal Execution
summary: How quickly should a fixed position be liquidated?
---

## Why?

How quickly should a fixed position be liquidated?

## Who?

Almgren and Chriss, Optimal Execution of Portfolio Transactions (2000 manuscript; 2001 publication), following earlier dynamic execution work by Bertsimas and Lo.

## How?

In a simplified continuous-time liquidation model, $x_0=Q$, $x_T=0$, and $v_t=-\dot x_t$:

$$\min_x\int_0^T[\eta\dot x_t^2+\lambda\sigma^2x_t^2]dt.$$

$$x_t^*=Q\frac{\sinh(\kappa(T-t))}{\sinh(\kappa T)},\qquad \kappa=\sqrt{\lambda\sigma^2/\eta}.$$

## So what?

Temporary impact favors slower trading; inventory risk favors earlier trading. With no risk penalty, the schedule becomes uniform. Linear permanent impact is schedule-independent under standard assumptions. Implementation shortfall compares actual proceeds or expenditure with the decision-price benchmark and includes fees and unfinished-order opportunity cost when applicable.

## References

[Almgren and Chriss, Optimal Execution of Portfolio Transactions (2000 manuscript; 2001 publication), following earlier dynamic execution work by Bertsimas and Lo.](https://doi.org/10.21314/JOR.2001.041)

