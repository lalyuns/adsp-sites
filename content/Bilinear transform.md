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

Bilinear transform 用 $s=c(1-z^{-1})/(1+z^{-1})$ 把 analog filter 映到 digital filter，優點是不會 alias，缺點是 frequency warping，所以常要 prewarping。

連結：[[Optimization for filter design]]、[[Frequency response]]。


## 講義截圖
![Bilinear transform mapping](assets/adsp/ADSP_Write1_p036_bilinear_transform.png)
