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

# ADSP notation survival guide

ADSP notation 最容易卡在同一個字母跨 domain 使用。建議每次看到公式先標三件事：變數、domain、單位。

- $n$ 通常是 discrete-time sample index；$t$ 是 continuous time。
- $\omega$ 是 normalized angular frequency，週期通常是 $2\pi$；$f$ 常是 Hz。
- $k$ 是 DFT bin index，代表第幾個 frequency sample，不是連續頻率。
- $z$ 是 complex plane variable；把 $z=e^{j\omega}$ 代入才是在 unit circle 上看 frequency response。
- $X(e^{j\omega})$、$X[k]$、$X(z)$ 可能都叫 spectrum，但資訊量不同：DTFT 連續、DFT 離散、Z-transform 還含 ROC/poles/zeros。

閱讀順序：先連到 [[Complex numbers for DSP]] 和 [[Euler formula]]，再讀 [[Discrete-time Fourier transform]]、[[Discrete Fourier transform]]、[[Z-transform]]。遇到 filter，就回到 [[Frequency response]]；遇到 compression，就回到 [[Discrete cosine transform]]；遇到 fast algorithm，就回到 [[Twiddle factor]]。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 expectation，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、cepstrum prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、quantization、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
