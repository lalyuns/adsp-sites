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

# Compound Hawkes process

Compound Hawkes process 在 [[Hawkes process]] 的每個 jump 上附加 random size，也就是 mark。普通 counting process 只記 event 出現次數；compound process 進一步記錄每次 event 帶來多少 volume、order size 或 impact。

用於 [[Limit order book event stream]] 時，可把 type $i$ 的累積 marked process 寫成

$$
S_i(t)=\sum_{t_n^i\le t}v_n^i.
$$

## ADSP Course Connection

這是從 event-count signal 走向 marked event signal。它把「何時發生」與「事件大小」合併，讓 signal representation 能連到 market impact 或 volume response。

## Mathematical Statistics Connection

它需要 [[Expectation]] 來理解 cumulative mark 的平均行為，也需要 [[Conditional distribution]] 來建模 mark size。

## Links

- [[Hawkes process]]
- [[Marked Hawkes process]]
- [[Conditional intensity]]
- [[Limit order book event stream]]
- [[Market impact simulation]]
- [[Expectation]]
- [[Conditional distribution]]
