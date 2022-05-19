---
title: "[Programmers] 정수 제곱근 판별"
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
def solution(n):
    if math.sqrt(n) == int(math.sqrt(n)):
        return (math.sqrt(n) + 1) ** 2
    return -1
~~~
