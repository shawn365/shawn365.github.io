---
title: "[Programmers] 나머지가 1이 되는 수 찾기"
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
    for i in range(1, n):
        if n % i == 1:
            return i
~~~
