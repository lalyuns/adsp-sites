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

# Cepstrum prerequisite map

Cepstrum 需要四個前置觀念：

- [[Convolution]]：source 和 filter 常以 convolution 混合。
- [[Discrete-time Fourier transform]]：convolution 進頻域變 multiplication。
- complex log：multiplication 取 log 變 addition。
- phase handling：如果要 inverse，phase unwrapping 和 minimum phase 會變重要。

讀 [[Cepstrum]] 和 [[Complex cepstrum]] 時，把流程寫成 $x*h \rightarrow XH \rightarrow \log X + \log H \rightarrow \hat{x}+\hat{h}$，會比直接看方塊圖更清楚。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 [[Expectation|expectation]]，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、cepstrum prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、[[Quantization|quantization]]、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
