---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
tags:
  - "adsp"
  - "project-concept"
  - "seismic"
---

# Seismic phase picking

Seismic phase picking 是在 seismogram 中估計 P-wave 或 S-wave arrival time：

$$
\hat{\tau}=\operatorname{pick}(x[n]).
$$

它不是單純找最大 amplitude，因為 arrival 可能很弱、很漸進，且 noise nonstationary。比較好的觀點是：先設計 [[Detector statistic]]，再用 threshold、minimum、peak 或 consistency rule 做 decision。

## ADSP Course Connection

這篇是 seismic project 的問題定義。它把地震學問題翻譯成 ADSP 問題：從 noisy discrete-time waveform 估計 event time。方法可分成 energy-ratio、change-point、multiscale、template correlation 四類。

## Mathematical Statistics Connection

如果 arrival 前後 waveform statistics 改變，就可以用 [[Change point detection]]。若使用 AIC，則連到 [[Akaike information criterion]] 和 [[Likelihood function]]。

## Links

- [[Seismic wave signal processing project]]
- [[Seismic wave detection as ADSP]]
- [[Detector statistic]]
- [[STA LTA picker]]
- [[AIC picker]]
- [[Wavelet transform for seismic picking]]
- [[Waveform correlation detector]]
- [[Change point detection]]
