---
title: "[Programmers] 예상 대진표"
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
def solution(n,a,b):
    answer = 0
    while a != b:
        answer += 1
        a, b = (a + 1) // 2, (b + 1) // 2

    return answer
~~~