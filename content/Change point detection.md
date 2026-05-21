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

Change point detection 問的是：一段 sequence 是否在某個 unknown time $\tau$ 前後改變 statistical law？

在 seismic picking 中，arrival 前後可能有 variance、spectrum、autocorrelation 或 waveform model 的改變。[[AIC picker]] 便把每個候選切點 $k$ 代入 cost function，選最能分割兩種狀態的位置。

和 threshold detector 相比，change-point view 更強調「前後兩段是否可由同一模型解釋」。這使它適合寫在報告的 methodology section，用來把 AIC 從公式連到 signal interpretation。
