---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Meta knowledge]]"
tags:
  - "adsp"
  - "meta-knowledge"
  - "prerequisite"
---

# Probability for random signals

Random signal 不是每個 sample 都亂猜，而是把整段訊號看成 stochastic process。ADSP 常用的統計量有：

- expectation $E[X]$：平均行為。
- variance：偏離平均的能量。
- autocorrelation：同一訊號不同 time lag 的相似度。
- cross-correlation：兩個訊號的相似度。
- power spectral density：random signal 在頻率上的平均能量分布。

[[Wiener filter]]、[[Matched filter]]、[[Covariance matrix]]、[[Karhunen-Loeve transform]] 都會用到這些工具。你修過數理統計，所以這裡要補的是「把 random variable 推廣成 indexed family $X[n]$」。

## 使用方法

這篇 meta note 不需要一次背完。你可以在讀講義時回來查：先找自己卡住的是 notation、domain、random signal、matrix factorization、還是 optimization，再沿著連結回到對應概念筆記。若一個公式同時含有 transform 和 expectation，先分開處理，不要把所有符號混在同一層理解。

## 和 ADSP 講義的關聯

- Write1/Write2 多半需要 notation、spectral analysis、filter-design optimization。
- Write3 需要 probability、cepstrum prerequisite、filter interpretation。
- Write4 需要 STFT、speech source-filter model、linear algebra。
- Write5 需要 transform coding、quantization、entropy。
- Write6 需要 index decomposition、matrix factorization、complexity counting。
