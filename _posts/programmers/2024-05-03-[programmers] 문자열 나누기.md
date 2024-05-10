---
title: "[Programmers] 문자열 나누기"
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
def solution(s):
    answer = 0
    current = ""
    count = 0
    for idx, val in enumerate(s):
        if count == 0:
            answer += 1
            current = val
            count += 1
        else:
            if current == val:
                count += 1
            else:
                count -= 1

    return answer
```
