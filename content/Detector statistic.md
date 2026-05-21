---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
tags:
  - "adsp"
  - "meta-knowledge"
  - "signal-detection"
---

# Detector statistic

Detector statistic 是把 raw signal 壓縮成可判斷事件的 scalar sequence：

$$
D[n]=T(x[n-W+1:n]).
$$

不同 detector 的差異在於 transform $T$ 選什麼。[[STA LTA picker]] 的 $D[n]$ 是 energy ratio；[[AIC picker]] 的 $D[k]$ 是 segmentation cost；[[Waveform correlation detector]] 的 $D[n]$ 是 template similarity；Hawkes model 裡的 counterpart 則是 [[Conditional intensity]] $\lambda(t)$。

## ADSP Course Connection

這是 ADSP 裡「representation supports decision」的核心。filter、transform、correlation、time-frequency analysis 都不是為了變漂亮，而是為了讓 event/non-event 更可分。

## Mathematical Statistics Connection

detector statistic 通常會搭配 threshold 或 extremum rule，因此自然連到 false alarm、missed detection、model selection。對 seismic project 最重要的是 [[Change point detection]] 和 [[Akaike information criterion]]。

## Links

- [[Seismic wave detection as ADSP]]
- [[STA LTA picker]]
- [[AIC picker]]
- [[Waveform correlation detector]]
- [[Conditional intensity]]
- [[Matched filter]]
- [[Probability for random signals]]
- [[Change point detection]]
- [[Akaike information criterion]]
