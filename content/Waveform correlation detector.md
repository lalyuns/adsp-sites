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
  - "matched-filter"
---

# Waveform correlation detector

Waveform correlation detector 把 seismic detection 看成 template matching。若 template $s[n]$ 與 incoming data $x[n]$ 在某段時間相似，normalized cross-correlation 會出現 peak：

$$
C[n]=\frac{\sum_{\ell=0}^{L-1}(x[n+\ell]-\bar{x}_n)(s[\ell]-\bar{s})}
{\sqrt{\sum_{\ell=0}^{L-1}(x[n+\ell]-\bar{x}_n)^2}\sqrt{\sum_{\ell=0}^{L-1}(s[\ell]-\bar{s})^2}}.
$$

它和 [[Matched filter]] 是同一族想法：若訊號形狀接近 template，similarity statistic 會變大。它適合 repeating or co-located events；若 event mechanism、location 或 path effect 差很多，template similarity 會下降。

## ADSP Course Connection

這是 seismic project 裡最直接連到 matched filtering 的部分。它不是找 onset sharpness，而是問「這段 waveform 是否像某個已知 template」。array case 中，會先對每個 station 算 $C_m[n]$，再根據 expected delay 對齊並 stack，連到 [[Array beamforming for seismic detection]]。

## Mathematical Statistics Connection

correlation peak 是 similarity evidence。若要設定 detection threshold，就需要 [[Probability for random signals]] 的 false alarm / noise distribution 直覺。

## Links

- [[Seismic wave detection as ADSP]]
- [[Matched filter]]
- [[Array beamforming for seismic detection]]
- [[Gibbons Ringdal 2006 array waveform correlation]]
- [[Detector statistic]]
- [[Probability for random signals]]
- [[Covariance matrix]]
