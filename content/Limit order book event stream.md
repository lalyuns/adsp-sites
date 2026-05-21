---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "market-microstructure"
  - "hawkes-process"
---

# Limit order book event stream

Limit order book (LOB) 可以看成 market events 的 timestamped sequence，而不是固定取樣的 price time series。每個 event 至少包含：

- time $t_n$；
- type $k_n$，例如 limit order、market order、cancel、bid side、ask side；
- mark $v_n$，例如 order size 或 volume。

因此自然模型是 marked point process。若把資料硬切成每秒或每分鐘的 bars，會遺失 event clustering、order flow imbalance、queue reaction 等 microstructure 資訊。[[Hawkes process limit order book project]] 的核心就是直接在 event time 上建模 [[Conditional intensity]]、[[Multivariate Hawkes process]] 的 event-type interaction，以及 [[Marked Hawkes process]] 的 order-size marks。
