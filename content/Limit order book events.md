---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "project-concept"
  - "limit-order-book"
---

# Limit order book events

Limit order book events 包含 limit orders、market orders、cancelations，通常還分 bid/ask side，並帶有 price/volume。把 LOB 看成 [[Limit order book event stream]] 後，資料不再是固定間隔取樣的 price sequence，而是 timestamped events。

## ADSP Course Connection

這篇負責把金融資料翻譯成 signal representation。ADSP 報告中不要從交易制度細節開始，而要先說：LOB events 是 irregular multichannel event signal，因此適合用 [[Multivariate Hawkes process]] 和 [[Marked Hawkes process]]。

## Mathematical Statistics Connection

事件類型是 categorical mark，order size 是 numerical mark；兩者都可放進 [[Conditional distribution]]。事件到達時間則由 [[Conditional intensity]] 描述。

## Links

- [[Limit order book event stream]]
- [[Conditional intensity]]
- [[Multivariate Hawkes process]]
- [[Marked Hawkes process]]
- [[Hawkes process limit order book project]]
- [[Conditional distribution]]
