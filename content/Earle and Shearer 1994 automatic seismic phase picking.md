---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
tags:
  - "adsp"
  - "seismic"
  - "paper-note"
---

# Earle and Shearer 1994 automatic seismic phase picking

這篇是地震波報告的 classical baseline。它的價值不是演算法複雜，而是把一個簡單 STA/LTA picker 套到大量全球 seismograms，證明 automatic picks 可以形成可解讀的 travel-time images。

## Method

流程可以寫成：

1. 從 seismogram 產生 envelope/characteristic function $e[n]$。
2. 計算 $\mathrm{STA}[n]$ 與 $\mathrm{LTA}[n]$。
3. 用 $R[n]=\mathrm{STA}[n]/\mathrm{LTA}[n]$ 找 trigger point。
4. 用 threshold、trigger timing、ratio shape 產生 arrival time 和 pick quality。
5. 把大量 picks 疊成 time-distance plots，觀察 P、PP、S、SS 等 phases。

## How To Use In The Report

這篇適合放在「energy-ratio detector」小節。它示範 ADSP 中最基本的 detection pipeline：preprocess -> characteristic function -> smoothing windows -> threshold -> visualization。

## Important Interpretation

高頻資料的 picks 較精準，但 long-period 資料能呈現更多低頻 phases。這提供一個很好的 discussion point：sampling rate / bandwidth / noise environment 會改變 detector 能看到的 seismic phases。

## Limitation

STA/LTA 對 threshold 很敏感，也容易受 emergent arrival、phase overlap、nonstationary noise 影響。這正好引出 [[AIC picker]] 與 [[Wavelet transform for seismic picking]]。

## Figures For Report

![STA/LTA envelope picker and trigger threshold](assets/adsp/projects/seismic_sta_lta_picker_figure.png)

![Automatically picked travel-time curves in time-distance space](assets/adsp/projects/seismic_global_travel_time_curves_cropped.png)
