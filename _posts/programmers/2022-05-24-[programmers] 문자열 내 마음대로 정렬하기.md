---
title: "[Programmers] 문자열 내 마음대로 정렬하기"
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
def solution(strings, n):
    return sorted(strings, key = lambda x : (x[n], x))
~~~
