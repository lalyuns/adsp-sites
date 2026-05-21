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

# Market impact simulation

Market impact simulation 問一筆或一串 trades 如何改變 price/quote state。放在 [[Hawkes process limit order book project]] 裡，它不是主模型，而是用來檢查 [[Limit order book event stream]] simulator 是否產生合理的 market response。

若只建模 event count，模型只能說事件何時出現；若加入 [[Compound Hawkes process]] 或 [[Marked Hawkes process]] 的 order size，才有機會討論 volume-driven impact。報告中可把它當成 evaluation angle：模型是否能重現 concave impact、order clustering、以及 liquidity recovery。
