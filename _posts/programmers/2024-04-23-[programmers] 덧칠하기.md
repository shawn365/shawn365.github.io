---
title: "[Programmers] 덧칠하기"
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
def solution(n, m, section):
    answer = 1
    paint = section[0] + m - 1
    for i in section:
        if i > paint:
            paint = i + m - 1
            answer += 1

    return answer
```
