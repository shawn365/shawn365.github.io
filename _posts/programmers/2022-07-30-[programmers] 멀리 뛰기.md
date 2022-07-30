---
title: "[Programmers] 멀리 뛰기"
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
    for i in range(0, n):
        a, b = b, a + b
        
    return b % 1234567
~~~