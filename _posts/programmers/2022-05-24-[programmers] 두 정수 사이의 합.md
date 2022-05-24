---
title: "[Programmers] 두 정수 사이의 합"
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
    if a < b :
        return sum(list(range(a, b + 1)))
    else:
        return sum(list(range(b, a + 1)))
~~~
