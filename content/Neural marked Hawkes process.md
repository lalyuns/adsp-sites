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
  - "neural-model"
---

# Neural marked Hawkes process

Neural marked Hawkes process 用 neural state 取代手工指定的 kernel shape 或 mark distribution。它仍然圍繞 [[Conditional intensity]]，但把 history $\mathcal{H}_t$ 壓成 hidden state，再預測下一個 event time/type 與 mark。

在 [[Hawkes process limit order book project]] 中，它的角色是 advanced extension：和 [[Hawkes kernel matrix]] 相比，neural model 較難解釋；和 [[Marked Hawkes process]] 相比，它更能處理 [[History dependent mark distribution]]。
