---
created: 2026-05-21
aliases:
  - "FFT"
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
  - "ADSP_Write6/page_016.png"
---

# Fast Fourier transform

FFT 是 DFT 的快速演算法家族，把 $O(N^2)$ 的 DFT 降到約 $O(N\log N)$。重點不是改變 DFT 定義，而是利用 factorization、symmetry、twiddle factors 重排計算。

常見版本有 [[Cooley-Tukey FFT]], [[Radix-4 FFT]], [[Prime factor FFT]]。

## 講義截圖

![Cooley-Tukey decomposition](assets/adsp/ADSP_Write6_p022_cooley_tukey.png)

![Complexity summary](assets/adsp/ADSP_Write6_p016_complexity_summary.png)

