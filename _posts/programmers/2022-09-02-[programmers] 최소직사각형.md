---
title: "[Programmers] 최소직사각형"
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
def solution(sizes):
    answer = 0
    min_size, max_size = [], []
    for size in sizes:
        min_size.append(min(size[0], size[1]))
        max_size.append(max(size[0], size[1]))
        
    return max(min_size) * max(max_size)
~~~