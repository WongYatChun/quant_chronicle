---
title: Order-Flow Imbalance — Supply and Demand at the Quotes
year: 2014
authors: Rama Cont, Arseniy Kukanov & Sasha Stoikov
track: Market Microstructure & Execution
section: LOB Modeling
summary: Why does signed trade volume miss important book changes?
---

## Why?

Why does signed trade volume miss important book changes?

## Who?

Cont, Kukanov and Stoikov, The Price Impact of Order Book Events (2014).

## How?

For event $n$, best prices are $b_n,a_n$ and displayed quantities $q_n^b,q_n^a$. Define:

$$e_n=\mathbf1_{b_n\ge b_{n-1}}q_n^b-\mathbf1_{b_n\le b_{n-1}}q_{n-1}^b-\mathbf1_{a_n\le a_{n-1}}q_n^a+\mathbf1_{a_n\ge a_{n-1}}q_{n-1}^a.$$

$$OFI=\sum_ne_n,\qquad \Delta m\approx\beta\,OFI+\varepsilon.$$

## So what?

OFI incorporates limit additions, cancellations, and executions at the best quotes. The empirical contemporaneous relationship is not automatically an executable forecast. Sensitivity depends on depth.

## References

[Cont, Kukanov and Stoikov, The Price Impact of Order Book Events (2014).](https://arxiv.org/abs/1011.6402)

