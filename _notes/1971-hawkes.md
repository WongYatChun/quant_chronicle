---
title: Hawkes Processes — Event Clustering
year: 1971
authors: Alan Hawkes; financial applications by many researchers
track: Market Microstructure & Execution
section: LOB Modeling
summary: How can recent events change the probability of further events?
---

## Why?

How can recent events change the probability of further events?

## Who?

Hawkes introduced self-exciting processes in 1971. Bacry, Mastromatteo and Muzy (2015) review finance applications.

## How?

For event types $i,j$, the conditional intensity is:

$$\lambda_i(t)=\mu_i+\sum_j\int_{-\infty}^t\phi_{ij}(t-s)dN_j(s).$$

In one dimension with $\phi(u)=ae^{-bu}$, the branching ratio is $n=a/b$. For $n<1$, stationary mean intensity is $\bar\lambda=\mu/(1-n)$.

## So what?

Models clustering and cross-excitation of trades, cancellations, and price events. In the nonnegative linear multivariate case, stability requires the integrated-kernel matrix to have spectral radius below one. Excitation is statistical dependence, not proof of causality.

## References

[Hawkes introduced self-exciting processes in 1971. Bacry, Mastromatteo and Muzy (2015) review finance applications.](https://arxiv.org/abs/1502.04592)

