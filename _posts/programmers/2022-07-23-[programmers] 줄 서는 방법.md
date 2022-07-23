---
title: "[Programmers] 줄 서는 방법"
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
import math
def solution(n, k):
    answer = []
    temps = list(range(1, n + 1))
    k -= 1
    for i in range(n, 0, -1):
        div, k = divmod(k, math.factorial(i - 1))
        answer.append(temps.pop(div))
    
    return answer
~~~
