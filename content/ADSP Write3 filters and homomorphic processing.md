---
created: 2026-05-21
aliases:
  - "ADSP Write3"
  - "Write3"
categories:
  - "[[Evergreen]]"
  - "[[Indexes]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Homomorphic processing]]"
type:
  - "[[MOCs]]"
status:
  - "[[Active]]"
tags:
  - "adsp"
  - "filters"
  - "cepstrum"
pages:
  - "ADSP_Write3/page_001.png-page_093.png"
---

# ADSP Write3 filters and homomorphic processing

Write3 分成兩段：先介紹常用 filters，再進入 homomorphic/cepstrum。

前半段的 filter 應該按任務讀：

- [[Notch filter]]：移除窄頻干擾。
- [[Smoother filter]]：用 local averaging 壓高頻雜訊，但會模糊快速變化。
- [[Hilbert transform filter]]：做 $90^\circ$ phase shift，常用於 analytic signal。
- [[Edge detection filter]]：差分/高通，強調影像或訊號中的 abrupt change。
- [[Matched filter]]：已知 template 時最大化 detection SNR。
- [[Wiener filter]]：已知 signal/noise statistics 時最小化 MSE。
- [[Equalizer filter]]：補償 channel distortion。

後半段是另一個思路：[[Homomorphic signal processing]] 把 convolution 透過 Fourier 和 log 轉成 addition；[[Cepstrum]]、[[Complex cepstrum]]、[[Differential cepstrum]]、[[Mel-frequency cepstrum]] 都是這條線的變形。讀這裡時要特別分清 spectrum 的 frequency axis 和 cepstrum 的 quefrency axis。

前置補洞：[[Probability for random signals]]、[[Cepstrum prerequisite map]]、[[Frequency response]]。


## 講義截圖
![Smoother as weighted average](assets/adsp/ADSP_Write3_p003_smoother_weighted_average.png)

![Matched filter](assets/adsp/ADSP_Write3_p016_matched_filter.png)

![Cepstrum process](assets/adsp/ADSP_Write3_p042_cepstrum_process.png)

![Mel-frequency cepstrum](assets/adsp/ADSP_Write3_p064_mel_frequency_cepstrum.png)
