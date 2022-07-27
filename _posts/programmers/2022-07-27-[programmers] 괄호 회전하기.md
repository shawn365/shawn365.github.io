---
title: "[Programmers] 괄호 회전하기"
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
import collections
def solution(s):
    answer = 0
    q: deque = collections.deque(s)
    table = {
            ')' : '(',
            '}' : '{',
            ']' : '[',
        }
    
    for i in s:
        boolean = True
        temp = []        
        for j in q:
            if j not in table:
                temp.append(j)
            elif not temp or table[j] != temp.pop():
                boolean = False
                break
        if boolean == True and not temp:
            answer += 1        
        q.append(q.popleft())
        
    return answer
~~~
