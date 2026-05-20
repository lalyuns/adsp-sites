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

MFCC 先用 Mel-frequency mask 模擬人耳頻率解析度，再對 log filterbank energy 做 cosine transform。它的優點是輸出 real、維度低、比較貼近 human perception，因此常作為 speech feature。

它連到 [[Speech signal processing]], [[Cepstrum]], [[Discrete cosine transform]]。

## 講義截圖

![Mel-frequency cepstrum](assets/adsp/ADSP_Write3_p064_mel_frequency_cepstrum.png)

