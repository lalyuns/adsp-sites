---
created: 2026-05-21
aliases:
  - "DFT complexity"
  - "convolution complexity"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "complexity"
  - "fft"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_016.png"
---

# Complexity of DFT and convolution

直接 $N$-point DFT 是 $O(N^2)$；FFT 後約為 $O(N\log N)$。Convolution 可用 FFT 轉成三次 DFT/IDFT 加 pointwise multiplication，因此長序列 convolution 常能從 quadratic 變成 near-linear-log。

這是 [[Fast algorithm design]] 的核心 tradeoff：用 transform overhead 換掉大量 direct convolution operations。

## 講義截圖

![Complexity summary](assets/adsp/ADSP_Write6_p016_complexity_summary.png)

