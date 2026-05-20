---
created: 2026-05-21
aliases:
  - "DFT complexity"
  - "convolution complexity"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fast algorithms]]"
tags:
  - "adsp"
  - "complexity"
  - "fft"
source:
  - "[[ADSP Write6 fast algorithms]]"
pages:
  - "ADSP_Write6/page_016.png"
---

# Complexity of DFT and convolution

這篇回答「為什麼需要 FFT」。直接 DFT 定義是

$$
X[k]=\sum_{n=0}^{N-1}x[n]W_N^{kn},
$$

每個 $k$ 都要加總 $N$ 項，總共有 $N$ 個 $k$，所以是 $O(N^2)$。當 $N$ 很大時，這個成本會主導整個系統。

Convolution 也有同樣問題。直接算長度約 $N$ 的 linear convolution 是 $O(N^2)$；但用 [[Fast Fourier transform]] 可以走

$$
x*h \rightarrow X\cdot H \rightarrow y,
$$

成本變成幾次 FFT/IFFT 加上 pointwise multiplication，約 $O(N\log N)$。

要注意 FFT convolution 常先做 zero padding，避免 circular convolution 造成 wrap-around。這裡應該連到 [[Convolution]]、[[Discrete Fourier transform]]、[[Fast Fourier transform]]，而不是只停在 Big-O 記號。


## 講義截圖
![Complexity summary](assets/adsp/ADSP_Write6_p016_complexity_summary.png)
