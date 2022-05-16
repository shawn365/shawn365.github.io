---
title: "[Programmers] 콜라츠 추측"
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
def solution(num):
    answer = 0
    while num != 1:
        answer += 1
        if answer == 500:
            return -1
        if num % 2 == 0:
            num /= 2
        else:
            num = num * 3 + 1
    
    return answer
~~~
