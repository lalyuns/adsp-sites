---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Seismic wave signal processing project]]"
  - "[[ADSP math prerequisites MOC]]"
tags:
  - "adsp"
  - "statistics"
  - "model-selection"
  - "seismic"
---

# Akaike information criterion

Akaike information criterion (AIC) 是用來比較 statistical models 的 criterion。直覺是：模型要 fit data，但不能因為參數太多而過度複雜。

常見形式：

$$
\mathrm{AIC}=2k-2\log \hat{L},
$$

其中 $k$ 是 model parameter count，$\hat{L}$ 是 maximized likelihood。

## ADSP Course Connection

在 seismic picking 裡，AIC 不是拿來選整篇論文模型，而是把每個候選切點 $k$ 當成一個 two-segment model，選讓前後兩段最合理的切點。這讓 arrival picking 變成 [[Change point detection]]。

## Mathematical Statistics Connection

AIC 連到 [[Likelihood function]] 與 [[Maximum likelihood estimator]]。你不需要完整推導 AIC，但要知道它是 likelihood-based model selection，而不是 amplitude threshold。

## Links

- [[AIC picker]]
- [[Change point detection]]
- [[Likelihood function]]
- [[Maximum likelihood estimator]]
- [[Seismic project notation]]
