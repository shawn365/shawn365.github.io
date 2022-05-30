---
title: "[Programmers] 3진법 뒤집기"
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
    answer = ''

    while n > 0:
        n, remainder = divmod(n,3)
        answer += str(remainder)
    return int(answer, 3)
~~~
