---
title: "[Programmers] 귤 고르기"
categories:
  - Programmers
tags:
  - [Programmers, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## Python

```python
import collections
def solution(k, tangerine):
    answer = 0
    dic = collections.Counter(tangerine)
    sorted_counts = sorted(dic.values(), reverse=True)
    count = 0

    for i in sorted_counts:
        count += i
        answer += 1
        if count >= k:
            break

    return answer
```
