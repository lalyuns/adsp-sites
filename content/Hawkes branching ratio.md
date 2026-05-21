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

穩定條件通常寫成 spectral radius $ho(G)<1$。這個 note 連接三件事：[[Conditional intensity]] 定義 instantaneous rate，[[Hawkes kernel matrix]] 描述 excitation direction，branching ratio 則把整體 excitation 強度壓成 stability condition。寫 [[Hawkes process limit order book project]] 時，可用它避免只用「kernel 看起來很大」這種模糊描述。
