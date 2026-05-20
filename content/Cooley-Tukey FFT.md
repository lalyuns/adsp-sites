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

Cooley-Tukey FFT 的核心是 index decomposition。若 $N=N_1N_2$，就把原本的一個 $N$-point DFT 拆成兩層 smaller DFT，再用 [[Twiddle factor]] 和 permutation 合成。

直覺上，這是在改寫 DFT 的雙重 sum：原本 $n$ 和 $k$ 是單一 index，現在拆成兩個 index。拆開後，有些加總可以先做成小 DFT，有些 phase term 變成 diagonal twiddle matrix。

讀講義圖時，請不要只跟著箭頭走。先問：

- $N$ 被拆成哪些因子？
- input index 是 decimation in time 還是 decimation in frequency？
- twiddle factors 出現在兩層 DFT 的哪裡？
- output 是否需要 bit reversal 或其他 permutation？

這篇往下接 [[Radix-4 FFT]] 和 [[Prime factor FFT]]；往上回到 [[Fast Fourier transform]]。


## 講義截圖
![Cooley-Tukey decomposition](assets/adsp/ADSP_Write6_p022_cooley_tukey.png)
