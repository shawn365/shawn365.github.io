---
title: "[Programmers] 푸드 파이트 대회"
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
def solution(food):
    answer = ''
    for i in range(1, len(food)):
        food_count = food[i] // 2
        if food_count != 0:
            for j in range(food_count):
                answer += str(i)
    answer += "0" + answer[::-1]

    return answer
```
