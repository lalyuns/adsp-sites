---
created: 2026-05-21
aliases:
  - "SSIM"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Image processing]]"
  - "[[Data compression]]"
tags:
  - "adsp"
  - "image-quality"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_030.png"
---

# Structural similarity index

SSIM 衡量兩張影像在 luminance、contrast、structure 上的相似度：

$$SSIM(x,y)=\frac{(2\mu_x\mu_y+c_1L^2)(2\sigma_{xy}+c_2L^2)}{(\mu_x^2+\mu_y^2+c_1L^2)(\sigma_x^2+\sigma_y^2+c_2L^2)}.$$

它比 MSE/NRMSE 更接近人類視覺，因為人眼對結構相似度比 pixel-wise error 更敏感。

## 講義截圖

![Structural similarity formula](assets/adsp/ADSP_Write5_p030_ssim_formula.png)

