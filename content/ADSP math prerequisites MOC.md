---
created: 2026-05-21
aliases:
  - "ADSP prerequisites"
  - "DSP 數學工具"
categories:
  - "[[Evergreen]]"
  - "[[Indexes]]"
topics:
  - "[[Advanced digital signal processing]]"
  - "[[Meta knowledge]]"
type:
  - "[[MOCs]]"
status:
  - "[[Active]]"
tags:
  - "adsp"
  - "math-prerequisites"
---

# ADSP math prerequisites MOC

這張 prerequisite map 應該當成補課清單：complex number 負責 Fourier notation，linear algebra 負責 projection/PCA/SVD/KLT，probability 負責 Wiener filter、covariance、MSE，optimization 負責 least-squares/minimax，coding theory 負責 entropy/Huffman。

## 深入解說

這篇是課程地圖，不是孤立定義。ADSP 的順序可以看成四層：先用 [[Fourier transform family]] 和 [[Z-transform]] 建立 signal/system language；再用 [[FIR filter]]、[[IIR filter]] 和 approximation norms 做 filter design；接著把這些工具放到 speech、image、compression、homomorphic processing；最後用 [[Fast Fourier transform]] 和 matrix factorization 讓演算法可計算。你的背景有微積分和數理統計，所以最需要補的是三塊橋樑：complex exponential notation、linear algebra projection/eigen concepts、random-signal expectation/correlation。

## 對你目前程度的讀法

先把這篇放回 [[ADSP notation survival guide]]。如果公式看起來突然跳太快，先不要急著背結論；把每個 symbol 的 role 寫在旁邊：它是 sample index、frequency variable、filter coefficient、random variable，還是 matrix/vector component。ADSP 很多困難其實不是微積分技巧，而是 notation 在 time domain、frequency domain、Z-domain、matrix domain 之間切換。

## 公式和講義圖怎麼讀

全課可用一條公式鏈串起來：signal $x[n]$ 進入 transform 得 coefficients，coefficients 被設計、壓縮、估計或快速計算，最後再回到 signal 或 decision。每章差別在 objective：filter design 要 response，speech 要 features，compression 要 rate-distortion，fast algorithm 要 complexity。

## 常見卡點

- 把 DFT bin 當成連續頻率，會誤讀頻譜解析度與 aliasing。
- 只看 magnitude 不看 phase，會漏掉 delay、linear phase、minimum phase、cepstrum inverse 等問題。
- 把 optimal 當成絕對最好；其實 optimal 永遠相對於 chosen model、norm、constraint。
- 忘記 implementation cost；ADSP 後半的 fast algorithms 會一直追問同一個數學結果能不能更有效率地算。

## 自我檢查

能不能把一個章節放到 transform、design、application、implementation 四層中的哪一層？能不能指出它需要補哪個 prerequisite？

## 相關筆記

- [[Advanced digital signal processing]]
- [[ADSP math prerequisites MOC]]
- [[ADSP notation survival guide]]
