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

# Marked Hawkes process

Marked Hawkes process 在 event time/type 之外加入 mark，例如 [[Limit order book event stream]] 裡的 order size，或 seismic catalog 裡的 earthquake magnitude。

可寫成一個 timing model 加上一個 mark model：

$$
\lambda_i(t,v)=\lambda_i(t)p_i(v\mid \mathcal{H}_t).
$$

## ADSP Course Connection

這像是把 event detection 和 feature/amplitude modeling 合在一起。對 LOB 來說，只看 event count 不足以描述 signal；order size mark 讓模型可以連到 volume、impact、以及 [[Market impact simulation]]。

## Mathematical Statistics Connection

mark model 本質上是 [[Conditional distribution]]：在 event type/time/history 已知時，mark $v$ 的分布是什麼？若用 likelihood fit，會連到 [[Likelihood function]]。

## Links

- [[Hawkes process]]
- [[Conditional intensity]]
- [[History dependent mark distribution]]
- [[Compound Hawkes process]]
- [[Neural marked Hawkes process]]
- [[Limit order book event stream]]
- [[Conditional distribution]]
- [[Likelihood function]]
