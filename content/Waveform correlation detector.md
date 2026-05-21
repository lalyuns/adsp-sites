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

它適合 repeating or co-located events，因為相近 source path 會產生相似 waveform。限制也很清楚：若 event mechanism、location 或 path effect 差很多，template similarity 會下降。

在 array case 中，會先對每個 station 算 $C_m[n]$，再根據 expected delay 對齊並 stack，連到 [[Array beamforming for seismic detection]]。
