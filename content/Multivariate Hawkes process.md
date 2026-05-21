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

Multivariate Hawkes process 有多個 event types，每個 type 都有自己的 [[Conditional intensity]]。它比單變量 [[Hawkes process]] 多出的重點是 cross-excitation：type $j$ 的 event 可以改變 type $i$ 的 future rate。

在 [[Hawkes process limit order book project]] 中，event type 可代表 bid/ask、limit/market/cancel 等 [[Limit order book event stream|LOB]] actions。所有 pairwise influence 放進 [[Hawkes kernel matrix]]，再用 [[Hawkes branching ratio]] 檢查 excitation 是否穩定。
