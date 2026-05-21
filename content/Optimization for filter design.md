---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Meta knowledge]]"
tags:
  - "adsp"
  - "meta-knowledge"
  - "prerequisite"
---

# Optimization for filter design

Filter design 裡的 optimization 可以分成三種語言：

- least squares / MSE：最小化平均平方誤差，連到 [[Least MSE FIR design]]。
- minimax / Chebyshev：最小化最大誤差，連到 [[Minimax FIR design]] 和 [[Remez exchange algorithm]]。
- weighted error：用權重表示哪個頻帶比較重要，連到 [[Weighted approximation error]]。

你已經修過微積分，所以可以把它想成「找一組係數讓 objective 最小」。進階點在於 objective 不是單一變數函數，而是整個頻帶上的函數誤差。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 [[Expectation|expectation]]，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、[[Cepstrum|cepstrum]] prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、[[Quantization|quantization]]、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
