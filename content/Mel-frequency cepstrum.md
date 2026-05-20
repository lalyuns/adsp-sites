---
created: 2026-05-21
aliases:
  - "MFCC"
  - "Mel-frequency cepstral coefficients"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Speech processing]]"
tags:
  - "adsp"
  - "speech"
  - "cepstrum"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_064.png"
---

# Mel-frequency cepstrum

MFCC 先把 spectrum 經過 Mel-scale filterbank，再取 log 和 DCT。它不是為了完美重建，而是為了抽取符合人耳感知的 speech/audio features。

連結：[[Cepstrum prerequisite map]]、[[Homomorphic signal processing]]。


## 講義截圖
![Mel-frequency cepstrum](assets/adsp/ADSP_Write3_p064_mel_frequency_cepstrum.png)
