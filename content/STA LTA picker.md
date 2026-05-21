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

報告中不要只說「計算 STA/LTA」。要說清楚它的 modeling assumption：arrival 是 amplitude/energy change。這也解釋它的 failure mode：若 onset 很 gradual、noise nonstationary、或 threshold 設錯，$R[n]$ 可能提前/延後 trigger。

關聯：[[Detector statistic]]、[[Seismic project notation]]、[[Earle and Shearer 1994 automatic seismic phase picking]]。
