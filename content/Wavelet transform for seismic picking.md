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
  - "wavelet"
---

# Wavelet transform for seismic picking

Wavelet transform 把 waveform 轉成 time-scale representation。對 seismic picking 來說，重點不是「畫時頻圖」而已，而是用 scale 來檢查 onset 是否穩定。

若 P-wave arrival 是真實 physical change，它在多個 scale 上應該都造成可定位的 coefficient change；反之，高頻 noise 的 local fluctuation 可能只在細尺度出現。[[Zhang Thurber Rowe 2003 wavelet AIC P-wave picking]] 的 wavelet-[[AIC picker|AIC]] 思路就是：先用 wavelet 分解降低雜訊與尺度混淆，再在各 scale 上用 AIC 找候選 arrival。

## ADSP Course Connection

這是非平穩訊號的 representation 問題。傳統全域 spectrum 不足以定位 onset；wavelet 提供 time-scale localization，和 [[Short-time Fourier transform]] 共享「localize signal behavior」的精神。

## Mathematical Statistics Connection

wavelet step 本身偏 ADSP；AIC step 則連到 [[Change point detection]] 和 [[Akaike information criterion]]。multiscale agreement 可被視為 robustness evidence。

## Links

- [[Seismic phase picking]]
- [[AIC picker]]
- [[Change point detection]]
- [[Akaike information criterion]]
- [[Short-time Fourier transform]]
- [[Spectral analysis workflow]]
- [[Zhang Thurber Rowe 2003 wavelet AIC P-wave picking]]
