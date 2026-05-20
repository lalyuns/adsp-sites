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

# Fast algorithm prerequisite map

Fast algorithm 的前置觀念不是高等微積分，而是 index decomposition 和矩陣分解。

- index decomposition：把 $n$ 或 $k$ 寫成多個 smaller indices。
- symmetry/periodicity：利用 $W_N^{k+N}=W_N^k$ 等重複。
- sparse factorization：把 dense transform matrix 拆成 sparse stages。
- complexity counting：分清楚 multiplication、addition、memory permutation。

這張圖連到 [[Fast Fourier transform]]、[[Butterfly computation]]、[[Cooley-Tukey FFT]]、[[Radix-4 FFT]]、[[Prime factor FFT]]。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 expectation，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、cepstrum prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、quantization、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
