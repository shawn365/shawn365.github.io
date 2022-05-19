---
title: "[Programmers] 자연수 뒤집어 배열로 만들기"
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
    answer =list(str(n))
    answer.reverse()
    return list(map(int, answer))
~~~
