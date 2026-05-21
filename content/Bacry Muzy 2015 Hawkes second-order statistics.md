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
---

# Bacry Muzy 2015 Hawkes second-order statistics

這篇是 Hawkes 專題的理論與 estimation 核心。作者說明 multivariate Hawkes process 的 second-order statistics 可以 characterization kernel matrix，並用 Wiener-Hopf integral equations 做 non-parametric estimation。

報告重點：

- [[Multivariate Hawkes process]] 的 intensity 是 baseline intensity 加上 past jumps 經 kernel matrix 的影響。
- [[Hawkes kernel matrix]] 的元素描述不同 event types 之間的 excitation/inhibition。
- second-order statistics 包含 covariance/correlation of jumps；這些統計量與 kernel matrix 之間可寫成 Wiener-Hopf system。
- [[Nonparametric Hawkes estimation]] 的優點是不必預先假設 exponential kernel shape。

這篇可放在 Background/Methodology，支撐後面 LOB papers 的 kernel calibration。

## 論文圖表截圖

![Multivariate Hawkes process definition](assets/adsp/projects/hawkes_second_order_statistics_p002_hawkes_definition.png)

![Wiener-Hopf system for Hawkes kernel estimation](assets/adsp/projects/hawkes_second_order_statistics_p004_wiener_hopf_system.png)
