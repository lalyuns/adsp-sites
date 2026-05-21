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
G_{ij}=\int_0^\infty \phi_{ij}(u)\,du.
$$

穩定條件通常寫成

$$
\rho(G)<1.
$$

## ADSP Course Connection

這是 Hawkes 版本的 stability condition。ADSP 中 filter/system 也會問 memory 是否 decay、系統是否穩定；Hawkes 用 kernel integral matrix 的 spectral radius 表示整體 excitation 會不會爆炸。這連到 [[Eigenvalues and eigenvectors]] 與 [[Matrix diagonalization for transforms]]。

## Mathematical Statistics Connection

branching ratio 是 expectation-level interpretation：一個 event 平均誘發幾個後代 event。這需要 [[Expectation]] 的直覺，也和 stochastic process 的 stationarity 有關。

## Links

- [[Conditional intensity]]
- [[Hawkes kernel matrix]]
- [[Multivariate Hawkes process]]
- [[Eigenvalues and eigenvectors]]
- [[Matrix diagonalization for transforms]]
- [[Expectation]]
