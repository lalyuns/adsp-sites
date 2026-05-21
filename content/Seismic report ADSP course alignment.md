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

# Seismic report ADSP course alignment

這篇是 seismic project 和 ADSP 課程的對齊筆記。它的用途是避免報告寫成地震學科普，而是明確寫成 advanced signal processing。

## Core Thesis

Seismic phase picking is an ADSP problem because it estimates arrival time from noisy, nonstationary waveforms by designing detector statistics, time-frequency representations, and template-matching filters.

換成中文：地震波 arrival picking 不是單純「看圖找波到哪裡」，而是把 waveform 經過 envelope、energy ratio、AIC cost、wavelet coefficients、correlation 等轉換，形成可判斷的 evidence。

## ADSP Course Connections

1. Signal representation：seismogram $x[n]$ 是 discrete-time signal，連到 [[ADSP notation survival guide]]。
2. Filtering and smoothing：STA/LTA 用 local energy/background energy，連到 [[Filter design]] 與 moving-window statistics。
3. Time-frequency/time-scale：wavelet-AIC 處理 nonstationary onset，連到 [[Short-time Fourier transform]] 與 [[Wavelet transform for seismic picking]]。
4. Matched filtering：waveform correlation 是 template similarity，連到 [[Matched filter]]。
5. Multichannel processing：array correlation/beamforming 把多 station evidence 疊加，連到 [[Array beamforming for seismic detection]]。
6. Random signal decision：threshold、false alarm、noise robustness 連到 [[Probability for random signals]]。

## Mathematical Statistics Connections

這題需要數理統計，但它是輔助 ADSP decision rule：

- [[Change point detection]]：arrival 前後統計性質改變。
- [[Likelihood function]]：AIC 是 likelihood-based model selection 的壓縮版本。
- [[Covariance matrix]]：correlation/similarity 的統計直覺。
- [[Expectation]]：energy/envelope/statistics 的平均行為。

## Report Framing

不要把題目寫成「Seismic Wave Introduction」。比較適合：

**Automatic Seismic Phase Detection as Advanced Signal Processing: Energy-Ratio, Change-Point, Multiscale, and Correlation Detectors**

這樣題目會明確表達：地震資料是 application，ADSP 主體是 detector design。

## Links

- [[Seismic wave signal processing project]]
- [[Seismic wave detection as ADSP]]
- [[Seismic project notation]]
- [[Seismic detector comparison]]
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
