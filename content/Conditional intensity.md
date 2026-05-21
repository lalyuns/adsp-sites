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

# Conditional intensity

Conditional intensity 是 point process 的「瞬時發生率」：

$$
\lambda_i(t)dt \approx P(dN_i(t)=1 \mid \mathcal{H}_t).
$$

它不是固定常數 rate，而是 depends on event history。[[Hawkes process]] 的特色是 past events 會提高 future intensity：

$$
\lambda_i(t)=\mu_i+\sum_j\int_0^t \phi_{ij}(t-s)dN_j(s).
$$

直覺：$\mu_i$ 是 background event rate；$\phi_{ij}$ 是 type $j$ event 對 type $i$ event 的 aftershock-like excitation。把所有 $\phi_{ij}$ 放在一起就是 [[Hawkes kernel matrix]]；把 kernel 積分後看平均 offspring 數，就連到 [[Hawkes branching ratio]]。在 [[Hawkes process limit order book project]] 中，$\lambda_i(t)$ 是把 LOB event clustering 寫成數學模型的入口。
