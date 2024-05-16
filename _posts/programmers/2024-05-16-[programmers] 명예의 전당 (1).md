---
title: "[Programmers] 명예의 전당 (1)"
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
def solution(k, score):
    arr = []
    answer = []
    for s in score:
        arr.append(s)
        if (len(arr) > k):
            arr.remove(min(arr))
        answer.append(min(arr))

    return answer
```
