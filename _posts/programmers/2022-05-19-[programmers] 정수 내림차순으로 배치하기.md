---
title: "[Programmers] 정수 내림차순으로 배치하기"
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
    temp.sort(reverse = True)
    return int("".join(temp))
~~~
