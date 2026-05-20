---
created: 2026-05-21
aliases:
  - "資料壓縮"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Data compression]]"
tags:
  - "adsp"
  - "compression"
source:
  - "[[ADSP Write5 data compression]]"
pages:
  - "ADSP_Write5/page_002.png"
---

# Data compression

Compression 先分 lossless/lossy。Lossless 用統計冗餘，lossy 進一步利用感知冗餘與任務容忍度。

## 深入解說

Compression 的核心不是「把檔案變小」而已，而是在 rate、distortion、perceptual quality 之間取 trade-off。JPEG 這條線尤其清楚：先把 RGB 換成 luminance/chrominance，利用人眼對色度較不敏感做 chroma subsampling，再用 DCT 把 spatial block 轉到 frequency-like coefficients，接著 quantization 丟掉不重要的高頻，最後 zigzag + entropy coding 把長串零有效編碼。讀講義圖時要一直問：這一步是 reversible 還是 lossy？它利用的是 human perception、statistical redundancy，還是 transform energy compaction？

## 對你目前程度的讀法

先把這篇放回 [[Compression math prerequisites]]。如果公式看起來突然跳太快，先不要急著背結論；把每個 symbol 的 role 寫在旁邊：它是 sample index、frequency variable、filter coefficient、random variable，還是 matrix/vector component。ADSP 很多困難其實不是微積分技巧，而是 notation 在 time domain、frequency domain、Z-domain、matrix domain 之間切換。

## 公式和講義圖怎麼讀

JPEG 的數學骨架是 block $f[m,n]$ 先做 DCT 得 $F[u,v]$，量化成 $\hat F[u,v]=\mathrm{round}(F[u,v]/Q[u,v])$，再用 zigzag 把低頻到高頻排成 1-D stream。Entropy coding 不是讓資訊消失，而是替已經量化後的符號序列找較短表示。

## 常見卡點

- 把 DFT bin 當成連續頻率，會誤讀頻譜解析度與 aliasing。
- 只看 magnitude 不看 phase，會漏掉 delay、linear phase、minimum phase、cepstrum inverse 等問題。
- 把 optimal 當成絕對最好；其實 optimal 永遠相對於 chosen model、norm、constraint。
- 忘記 implementation cost；ADSP 後半的 fast algorithms 會一直追問同一個數學結果能不能更有效率地算。

## 自我檢查

能不能把每個 JPEG step 標成 lossless 或 lossy？能不能說明為什麼 DCT 後低頻係數重要？能不能解釋 entropy coding 和 quantization 的差別？

## 相關筆記

- [[Advanced digital signal processing]]
- [[ADSP math prerequisites MOC]]
- [[Compression math prerequisites]]


## 講義截圖

![Compression philosophy](assets/adsp/ADSP_Write5_p002_compression_philosophy.png)
