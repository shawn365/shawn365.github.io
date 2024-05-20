---
title: "[Programmers] 점프와 순간 이동"
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
def solution(n):
    ans = 0
    while n > 0:
        if n % 2 == 0:
            n = n // 2
        else:
            n = n - 1
            ans += 1

    return ans
```
