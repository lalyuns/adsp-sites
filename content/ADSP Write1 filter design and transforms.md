---
created: 2026-05-21
aliases:
  - "ADSP Write1"
  - "Write1"
categories:
  - "[[Evergreen]]"
  - "[[Indexes]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Filter design]]"
type:
  - "[[MOCs]]"
status:
  - "[[Active]]"
tags:
  - "adsp"
  - "filter-design"
  - "transforms"
pages:
  - "ADSP_Write1/page_001.png-page_080.png"
---

# ADSP Write1 filter design and transforms

Write1 是 ADSP 的語言層：先把 signal 和 system 放到 transform domain，再把 filter design 寫成 approximation problem。

建議閱讀順序是：

1. [[Fourier transform family]] -> [[Discrete-time Fourier transform]] -> [[Discrete Fourier transform]]：釐清 CTFT/DTFT/DFT 的 domain 差別。這裡最容易混的是 continuous frequency $\omega$ 和 DFT bin $k$。
2. [[Normalized frequency]] -> [[Z-transform]] -> [[Unit circle and Z-transform]]：把 sampling frequency、unit circle、poles/zeros 和 frequency response 接起來。
3. [[Frequency response]] -> [[FIR filter]] / [[IIR filter]]：理解 filter 不是看係數本身，而是看它如何改變各頻率的 magnitude 和 phase。
4. [[Linear phase FIR filter]] -> [[Least MSE FIR design]] -> [[Minimax FIR design]] -> [[Remez exchange algorithm]]：從「想要什麼響應」走到「如何決定 FIR 係數」。

這份講義的重點不是把所有 Fourier 公式重背一次，而是建立後面幾份講義都會用的座標系。讀圖時先問：圖上是 time domain、frequency domain、Z-plane，還是 error curve？如果是 error curve，再問它對應 [[Weighted approximation error]]、$L_2$ least MSE，還是 $L_\infty$ minimax。

前置補洞：[[ADSP notation survival guide]]、[[Sampling and aliasing]]、[[Optimization for filter design]]。


## 講義截圖
![Fourier transform types](assets/adsp/ADSP_Write1_p022_fourier_transform_types.png)

![Digital filter classification](assets/adsp/ADSP_Write1_p042_filter_classification.png)

![Minimax FIR equiripple error](assets/adsp/ADSP_Write1_p054_minimax_error.png)

![DFT samples of a sampled signal](assets/adsp/ADSP_Write1_p075_sampled_signal_spectrum.png)
