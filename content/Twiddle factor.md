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

Twiddle factor 通常寫成

$$
W_N^k=e^{-j2\pi k/N}.
$$

它不是額外發明的係數，而是 DFT kernel $W_N^{kn}$ 在分解 index 後留下來的 phase correction。當 [[Cooley-Tukey FFT]] 把 $N$-point DFT 拆成 smaller DFTs，子問題之間必須用 twiddle factors 接合，否則相位會不對。

你可以把 twiddle factor 看成旋轉：乘上 $W_N^k$ 等於在 complex plane 上轉一個角度。這裡需要 [[Complex numbers for DSP]] 和 [[Euler formula]] 的直覺。

和 [[Butterfly computation]] 的關係：butterfly 負責加減重用，twiddle factor 負責 stage 之間的 phase alignment。


## 講義截圖
![Cooley-Tukey decomposition](assets/adsp/ADSP_Write6_p022_cooley_tukey.png)
