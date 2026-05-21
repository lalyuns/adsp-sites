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

# Compression math prerequisites

Compression 需要三種數學直覺：

1. Transform coding：用 DCT/KLT/PCA 把 energy 集中。
2. Quantization：用有限 levels 近似係數，產生 distortion。
3. Entropy coding：利用符號機率分布縮短平均碼長。

JPEG 是這三者的組合。看 [[JPEG compression]] 時，不要把 pipeline 當步驟背誦；要問每一步是在移除 spatial redundancy、perceptual irrelevance，還是 statistical redundancy。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 [[Expectation|expectation]]，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、[[Cepstrum|cepstrum]] prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、[[Quantization|quantization]]、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
