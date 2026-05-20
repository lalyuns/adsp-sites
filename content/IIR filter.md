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

IIR filter 是 infinite impulse response filter，常由 analog filter 轉成 digital filter，或由 difference equation recursion 產生。它可能用較少係數達到 sharp response，但需要注意 stability。

常見轉換有 impulse invariance、step invariance、[[Bilinear transform]]。

## 講義截圖

![Digital filter classification](assets/adsp/ADSP_Write1_p042_filter_classification.png)

![Bilinear transform mapping](assets/adsp/ADSP_Write1_p036_bilinear_transform.png)

