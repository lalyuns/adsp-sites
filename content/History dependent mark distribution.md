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

在 LOB 中，order size 不是獨立噪音。它可能受近期 volatility、order-flow imbalance、queue depletion、前一串 market orders 影響。傳統 marked Hawkes 常用較簡單的 parametric mark distribution；[[Neural marked Hawkes process]] 的動機是用 neural encoder 把 $\mathcal{H}_t$ 壓成 state，再預測 mark distribution。

這個 note 可放在報告中銜接 compound Hawkes 與 neural [[Marked Hawkes process|marked Hawkes]]：前者讓 size 進入模型，後者讓 size distribution 更彈性地 depends on history。
