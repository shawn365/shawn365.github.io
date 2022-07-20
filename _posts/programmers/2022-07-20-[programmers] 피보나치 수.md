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
    a, b = 0, 1
    for i in range(n):
        a, b = b, a + b
    
    return a
~~~
