---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "project-concept"
  - "hawkes-process"
---

# Multivariate Hawkes process

Multivariate Hawkes process 有多個 event types，每個 type 都有自己的 [[Conditional intensity]]：

$$
\lambda_i(t)=\mu_i+\sum_{j=1}^{K}\int_0^t \phi_{ij}(t-s)dN_j(s).
$$

它比單變量 [[Hawkes process]] 多出的重點是 cross-excitation：type $j$ 的 event 可以改變 type $i$ 的 future rate。

## ADSP Course Connection

這是 multichannel event-stream model。若把每個 event type 當成一個 channel，$\phi_{ij}$ 就像 channel $j$ 到 channel $i$ 的 impulse response。這和多輸入多輸出系統、cross-correlation、[[Matrix diagonalization for transforms]] 的「矩陣描述 cross-channel coupling」有相同味道。

## Mathematical Statistics Connection

估計 $\phi_{ij}$ 需要從多類 event data 推回 dependence structure，會用到 [[Covariance matrix]]、[[Likelihood function]]，以及 [[Maximum likelihood estimator]] 的估計觀點。

## Links

- [[Hawkes process]]
- [[Conditional intensity]]
- [[Hawkes kernel matrix]]
- [[Hawkes branching ratio]]
- [[Limit order book event stream]]
- [[Covariance matrix]]
- [[Likelihood function]]
