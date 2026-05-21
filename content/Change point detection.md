---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
tags:
  - "adsp"
  - "meta-knowledge"
  - "statistics"
---

# Change point detection

Change point detection 問的是：一段 sequence 是否在某個 unknown time $	au$ 前後改變 statistical law？

在 [[Seismic phase picking]] 中，arrival 前後可能有 variance、spectrum、autocorrelation 或 waveform model 的改變。[[AIC picker]] 把每個候選切點 $k$ 代入 cost function，選最能分割兩種狀態的位置。

和 threshold detector 相比，change-point view 更強調「前後兩段是否可由同一模型解釋」。因此它是 [[Detector statistic]] 的一種設計方式：不是看 amplitude 最大，而是看 segmentation cost 最小。放在 [[Seismic wave signal processing project]] 中，它負責把 AIC 公式連到 signal interpretation。
