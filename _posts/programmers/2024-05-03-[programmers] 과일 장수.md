---
title: "[Programmers] 과일 장수"
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
def solution(k, m, score):
    answer = 0
    sort_score = sorted(score, reverse=True)
    lst = []
    for i in range(len(sort_score)):
        lst.append(sort_score[i])
        if len(lst) == m:
            answer += min(lst) * m
            lst = []

    return answer
```
