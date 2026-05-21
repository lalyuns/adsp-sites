---
created: 2026-05-21
aliases:
  - "finite impulse response"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "fir"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_042.png"
  - "ADSP_Write1/page_045.png"
---

# FIR filter

FIR filter 的 impulse response 長度有限，所以一定 BIBO stable，也容易做 [[Linear phase FIR filter|linear phase]]。代價是要達到尖銳 transition 通常需要較長 filter length。

連結：[[Optimization for filter design]]、[[Frequency response]]。


## 講義截圖
![Digital filter classification](assets/adsp/ADSP_Write1_p042_filter_classification.png)

![Linear phase FIR impulse response](assets/adsp/ADSP_Write1_p045_linear_phase_fir.png)
