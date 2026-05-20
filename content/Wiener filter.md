---
created: 2026-05-21
aliases:
  - "Wiener filter"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Popular filters]]"
tags:
  - "adsp"
  - "filters"
  - "statistics"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_026.png"
---

# Wiener filter

Wiener filter 用 signal/noise statistics 設計 optimal linear filter。講義中的頻域形式可寫成

$$H_{opt}(F)=\frac{R_{xy}(F,F)}{R_{yy}(F,F)},$$

其中 $R_{xy}$ 是原訊號與接收訊號的 cross-correlation spectrum，$R_{yy}$ 是接收訊號 autocorrelation spectrum。它需要 [[Covariance matrix]] 與 [[Expectation]] 的直覺。

## 講義截圖

![Wiener filter](assets/adsp/ADSP_Write3_p026_wiener_filter.png)

