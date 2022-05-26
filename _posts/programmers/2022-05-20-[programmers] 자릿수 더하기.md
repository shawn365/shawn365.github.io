---
title: "[Programmers] 자릿수 더하기"
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
    temp = list(str(n))
    answer = list(map(int, temp))

    return sum(answer)
~~~
