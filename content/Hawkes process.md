---
created: 2026-05-21
categories:
  - "[[Evergreen]]"
topics:
  - "[[Hawkes process limit order book project]]"
tags:
  - "adsp"
  - "project-concept"
  - "hawkes-process"
---

# Hawkes process

Hawkes process 是 self-exciting point process：事件發生後，短時間內會提高後續事件的 [[Conditional intensity]]。它很適合描述 clustering，例如 earthquake aftershocks、order arrivals、click streams。

基本單變量形式：

$$
\lambda(t)=\mu+\int_0^t \phi(t-s)dN(s)
=\mu+\sum_{t_n<t}\phi(t-t_n).
$$

這裡 $dN(s)$ 可以看成 event impulse，$\phi$ 是 event-domain memory kernel。

## ADSP Course Connection

Hawkes process 與 ADSP 的關聯不在 FFT 本身，而在 [[Probability for random signals]]、[[Convolution]]、filter memory、system response 這條線。它把 regular sampled signal $x[n]$ 換成 event sequence $N(t)$，再用 kernel 把 history 轉成 activity level $\lambda(t)$。

## Mathematical Statistics Connection

它需要 [[Conditional expectation]] 的 conditioning 直覺：所有機率都 conditioned on history $\mathcal{H}_t$。若要估參數，會進入 [[Likelihood function]] 和 [[Maximum likelihood estimator]]。

## Links

- [[Hawkes process as event-domain filtering]]
- [[Conditional intensity]]
- [[Multivariate Hawkes process]]
- [[Marked Hawkes process]]
- [[Probability for random signals]]
- [[Convolution]]
- [[Conditional expectation]]
- [[Likelihood function]]
