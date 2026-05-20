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

FFT 是一族快速計算 DFT 的演算法，不是一個新的 transform。它的輸出仍然是 [[Discrete Fourier transform]] 的 $X[k]$；差別只在計算方式。

最常見的 [[Cooley-Tukey FFT]] 利用 $N=N_1N_2$ 把一個 $N$-point DFT 拆成 smaller DFTs。拆完後需要三種東西把結果接回來：

- sub-DFTs：較小的 DFT problem。
- [[Twiddle factor]]：補上原本 DFT kernel 中跨子問題的 phase。
- permutation/index mapping：重新安排 input/output 順序。

講義的 complexity summary 是這章的核心：直接 DFT 是 $O(N^2)$，FFT 約 $O(N\log N)$。讀 FFT 圖時先找 [[Butterfly computation]]，它是每個 stage 的基本單元；再看 stage 如何串成 radix-2、[[Radix-4 FFT]] 或 [[Prime factor FFT]]。


## 講義截圖
![Cooley-Tukey decomposition](assets/adsp/ADSP_Write6_p022_cooley_tukey.png)

![Complexity summary](assets/adsp/ADSP_Write6_p016_complexity_summary.png)
