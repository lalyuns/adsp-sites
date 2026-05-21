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

這篇是 Hawkes project 的 theoretical backbone。它的重點是：不用先假設 kernel 是 exponential，而是從 second-order statistics 反推出 kernel structure。

## Method In Words

Multivariate [[Hawkes process]]：

$$
\lambda_i(t)=\mu_i+\sum_j\int_0^t \phi_{ij}(t-s)dN_j(s).
$$

$\phi_{ij}$ 是 type $j$ event 對 type $i$ future intensity 的 influence function。Bacry and Muzy 把 jumps covariance/correlation 與 $\phi_{ij}$ 連成 Wiener-Hopf integral equations，因此可做 [[Nonparametric Hawkes estimation]]。

報告中不要截論文方程式圖。應直接寫上式，然後用文字說：second-order statistics 在這裡不是描述性統計，而是 kernel identification 的工具。

## What It Supports

- 幫 [[Hawkes kernel matrix]] 提供理論來源。
- 解釋為何 calibrated kernels 可被解讀為 market event interaction。
- 和 neural model 形成對照：這篇重 interpretability；[[Neural marked Hawkes process for LOB]] 重 flexible prediction。
