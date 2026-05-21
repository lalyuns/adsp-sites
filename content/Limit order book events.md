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

這個觀點自然連到 [[Multivariate Hawkes process]]：不同 event type 之間可能互相激發；也連到 [[Marked Hawkes process]]：order size 或 volume 是 mark，不能只被當成普通欄位丟掉。
