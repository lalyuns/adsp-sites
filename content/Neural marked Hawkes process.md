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

## ADSP Course Connection

它是 Hawkes 報告裡的 flexible representation model。和 classical kernel model 相比，它較不像可解釋 filter，但仍是在做 signal prediction：用過去 event history 預測 future event behavior。

## Mathematical Statistics Connection

它的 mark head 仍是 [[Conditional distribution]]；training objective 通常仍和 [[Likelihood function]] 有關。neural network 只是讓 conditional law 的 parameterization 更有彈性。

## Links

- [[Neural marked Hawkes process for LOB]]
- [[Marked Hawkes process]]
- [[History dependent mark distribution]]
- [[Conditional intensity]]
- [[Conditional distribution]]
- [[Likelihood function]]
- [[Hawkes model comparison]]
