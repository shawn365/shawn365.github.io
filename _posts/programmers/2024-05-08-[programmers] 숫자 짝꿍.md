---
title: "[Programmers] 숫자 짝꿍"
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
def solution(X, Y):
    answer = ""
    for i in range(9,-1,-1) :
        answer += (str(i) * min(X.count(str(i)), Y.count(str(i))))

    if not answer:
        answer = "-1"
    elif answer[0] == "0":
        answer = "0"

    return answer
```
