---
created: 2026-05-21
aliases:
  - "DTFT"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fourier analysis]]"
tags:
  - "adsp"
  - "fourier"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_022.png"
  - "ADSP_Write1/page_026.png"
---

# Discrete-time Fourier transform

DTFT 把無限長 sequence $x[n]$ 映到週期性的 $X(e^{j\omega})$。因為 input 是 discrete time，frequency domain 會以 $2\pi$ 為週期；這件事會支配 normalized frequency、aliasing、digital filter response。

連結：[[ADSP notation survival guide]]、[[Spectral analysis workflow]]。


## 講義截圖
![Fourier transform types](assets/adsp/ADSP_Write1_p022_fourier_transform_types.png)

![Normalized frequency and folding frequency](assets/adsp/ADSP_Write1_p026_normalized_frequency.png)
