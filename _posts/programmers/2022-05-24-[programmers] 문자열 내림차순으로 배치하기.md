---
title: "[Programmers] 문자열 내림차순으로 배치하기"
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
def solution(s):
    answer = "".join(sorted(s, reverse = True))
    return answer
~~~
