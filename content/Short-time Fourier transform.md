---
created: 2026-05-21
aliases:
  - "STFT"
  - "windowed Fourier transform"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Speech processing]]"
  - "[[Fourier analysis]]"
tags:
  - "adsp"
  - "speech"
  - "fourier"
source:
  - "[[ADSP Write4 acoustics speech PCA SVD]]"
pages:
  - "ADSP_Write4/page_018.png"
---

# Short-time Fourier transform

STFT 用 sliding window 做 Fourier transform，得到 time-frequency representation。window 太短 frequency resolution 差，太長 time resolution 差，這是 uncertainty trade-off。

連結：[[Spectral analysis workflow]]、[[Cepstrum prerequisite map]]。


## 講義截圖
![Short-time Fourier transform](assets/adsp/ADSP_Write4_p018_stft.png)
