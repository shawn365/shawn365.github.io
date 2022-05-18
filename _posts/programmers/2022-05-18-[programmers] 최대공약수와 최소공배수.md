---
title: "[Programmers] 최대공약수와 최소공배수"
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
def solution(n, m):
    answer = [math.gcd(n, m), ((n * m) // math.gcd(n, m))]
    return answer
~~~
