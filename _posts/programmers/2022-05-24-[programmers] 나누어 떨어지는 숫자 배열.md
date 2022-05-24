---
title: "[Programmers] 나누어 떨어지는 숫자 배열"
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
def solution(arr, divisor):
    answer = []
    for i in arr:
        if i % divisor == 0:
            answer.append(i)
    if answer:
        return sorted(answer)
    else:
        return [-1]
~~~
