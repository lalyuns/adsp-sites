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

Marked [[Hawkes process]] 在 event time/type 之外加入 mark，例如 [[Limit order book event stream]] 裡的 order size，或 seismic catalog 裡的 earthquake magnitude。

它回答兩個問題：事件何時發生，由 [[Conditional intensity]] 描述；事件帶著什麼大小或屬性，由 mark distribution 描述。若 mark distribution depends on history，就連到 [[History dependent mark distribution]]；若用 neural encoder 學這個 dependence，就連到 [[Neural marked Hawkes process]]。
