---
title: "[Programmers] H-Index"
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
def solution(citations):
    citations.sort()
    for i in range(len(citations)):
        if citations[i] >= len(citations) - i:
            return len(citations) - i
            
    return 0
~~~