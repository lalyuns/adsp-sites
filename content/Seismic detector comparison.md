---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
tags:
  - "adsp"
  - "seismic"
  - "method-comparison"
  - "project-report"
---

# Seismic detector comparison

這篇是報告 discussion 的素材，重點是比較 assumptions，不是列優缺點清單。

## Detector Families

| Method | Core statistic | Hidden assumption | Best case | Failure mode |
|---|---|---|---|---|
| [[STA LTA picker|STA/LTA]] | short/long energy ratio | arrival causes energy jump | sharp onset, high SNR | emergent onset, drifting noise |
| [[AIC picker|AIC]] picker | change-point model selection | pre/post arrival have different variance/model | local arrival refinement | wrong window, multiple local minima |
| Wavelet-AIC | multiscale consistency + AIC | real onset persists across scales | low SNR, singular onset | parameter-heavy; [[Wavelet transform for seismic picking|wavelet]] choice matters |
| Waveform correlation | normalized template similarity | future event resembles known template | repeating/co-located events | poor for novel mechanisms |
| Array correlation | coherent stack of station statistics | signal aligns across array; noise does not | weak-event detection | needs array geometry/delay correction |

## ADSP Course Connection

這張表的重點是：每個 method 都是不同的 signal representation plus decision rule。這正是 ADSP 的核心。

## Mathematical Statistics Connection

STA/LTA 是 threshold decision；AIC 是 likelihood/model-selection decision；correlation detector 是 similarity statistic；array stacking 是 averaging/coherence evidence。

## Links

- [[Seismic wave signal processing project]]
- [[Seismic wave detection as ADSP]]
- [[Detector statistic]]
- [[STA LTA picker]]
- [[AIC picker]]
- [[Akaike information criterion]]
- [[Wavelet transform for seismic picking]]
- [[Waveform correlation detector]]
- [[Array beamforming for seismic detection]]
- [[Matched filter]]
- [[Probability for random signals]]
