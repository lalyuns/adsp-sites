---
created: 2026-05-21
aliases:
  - "Cooley Tukey algorithm"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "fft"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_022.png"
---

# Cooley-Tukey FFT

Cooley-Tukey FFT 把 $N$-point DFT 分成兩個 $N/2$-point DFT 加上 twiddle factors。當 $N=2^k$ 時，可以遞迴分解成 butterfly network。

它的核心分解是把 even-indexed samples 與 odd-indexed samples 分開。

## 講義截圖

![Cooley-Tukey decomposition](assets/adsp/ADSP_Write6_p022_cooley_tukey.png)

