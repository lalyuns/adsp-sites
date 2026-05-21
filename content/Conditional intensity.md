---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "meta-knowledge"
  - "hawkes-process"
---

# Conditional intensity

Conditional intensity 是 point process 的「history-conditioned instantaneous event rate」：

$$
\lambda_i(t)dt \approx P(dN_i(t)=1 \mid \mathcal{H}_t).
$$

它不是固定常數 rate，而是 depends on event history。Hawkes process 的特色是 past events 會提高 future intensity：

$$
\lambda_i(t)=\mu_i+\sum_j\int_0^t \phi_{ij}(t-s)dN_j(s).
$$

直覺：$\mu_i$ 是 background event rate；$\phi_{ij}$ 是 type $j$ event 對 type $i$ event 的 aftershock-like excitation。把所有 $\phi_{ij}$ 放在一起就是 [[Hawkes kernel matrix]]。

## ADSP Course Connection

在 ADSP 語言中，$\lambda_i(t)$ 是 event-stream 的 time-varying activity representation。它扮演的角色有點像 signal envelope 或 detector statistic，但對象不是 amplitude，而是 event arrival rate。kernel convolution 則連到 [[Convolution]] 和 random-signal filtering。

## Mathematical Statistics Connection

這個概念是 [[Conditional expectation]] 和 [[Conditional distribution]] 的連續時間版本：不是問 unconditional event probability，而是問在 $\mathcal{H}_t$ 已知時，下一瞬間事件發生的 rate。

## Links

- [[Hawkes process]]
- [[Hawkes kernel matrix]]
- [[Hawkes branching ratio]]
- [[Probability for random signals]]
- [[Convolution]]
- [[Conditional expectation]]
- [[Conditional distribution]]
