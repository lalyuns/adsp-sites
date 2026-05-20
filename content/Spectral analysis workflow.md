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

# Spectral analysis workflow

Spectral analysis 不是把資料丟進 FFT 就結束。完整流程應該是：

1. 先確認 sampling rate $f_s$，決定 Nyquist frequency $f_s/2$。
2. 判斷訊號是否 stationary；如果不是，用 [[Short-time Fourier transform]]。
3. 選 window 和 frame length；長 window 頻率解析度好，短 window 時間定位好。
4. 決定 frequency axis：Hz、normalized frequency、或 DFT bin。
5. 解讀 magnitude 和 phase；filter design 常重 magnitude，speech/cepstrum 常不能忽略 phase。

這張 workflow 連接 [[Normalized frequency]]、[[Discrete Fourier transform]]、[[Frequency response]]、[[Cepstrum]]。你可以把它當成看講義頻譜圖的 checklist。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 expectation，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、cepstrum prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、quantization、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
