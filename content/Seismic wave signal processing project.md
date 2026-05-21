---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
tags:
  - "adsp"
  - "project-report"
  - "seismic"
  - "signal-detection"
---

# Seismic wave signal processing project

這個題目適合寫成一篇方法比較型報告：

**Automatic seismic phase detection and picking: from energy ratios to multiscale change-point and waveform-correlation detectors.**

報告的核心論點可以是：地震波 arrival picking 不是單一演算法問題，而是在 noisy, nonstationary waveform 中找「可被物理解釋的 arrival time」。不同方法其實對應不同假設：STA/LTA 假設 arrival 造成能量突然上升；AIC 假設 arrival 前後統計模型改變；wavelet-AIC 假設真正 arrival 會跨尺度穩定存在；waveform correlation 假設 repeating/co-located events 具有相似 waveform。

## Unified Notation

- 單站 seismogram：$x[n]$，sampling interval 為 $\Delta t$。
- 多站 array waveform：$x_m[n]$，$m=1,\ldots,M$。
- phase arrival time：$\tau$，目標是估計 $\hat{\tau}$。
- detector statistic：$D[n]$，超過 threshold 或達到 extremum 時產生 pick。
- template waveform：$s_m[n]$，用於 correlation/matched-filter detector。

## Method Chain

1. [[STA LTA picker]]：用局部能量比 $R[n]$ 做 quick detection。適合高 SNR、onset sharp 的事件。
2. [[AIC picker]]：用 change-point criterion 精修 arrival time。適合把 arrival 前後視為兩段不同 stochastic process。
3. [[Wavelet transform for seismic picking]]：用 multiscale representation 檢查 pick 是否跨尺度一致，減少 noise/scattering 假訊號。
4. [[Waveform correlation detector]]：對 known template 或 repeating events 最強；array case 可接 [[Array beamforming for seismic detection]]。

## Report Structure Suggestion

1. Abstract：一句話說明本報告比較三類 automatic seismic detectors。
2. Introduction：地震相位 picking 為何是 ADSP 問題：nonstationary signal、noise、time-frequency、matched filtering。
3. Signal model and notation：使用 [[Seismic project notation]]。
4. Classical detector：Earle and Shearer 的 STA/LTA envelope picker。
5. Multiscale change-point detector：Zhang et al. 的 wavelet-AIC。
6. Template/correlation detector：Gibbons and Ringdal 的 array waveform correlation。
7. Comparison：使用 [[Seismic detector comparison]]。
8. Conclusion：何時用哪個方法，以及對課程內容的連結。

核心 paper notes：[[Earle and Shearer 1994 automatic seismic phase picking]]、[[Zhang Thurber Rowe 2003 wavelet AIC P-wave picking]]、[[Gibbons Ringdal 2006 array waveform correlation]]。

## Figures For Report

![STA/LTA envelope picker and trigger threshold](assets/adsp/projects/seismic_sta_lta_picker_figure.png)

![Wavelet-AIC picks across several scales](assets/adsp/projects/seismic_wavelet_aic_multiscale_examples.png)

![Array waveform correlation improves weak-event detection](assets/adsp/projects/seismic_array_correlation_example_cropped.png)
