---
title: "[Programmers] 가장 큰 수"
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
def solution(numbers):
    number = list(map(str, numbers))
    number.sort(key = lambda x : x * 3, reverse = True)
    
    return str(int(''.join(number)))
~~~