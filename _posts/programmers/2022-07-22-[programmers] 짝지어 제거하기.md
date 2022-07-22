---
title: "[Programmers] 짝지어 제거하기"
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
    for i in range(len(s)):
        if len(temp) == 0:
            temp.append(s[i])
        elif s[i] == temp[-1]:
            temp.pop()
        else:
            temp.append(s[i])
    
    if temp:
        return 0
    else:
        return 1
~~~
