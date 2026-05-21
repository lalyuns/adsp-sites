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
| STA/LTA | short/long energy ratio | arrival causes energy jump | sharp onset, high SNR | emergent onset, drifting noise |
| AIC picker | change-point model selection | pre/post arrival have different variance/model | local arrival refinement | wrong window, multiple local minima |
| Wavelet-AIC | multiscale consistency + AIC | real onset persists across scales | low SNR, singular onset | parameter-heavy; wavelet choice matters |
| Waveform correlation | normalized template similarity | future event resembles known template | repeating/co-located events | unknown source or changing path |
| Array correlation | stacked coherent correlation | correlation traces align across array | weak events with array gain | wrong slowness/backazimuth model |

## Report Argument

STA/LTA is a detector of amplitude change; AIC is a detector of statistical change; wavelet-AIC is a detector of scale-persistent singularity; waveform correlation is a detector of waveform similarity. This distinction is useful because it explains why no single method dominates all seismic picking tasks.

連結：[[Earle and Shearer 1994 automatic seismic phase picking]]、[[Zhang Thurber Rowe 2003 wavelet AIC P-wave picking]]、[[Gibbons Ringdal 2006 array waveform correlation]]。
