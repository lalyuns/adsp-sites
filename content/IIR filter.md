---
created: 2026-05-21
aliases:
  - "infinite impulse response"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "iir"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_042.png"
  - "ADSP_Write1/page_036.png"
---

# IIR filter

IIR filter 用 feedback 產生無限長 impulse response，常能用較低 order 達成 sharp response。風險是 stability 取決於 poles 是否在 unit circle 內，phase 通常也較難控制。

連結：[[Optimization for filter design]]、[[Frequency response]]。


## 講義截圖
![Digital filter classification](assets/adsp/ADSP_Write1_p042_filter_classification.png)

![Bilinear transform mapping](assets/adsp/ADSP_Write1_p036_bilinear_transform.png)
