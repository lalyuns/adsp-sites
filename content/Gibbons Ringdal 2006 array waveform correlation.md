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

# Gibbons Ringdal 2006 array waveform correlation

這篇代表 template-based seismic detection。它問的不是「第一個 onset 在哪裡」，而是：continuous data stream 裡是否出現與已知 template 足夠相似的弱事件？

## Method In Words

對每個 station $m$，計算 template $s_m$ 和 incoming waveform $x_m$ 的 normalized running cross-correlation $C_m[n]$。若 source location 相近，各 station 的 correlation peak 應該在校正 delay 後 coherent。把 $C_m[n]$ 對齊後 stack：

$$
C_{\mathrm{array}}[n]=\frac{1}{M}\sum_{m=1}^{M} C_m[n-\Delta_m].
$$

這就是 [[Array beamforming for seismic detection]] 與 [[Matched filter]] 的交會：不是疊加 raw waveform，而是疊加 similarity evidence。

這張圖放在 results/discussion 小節，說明 array stack 如何讓 weak-event correlation peak 更清楚。報告文字應強調：提升來自跨 station coherence，而非單一 station 的 amplitude 變大。

![Array waveform correlation improves weak-event detection](assets/adsp/projects/seismic_array_correlation_example_cropped.png)
