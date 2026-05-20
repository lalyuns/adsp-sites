---
created: 2026-05-21
aliases:
  - "Z transform"
  - "Z 轉換"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fourier analysis]]"
  - "[[Filter design]]"
tags:
  - "adsp"
  - "z-transform"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_036.png"
---

# Z-transform

Z-transform 把 sequence 表成 $X(z)=\sum x[n]z^{-n}$，比 DTFT 多了 radius/ROC 資訊。它讓 poles/zeros、stability、causality、frequency response 可以在同一張 complex plane 上討論。

連結：[[ADSP notation survival guide]]、[[Spectral analysis workflow]]。


## 講義截圖
![Bilinear transform mapping](assets/adsp/ADSP_Write1_p036_bilinear_transform.png)
