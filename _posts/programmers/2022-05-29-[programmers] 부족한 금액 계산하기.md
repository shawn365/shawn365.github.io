---
title: "[Programmers] 부족한 금액 계산하기"
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
def solution(price, money, count):
    answer = 0
    for i in range(1, count + 1):
        answer += price * i
        
    if answer - money >= 0:
        return answer - money
    else:
        return 0
~~~
