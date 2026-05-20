---
created: 2026-05-21
aliases:
  - "雙線性轉換"
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
  - "ADSP_Write1/page_036.png"
---

# Bilinear transform

Bilinear transform 用

$$s=c\frac{1-z^{-1}}{1+z^{-1}}$$

把 analog Laplace-domain filter 映到 digital Z-domain filter。優點是 no aliasing；缺點是 high-frequency warping，所以設計時常要 pre-warping。

它需要 [[Complex numbers for DSP]]、[[Z-transform]] 與 unit circle 的直覺。

## 講義截圖

![Bilinear transform mapping](assets/adsp/ADSP_Write1_p036_bilinear_transform.png)

