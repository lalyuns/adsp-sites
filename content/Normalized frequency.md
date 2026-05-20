---
created: 2026-05-21
aliases:
  - "normalized frequency"
  - "歸一化頻率"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fourier analysis]]"
tags:
  - "adsp"
  - "frequency"
source:
  - "[[ADSP Write1 filter design and transforms]]"
pages:
  - "ADSP_Write1/page_026.png"
---

# Normalized frequency

Normalized frequency 把物理頻率除以 sampling frequency：

$$F=\frac{f}{f_s}=f\Delta_t.$$ 

DTFT/DFT 常用 $F\in[-1/2,1/2]$ 或 $[0,1)$。$F=1/2$ 是 folding frequency，也就是 Nyquist frequency。這能避免每次都帶著 Hz 和 sampling interval 計算。

## 講義截圖

![Normalized frequency and folding frequency](assets/adsp/ADSP_Write1_p026_normalized_frequency.png)

