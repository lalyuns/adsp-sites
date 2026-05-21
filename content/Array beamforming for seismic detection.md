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

$$
C_{\mathrm{array}}[n]=\frac{1}{M}\sum_{m=1}^{M}C_m[n-\Delta_m].
$$

## ADSP Course Connection

這是 multichannel signal processing。coherent signal 會跨 station 對齊，random noise 不會；所以 stacking 可以提升 weak-event detection 的 SNR。它連到 array processing、[[Matched filter]]、correlation detector。

## Mathematical Statistics Connection

stacking 的直覺是 averaging reduces incoherent noise，這需要 [[Expectation]] 和 random signal 的平均直覺。

## Links

- [[Waveform correlation detector]]
- [[Matched filter]]
- [[Gibbons Ringdal 2006 array waveform correlation]]
- [[Probability for random signals]]
- [[Expectation]]
- [[Seismic wave signal processing project]]
