---
created: 2026-05-21
aliases:
  - "frequency response"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "filters"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_042.png"
---

# Frequency response

Frequency response $H(F)$ 描述 LTI system 對不同 frequency component 的增益與相位。若 $y[n]=x[n]*h[n]$，則

$$Y(F)=X(F)H(F).$$

Filter design 的目標通常是讓實作得到的 $R(F)$ 接近 desired response $H_d(F)$。因此它連到 [[Convolution]], [[FIR filter]], [[IIR filter]], [[Least MSE FIR design]], [[Minimax FIR design]]。

## 講義截圖

![Digital filter classification](assets/adsp/ADSP_Write1_p042_filter_classification.png)

