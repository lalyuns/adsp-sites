---
created: 2026-05-21
aliases:
  - "DFT"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fourier analysis]]"
tags:
  - "adsp"
  - "dft"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_075.png"
---

# Discrete Fourier transform

DFT 把有限長度、週期延拓的 sequence 轉成有限個 frequency bins：

$$X[m]=\sum_{n=0}^{N-1}x[n]e^{-j2\pi mn/N},\qquad x[n]=\frac1N\sum_{m=0}^{N-1}X[m]e^{j2\pi mn/N}.$$

在 sampled spectrum 中，第 $m$ 個 DFT bin 對應實際頻率 $f=m f_s/N$；若 $m>N/2$，通常解讀成負頻率或 folding 後的頻率。

## 講義截圖

![DFT samples of a sampled signal](assets/adsp/ADSP_Write1_p075_sampled_signal_spectrum.png)

