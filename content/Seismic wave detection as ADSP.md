---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
  - "[[Advanced digital signal processing]]"
tags:
  - "adsp"
  - "seismic"
  - "course-connection"
  - "project-report"
---

# Seismic wave detection as ADSP

Seismic wave detection 和 ADSP 的核心連結是：它把 noisy, nonstationary waveform 轉成 detector statistics，再用 decision rule 找出 physically meaningful phase arrival。

在一般 DSP 裡，我們常從 signal $x[n]$ 經過 filter/transform 得到 representation：

$$
z[n]=T(x[n]).
$$

在 seismic phase picking 裡，這個 representation 不是最後答案，而是為了產生 detector statistic：

$$
D[n]=T(x[n-W+1:n]),
\qquad
\hat{\tau}=\operatorname{decision}(D[n]).
$$

因此報告主線應該寫成：不同方法其實是在設計不同的 $T$ 與 decision rule。

## ADSP Course Connection

- [[Detector statistic]]：把 waveform 壓縮成可判斷事件的 scalar evidence。
- [[Filter design]] / [[Matched filter]]：STA/LTA、waveform correlation 都是把 waveform 轉成更容易判斷的 statistic。
- [[Short-time Fourier transform]] / [[Wavelet transform for seismic picking]]：處理 nonstationary signal 的 time-frequency/time-scale representation。
- [[Probability for random signals]]：noise、false alarm、threshold、correlation peak 都需要 random signal 直覺。
- [[Spectral analysis workflow]]：地震波是非平穩訊號，不能只看全域 frequency content。

## Mathematical Statistics Connection

- [[Change point detection]]：AIC picking 把 arrival 看成 statistical regime change。
- [[Likelihood function]]：AIC 的思想來自 likelihood-based model selection。
- [[Covariance matrix]] / correlation：waveform correlation 和 array stacking 依賴 similarity/evidence aggregation。

## Links

- [[Seismic wave signal processing project]]
- [[Seismic report ADSP course alignment]]
- [[Detector statistic]]
- [[STA LTA picker]]
- [[AIC picker]]
- [[Wavelet transform for seismic picking]]
- [[Waveform correlation detector]]
- [[Matched filter]]
- [[Short-time Fourier transform]]
- [[Probability for random signals]]
- [[Change point detection]]
- [[Likelihood function]]
