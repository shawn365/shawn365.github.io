---
title: "[Programmers] 피보나치 수"
categories:
  - Programmers
tags:
  - [Programmers, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## Python
~~~python
def solution(n):
    answer = []
    for i in range(0, n+1):
        if i == 0:
            answer.append(0)
        elif i == 1:
            answer.append(1)
        else:
            answer.append(answer[i - 2] + answer[i - 1])

    return answer[n] % 1234567
~~~
