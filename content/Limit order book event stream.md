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

因此自然模型是 marked point process。

## ADSP Course Connection

這篇是報告的 signal representation note。ADSP 通常從 regular samples $x[n]$ 開始，但 LOB 是 irregular event data；因此要用 [[Conditional intensity]] 取代 amplitude，用 [[Hawkes kernel matrix]] 取代 ordinary filter response。

## Mathematical Statistics Connection

event time model 需要 point-process probability；mark model 需要 [[Conditional distribution]]；若要估參數，需要 [[Likelihood function]]。

## Links

- [[Hawkes process limit order book project]]
- [[Conditional intensity]]
- [[Multivariate Hawkes process]]
- [[Marked Hawkes process]]
- [[Hawkes process as event-domain filtering]]
- [[Conditional distribution]]
- [[Likelihood function]]
