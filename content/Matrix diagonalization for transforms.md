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

# Matrix diagonalization for transforms

很多 transform 的目的都是讓某個 operation 變 diagonal 或接近 diagonal。

- [[Discrete Fourier transform|DFT]] diagonalizes circular [[Convolution|convolution]]。
- KLT diagonalizes [[Covariance matrix|covariance matrix]]。
- PCA/SVD 把資料 energy 排序到主要方向。
- DCT 不是完全 data-adaptive，但對自然影像常接近 KLT 的 energy compaction。

「diagonal」代表各座標彼此 decoupled，計算和解讀都會簡化。這個 meta note 連到 [[Eigenvalues and eigenvectors]]、[[Singular value decomposition]]、[[Principal component analysis]]、[[Karhunen-Loeve transform]]、[[Discrete cosine transform]]。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 [[Expectation|expectation]]，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、[[Cepstrum|cepstrum]] prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、[[Quantization|quantization]]、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
