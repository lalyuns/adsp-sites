---
created: 2026-05-21
aliases:
  - "twiddle factor"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fast algorithms]]"
  - "[[Fourier analysis]]"
tags:
  - "adsp"
  - "fft"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_022.png"
---

# Twiddle factor

Twiddle factor 是 DFT/FFT 中反覆出現的旋轉因子

$$W_N^m=e^{-j2\pi m/N}.$$

FFT 的效率來自大量重複使用與簡化這些 factors，例如 $W_N^{m+N/2}=-W_N^m$。理解它需要 [[Euler formula]] 與 [[Complex numbers for DSP]]。

## 講義截圖

![Cooley-Tukey decomposition](assets/adsp/ADSP_Write6_p022_cooley_tukey.png)

