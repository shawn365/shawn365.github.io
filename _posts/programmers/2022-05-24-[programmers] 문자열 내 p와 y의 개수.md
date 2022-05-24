---
title: "[Programmers] 문자열 내 p와 y의 개수"
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
    if s.lower().count('p') == 0 and s.lower().count('y') == 0:
        return True
    
    if s.lower().count('p') == s.lower().count('y'):
        return True
    
    else:
        return False
~~~
