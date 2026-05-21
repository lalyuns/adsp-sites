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

# STA LTA picker

STA/LTA picker 是 energy-ratio detector。先把 waveform $x[n]$ 轉成 envelope 或 characteristic function $e[n]$，再比較短窗與長窗平均能量：

$$
R[n]=\frac{\mathrm{STA}[n]}{\mathrm{LTA}[n]+\epsilon}.
$$

若 $R[n]$ 超過 threshold，就判定附近可能有 phase arrival。直覺是：arrival 讓 local energy 突然升高，而 LTA 代表背景 noise level。

## ADSP Course Connection

STA/LTA 是最直覺的 moving-window detector：短窗估 local energy，長窗估 background。它連到 filtering/smoothing、windowed statistics，以及 [[Detector statistic]] 的設計。報告中要說清楚它的 assumption：arrival 會造成 amplitude/energy jump。

## Mathematical Statistics Connection

threshold choice 對 false alarm/missed detection 有影響。若 noise nonstationary，LTA 估計的 background 會偏掉。

## Links

- [[Seismic phase picking]]
- [[Detector statistic]]
- [[Seismic project notation]]
- [[Earle and Shearer 1994 automatic seismic phase picking]]
- [[Probability for random signals]]
