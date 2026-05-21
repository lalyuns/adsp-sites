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

# Hawkes branching ratio

Hawkes branching ratio 衡量一個 event 平均會觸發多少 offspring events。單變量時常寫成

$$
\eta=\int_0^\infty \phi(u)\,du.
$$

$\eta<1$ 時 process 穩定；$\eta$ 越接近 1，event clustering 越強。多變量時把每個 kernel integral 組成 matrix

$$
G_{ij}=\int_0^\infty \phi_{ij}(u)\,du,
$$

穩定條件通常寫成 spectral radius $\rho(G)<1$。報告中可用這個概念把 [[Hawkes kernel matrix]] 的視覺結果連到數學條件，而不是只說 kernel 看起來很大或很小。
