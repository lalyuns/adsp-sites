---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "hawkes-process"
  - "paper-note"
---

# Bacry Muzy 2015 Hawkes second-order statistics

這篇是 Hawkes project 的 theoretical backbone。它的重點是：不先假設 kernel 是 exponential，而是從 second-order statistics 反推出 kernel structure。

## Method In Words

Multivariate [[Hawkes process]]：

$$
\lambda_i(t)=\mu_i+\sum_j\int_0^t \phi_{ij}(t-s)dN_j(s).
$$

$\phi_{ij}$ 是 type $j$ event 對 type $i$ future intensity 的 influence function。Bacry and Muzy 把 jumps covariance/correlation 與 $\phi_{ij}$ 連成 Wiener-Hopf integral equations，因此可做 [[Nonparametric Hawkes estimation]]。

## ADSP Course Connection

這篇最適合拿來證明 Hawkes 題目和 ADSP 有關。它用 second-order statistics 反推 event-response kernel，形式上接近 random signal processing 的 correlation/inverse problem。Wiener-Hopf 這個關鍵字也能自然連到 [[Wiener filter]]，但報告應講「second-order thinking」而不是硬說它在做傳統 Wiener filtering。

## Mathematical Statistics Connection

second-order statistics 連到 [[Expectation]] 與 [[Covariance matrix]]。若把 kernel estimation 看成參數/函數估計，也能和 [[Maximum likelihood estimator]] 作對照。

## What It Supports

- 幫 [[Hawkes kernel matrix]] 提供理論來源。
- 解釋為何 calibrated kernels 可被解讀為 market event interaction。
- 和 neural model 形成對照：這篇重 interpretability；[[Neural marked Hawkes process for LOB]] 重 flexible prediction。

## Links

- [[Hawkes process as event-domain filtering]]
- [[Nonparametric Hawkes estimation]]
- [[Hawkes kernel matrix]]
- [[Conditional intensity]]
- [[Wiener filter]]
- [[Probability for random signals]]
- [[Expectation]]
- [[Covariance matrix]]
- [[Maximum likelihood estimator]]
