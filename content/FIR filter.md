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

FIR filter 是 finite impulse response filter：$h[n]$ 只在有限個 sample 非零。優點是容易計算、總是 BIBO stable；缺點是如果要逼近很尖銳的 ideal response，filter length 可能很長。

FIR 是 Write1/Write2 的主角，設計方法包括 [[Least MSE FIR design]], [[Minimax FIR design]], [[Frequency sampling FIR design]]。

## 講義截圖

![Digital filter classification](assets/adsp/ADSP_Write1_p042_filter_classification.png)

![Linear phase FIR impulse response](assets/adsp/ADSP_Write1_p045_linear_phase_fir.png)

