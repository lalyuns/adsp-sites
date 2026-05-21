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

# AIC picker

AIC picker 把 onset picking 改寫成 [[Change point detection]]。給定一段 waveform window，假設切點 $k$ 之前與之後可用不同 variance/model 描述，常見形式可寫成

$$
\mathrm{AIC}(k)=k\log(\sigma_1^2(k))+(N-k-1)\log(\sigma_2^2(k)).
$$

$\hat{\tau}$ 取 AIC 最小的位置。這不是神秘公式，而是在問：哪個切點讓「arrival 前」與「arrival 後」兩段最像兩個不同統計狀態？

## ADSP Course Connection

AIC picker 把 waveform picking 變成 model-based detector。和 [[STA LTA picker]] 相比，它不只看 energy jump，而是看 segmentation cost 是否支持前後兩段有不同 statistics。

## Mathematical Statistics Connection

AIC 來自 [[Akaike information criterion]]，背後是 [[Likelihood function]] 和 model selection。報告可以寫「AIC is a change-point criterion」，不用深入推導 asymptotic theory。

## Links

- [[Seismic phase picking]]
- [[Change point detection]]
- [[Akaike information criterion]]
- [[Likelihood function]]
- [[STA LTA picker]]
- [[Wavelet transform for seismic picking]]
- [[Seismic project notation]]
