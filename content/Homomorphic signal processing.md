---
created: 2026-05-21
aliases:
  - "homomorphism"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Homomorphic processing]]"
tags:
  - "adsp"
  - "homomorphic"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_041.png"
---

# Homomorphic signal processing

Homomorphic 的關鍵 pipeline 是 convolution -> Fourier -> multiplication -> log -> addition。進入 cepstrum domain 後，source 和 filter 如果落在不同 quefrency range，就能用 lifter 分離。

連結：[[Cepstrum prerequisite map]]、[[Homomorphic signal processing]]。


## 講義截圖
![Homomorphic signal processing](assets/adsp/ADSP_Write3_p041_homomorphism.png)
