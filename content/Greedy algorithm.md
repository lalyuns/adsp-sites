---
created: 2026-05-21
aliases:
  - "貪婪演算法"
categories:
  - "[[Evergreen]]"
topics:
  - "[[Meta knowledge]]"
  - "[[Data compression]]"
tags:
  - "adsp"
  - "math-prerequisites"
  - "algorithms"
---

# Greedy algorithm

Greedy algorithm 每一步都選當下看起來最好的局部決策。[[Huffman coding]] 是經典例子：每次合併最低機率的兩個 node，最後得到 prefix code tree。

Greedy 不一定總是 globally optimal，但 Huffman coding 這個問題剛好有 optimal substructure。
