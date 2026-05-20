---
created: 2026-05-21
aliases:
  - "edge detector"
  - "Sobel operator"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Popular filters]]"
  - "[[Image processing]]"
tags:
  - "adsp"
  - "image-processing"
  - "filters"
source:
  - "[[ADSP Write3 filters and homomorphic processing]]"
pages:
  - "ADSP_Write3/page_009.png"
---

# Edge detection filter

Edge detection filter 近似 highpass 或 differentiation。1-D difference $x[n+1]-x[n]$ 對 step edge 很敏感；2-D image 中可用 Sobel operator 偵測水平、垂直、斜向 edge。

直覺：edge 是 intensity 突變，所以在 frequency domain 有較多 high-frequency energy。

## 講義截圖

![Edge detection filter](assets/adsp/ADSP_Write3_p009_edge_detection_filter.png)

