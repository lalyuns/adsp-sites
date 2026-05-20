---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Meta knowledge]]"
tags:
  - "adsp"
  - "meta-knowledge"
  - "prerequisite"
---

# Sampling and aliasing

Sampling 把 continuous-time signal 變成 $x[n]=x_c(nT)$。取樣後的頻譜會以 sampling frequency 為週期複製；如果原訊號超過 Nyquist frequency，複製的頻譜會重疊，這就是 aliasing。

對 ADSP 來說，aliasing 不是只在 A/D 發生。DFT frequency sampling、downsampling、chroma subsampling、FFT circular convolution 都有類似「週期化後重疊」的影子。看到 fold、periodic spectrum、circular convolution 時都該想到這個概念。

連結：[[Normalized frequency]]、[[Discrete-time Fourier transform]]、[[Discrete Fourier transform]]、[[Chroma subsampling]]。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 expectation，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、cepstrum prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、quantization、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
