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

# History dependent mark distribution

History dependent mark distribution 指 mark 的分布不只依賴 event type，也依賴過去完整事件序列：

$$
p(v_{n+1}\mid k_{n+1},t_{n+1},\mathcal{H}_{t_{n+1}}).
$$

在 LOB 中，order size 不是獨立噪音。它可能受近期 volatility、order-flow imbalance、queue depletion、前一串 market orders 影響。

## ADSP Course Connection

這是 event-stream 版本的 adaptive/statistical signal modeling：representation 不是固定特徵，而是根據 history state 改變。它和 [[Probability for random signals]] 共享同一個觀點：signal behavior 要用 distribution 和 conditioning 描述。

## Mathematical Statistics Connection

核心是 [[Conditional distribution]]。若模型用 neural network 產生 distribution parameter，就仍然是在估計 conditional law，不只是做黑箱分類。

## Links

- [[Marked Hawkes process]]
- [[Neural marked Hawkes process]]
- [[Conditional intensity]]
- [[Conditional distribution]]
- [[Probability for random signals]]
