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

# Array beamforming for seismic detection

Array beamforming 把多個 sensors 的 evidence 按照 expected delay 對齊後疊加。對 [[Waveform correlation detector]] 而言，常疊加的是 correlation traces，而不是 raw waveform。

它的核心假設是 coherent signal 會跨 station 對齊，random noise 不會。這和 [[Matched filter]] 的 template similarity 結合後，可提高 weak-event detection 的 SNR。放在 [[Seismic wave signal processing project]] 裡，它是從 single-channel picking 走向 array-level detection 的關鍵橋樑。
