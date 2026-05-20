---
created: 2026-05-21
aliases:
  - "摺積"
  - "卷積"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Fourier analysis]]"
  - "[[Filter design]]"
tags:
  - "adsp"
  - "math-prerequisites"
---

# Convolution

Convolution 描述 LTI system 的 input-output relation：

$$y[n]=x[n]*h[n]=\sum_r x[n-r]h[r].$$

Fourier domain 中 convolution 變 multiplication：$Y(F)=X(F)H(F)$。這個對偶是 filter design、equalizer、cepstrum、FFT convolution 的共同地基。
