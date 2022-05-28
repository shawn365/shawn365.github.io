---
title: "[Programmers] 없는 숫자 더하기"
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
    answer = 0
    temp = [0,1,2,3,4,5,6,7,8,9]
    for i in temp:
        if i not in numbers:
            answer += i
            
    return answer
~~~
