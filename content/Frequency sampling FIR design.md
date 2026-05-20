---
created: 2026-05-21
aliases:
  - "frequency sampling method"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Filter design]]"
tags:
  - "adsp"
  - "fir"
source:
  - "[[ADSP Write2 FIR design details]]"
pages:
  - "ADSP_Write2/page_026.png"
---

# Frequency sampling FIR design

Frequency sampling method 先在頻域指定若干點的 $H[k]$，再 IDFT 得到 $h[n]$。它直觀但對 transition/ripple 的控制不如 Remez 精細。

連結：[[Optimization for filter design]]、[[Frequency response]]。


## 講義截圖
![Frequency sampling FIR method](assets/adsp/ADSP_Write2_p026_frequency_sampling_method.png)
