---
title: "[Programmers] 큰 수 만들기"
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
def solution(number, k):
    answer = []    
    for i in number:
        while k > 0 and answer and answer[-1] < i:
            answer.pop()
            k -= 1
        answer.append(i)
        
    return ''.join(answer[:len(answer) - k])
~~~