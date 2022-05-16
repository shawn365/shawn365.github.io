---
title: "[Programmers] 하샤드 수"
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
def solution(x):
    arr : list = list(str(x))
    sum= 0
    
    for i in arr:
        sum += int(i)
        
    if x % sum == 0:
        return True
    
    return False
~~~
