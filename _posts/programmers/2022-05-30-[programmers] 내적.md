---
title: "[Programmers] 내적"
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
def solution(a, b):
    answer = 0
    for i in range(len(a)):
        answer += a[i] * b[i]
        
    return answer
~~~
