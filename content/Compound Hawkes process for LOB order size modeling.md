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
S_i(t)=\sum_{n:t_n^i\le t} v_n^i.
$$

## ADSP Course Connection

這篇讓 Hawkes project 從 event timing 走到 marked signal modeling。對 ADSP 來說，這等於 signal representation 多了一個 amplitude/size channel，不再只處理 event impulses。

## Mathematical Statistics Connection

mark size 的分布是 [[Conditional distribution]] 問題；累積 mark 的平均行為需要 [[Expectation]]。若估參數，會用到 [[Likelihood function]]。

這張圖放在 calibrated kernel 小節。文字要說明 kernel matrix 代表 excitation direction and decay，適合討論 market microstructure interpretation。

![Calibrated Hawkes kernels for LOB event interactions](assets/adsp/projects/hawkes_compound_calibrated_kernels_cropped.png)

這張圖放在 marked/impact 小節。它不是單純結果展示，而是支撐「marks make intensity model financially meaningful」：order size 讓 event model 能連到 volume/impact。

![Compound Hawkes model links event intensity and market impact](assets/adsp/projects/hawkes_compound_market_impact_cropped.png)

## Links

- [[Compound Hawkes process]]
- [[Marked Hawkes process]]
- [[Hawkes kernel matrix]]
- [[Limit order book event stream]]
- [[Market impact simulation]]
- [[Conditional distribution]]
- [[Expectation]]
- [[Likelihood function]]
