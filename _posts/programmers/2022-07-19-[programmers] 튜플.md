---
title: "[Programmers] 튜플"
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
    answer = []
    temp = sorted([s.split(',') for s in s[2:-2].split('},{')], key = len)
    for i in temp:
        for j in i:
            if int(j) not in answer:
                answer.append(int(j))
    
    return answer
~~~
