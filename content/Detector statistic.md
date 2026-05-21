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

對你的程度來說，這個概念很重要：演算法不是黑箱步驟，而是在設計一個 statistic，使它在「事件存在」與「事件不存在」時有可分辨行為。
