---
title: "[Programmers] N개의 최소공배수"
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
def solution(arr):
    answer = arr[0]
    for i in range(1, len(arr)):
        answer = (answer * arr[i]) // math.gcd(answer, arr[i])
        
    return answer
~~~
