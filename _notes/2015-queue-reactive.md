---
title: Queue-Reactive Models — State-Dependent Order Flow
year: 2015
authors: Weibing Huang, Charles-Albert Lehalle & Mathieu Rosenbaum
track: Market Microstructure & Execution
section: LOB Modeling
summary: How does current queue depth affect arrivals and removals?
---

## Why?

How does current queue depth affect arrivals and removals?

## Who?

Huang, Lehalle and Rosenbaum, Simulating and Analyzing Order Book Data: The Queue-Reactive Model (2013 preprint; 2015 publication).

## How?

Between reference-price changes, queue sizes form a Markov state $Q_t$. Event intensities depend on that state:

$$\lambda_e(t)=\lambda_e(Q_{t-}),\qquad \widehat\lambda_e(q)=\frac{\text{events of type }e\text{ in state }q}{\text{time spent in state }q}.$$

## So what?

The framework models depletion and replenishment and supports execution simulation. A separate mechanism handles reference-price changes. Individual-order fills additionally require queue-priority and cancellation-location assumptions.

## References

[Huang, Lehalle and Rosenbaum, Simulating and Analyzing Order Book Data: The Queue-Reactive Model (2013 preprint; 2015 publication).](https://arxiv.org/abs/1312.0563)

