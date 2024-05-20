---
title: "[Programmers] 옹알이 (2)"
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
def solution(babbling):
    answer = 0
    arr = ["aya", "ye", "woo", "ma"]
    for i in babbling:
        for j in arr:
            if j * 2 not in i:
                i = i.replace(j, " ")
        if i.isspace():
            answer += 1

    return answer
```
