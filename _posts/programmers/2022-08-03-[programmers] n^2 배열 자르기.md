---
title: "[Programmers] n^2 배열 자르기"
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
def solution(n, left, right):
    answer = []
    for i in range(left, right+1):
        answer.append(max(divmod(i, n)) + 1)

    return answer
~~~