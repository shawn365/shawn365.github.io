---
title: "[Programmers] 크기가 작은 부분문자열"
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
def solution(t, p):
    answer = 0
    for i in range(len(t) - len(p) + 1):
        temp = ""
        for j in range(len(p)):
            temp += t[i + j]
        if int(temp) <= int(p):
            answer += 1

    return answer
```
