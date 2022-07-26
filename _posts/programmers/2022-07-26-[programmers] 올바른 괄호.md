---
title: "[Programmers] 올바른 괄호"
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
    temp = []
    
    for i in s:
        if not temp:
            temp.append(i)
        elif temp[-1] == '(' and i == ')':
            temp.pop()
        else:
            temp.append(i)
            
    if temp:
        return False
    else:
        return True
~~~
