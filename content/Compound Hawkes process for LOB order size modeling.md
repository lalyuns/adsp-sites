---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "hawkes-process"
  - "paper-note"
  - "limit-order-book"
---

# Compound Hawkes process for LOB order size modeling

這篇把 Hawkes timing model 和 order-size marks 連起來。對 project report 來說，它的角色是橋接 [[Hawkes kernel matrix]] 與 [[Marked Hawkes process]]。

## Method In Words

一般 Hawkes 主要描述 event time/type。Compound Hawkes 進一步讓 event carry size mark $v_n$，使模型可討論 accumulated volume、order size distribution 與 market impact。報告中可寫成：

$$
S_i(t)=\sum_{n:t_n^i\le t} v_n^i,
$$

其中 $S_i(t)$ 是 type $i$ events 累積的 marked process。這比只看 $N_i(t)$ 多了 size information。

這張圖放在 calibrated kernel 小節。文字要說明 kernel matrix 代表 excitation direction and decay，適合討論 market microstructure interpretation。

![Calibrated Hawkes kernels for LOB event interactions](assets/adsp/projects/hawkes_compound_calibrated_kernels_cropped.png)

這張圖放在 marked/impact 小節。它不是單純結果展示，而是支撐「marks make intensity model financially meaningful」：order size 讓 event model 能連到 volume/impact。

![Compound Hawkes model links event intensity and market impact](assets/adsp/projects/hawkes_compound_market_impact_cropped.png)
