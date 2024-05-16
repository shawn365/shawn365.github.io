---
title: "[Programmers] 기사단원의 무기"
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
def solution(number, limit, power):
    answer = 0
    arr = []
    for i in range(1, number + 1):
        cnt = 0
        for j in range(1, int(i ** 0.5) + 1):
            if i % j == 0:
                if i // j == j:
                    cnt += 1
                else:
                    cnt += 2
            if cnt > limit:
                cnt = power
                break
        answer += cnt

    return answer
```
