---
title: "[Programmers] 최댓값과 최솟값"
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
    arr = list(map(int, s.split(' ')))
    
    return str(min(arr)) + " " + str(max(arr))
~~~
