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

若 P-wave arrival 是真實 physical change，它在多個 scale 上應該都造成可定位的 coefficient change；反之，高頻 noise 的 local fluctuation 可能只在細尺度出現。[[Zhang Thurber Rowe 2003 wavelet AIC P-wave picking]] 的 wavelet-AIC 思路就是：先用 wavelet 分解降低雜訊與尺度混淆，再在各 scale 上用 AIC 找候選 arrival。

報告寫法：wavelet step 提供 representation；AIC step 提供 decision rule；multiscale agreement 提供 robustness。
