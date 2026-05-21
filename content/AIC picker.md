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

報告中可把它定位為 STA/LTA 之後的 refinement：STA/LTA 找粗略 event window，AIC 在 window 內找更精準 onset。缺點是 window choice 與 local minima 會影響結果，所以 [[Wavelet transform for seismic picking]] 會引入 multiscale consistency。
