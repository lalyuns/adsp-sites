---
created: 2026-05-21
aliases:
  - "影像壓縮"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Data compression]]"
  - "[[Image processing]]"
tags:
  - "adsp"
  - "compression"
  - "image-processing"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_008.png"
---

# Image compression

Image compression 利用 spatial correlation：鄰近 pixels 通常相似，transform 後 energy 集中在低頻。這就是 DCT/JPEG 有效的根本原因。

連結：[[Compression math prerequisites]]、[[JPEG compression]]。


## 講義截圖
![Image frequency-domain consistency](assets/adsp/ADSP_Write5_p008_image_frequency_domain.png)
