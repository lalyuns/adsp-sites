---
created: 2026-05-21
aliases:
  - "formant"
  - "共振峰"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Speech processing]]"
tags:
  - "adsp"
  - "speech"
source:
  - "[[ADSP Write4 acoustics speech PCA SVD]]"
pages:
  - "ADSP_Write4/page_020.png"
---

# Formant

Formants 是 vocal tract resonance 的頻率峰值，常記為 F1、F2、F3。它們比較反映 articulation，不等同於 pitch。

## 深入解說

Speech/audio 筆記的重點是 nonstationary signal。普通 Fourier transform 假設整段訊號統計性質不變，但語音會隨時間改變，所以用 [[Short-time Fourier transform]] 把訊號切成短 window，再看每個 frame 的 spectrum。pitch 對應 vocal-fold vibration 的 fundamental frequency，formants 對應 vocal tract resonance；前者比較像 source，後者比較像 filter。這就是 source-filter model，也會和 [[Cepstrum]]、[[Mel-frequency cepstrum]] 接在一起。

## 對你目前程度的讀法

先把這篇放回 [[Spectral analysis workflow]] 和 [[Cepstrum prerequisite map]]。如果公式看起來突然跳太快，先不要急著背結論；把每個 symbol 的 role 寫在旁邊：它是 sample index、frequency variable、filter coefficient、random variable，還是 matrix/vector component。ADSP 很多困難其實不是微積分技巧，而是 notation 在 time domain、frequency domain、Z-domain、matrix domain 之間切換。

## 公式和講義圖怎麼讀

STFT 常寫成 $X(m,\omega)=\sum_n x[n]w[n-mR]e^{-j\omega n}$。$m$ 是 frame/time position，$\omega$ 是 frame 內的 frequency。Formant 圖中的峰值不是 harmonic spacing；pitch 看的是 harmonic 間距，formant 看的是 spectral envelope。

## 常見卡點

- 把 DFT bin 當成連續頻率，會誤讀頻譜解析度與 aliasing。
- 只看 magnitude 不看 phase，會漏掉 delay、linear phase、minimum phase、cepstrum inverse 等問題。
- 把 optimal 當成絕對最好；其實 optimal 永遠相對於 chosen model、norm、constraint。
- 忘記 implementation cost；ADSP 後半的 fast algorithms 會一直追問同一個數學結果能不能更有效率地算。

## 自我檢查

能不能在 spectrogram 上分 pitch harmonics 和 formant envelope？能不能說明 window length 改變會影響哪個解析度？

## 相關筆記

- [[Advanced digital signal processing]]
- [[ADSP math prerequisites MOC]]
- [[Spectral analysis workflow]] 和 [[Cepstrum prerequisite map]]


## 講義截圖

![Speech formants](assets/adsp/ADSP_Write4_p020_formants.png)
