---
created: 2026-05-21
aliases:
  - "equalizer"
  - "等化器"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Popular filters]]"
tags:
  - "adsp"
  - "filters"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_031.png"
---

# Equalizer filter

Equalizer 用來補償 channel/system effect。若 $y[n]=x[n]*k[n]$，frequency domain 中 $Y(F)=X(F)K(F)$，理想 equalizer 是

$$H(F)=\frac{1}{K(F)}.$$

但當 $K(F)$ 很接近 0 時，noise 會被放大，所以實務上會結合 [[Wiener filter]] 或 regularization。

## 講義截圖

![Equalizer filter](assets/adsp/ADSP_Write3_p031_equalizer.png)

