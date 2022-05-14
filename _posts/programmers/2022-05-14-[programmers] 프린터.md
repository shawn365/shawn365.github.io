---
title: "[Programmers] 프린터"
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
def solution(priorities, location):
    answer = 0
    q: deque = collections.deque([(v, i) for i, v in enumerate(priorities)])
    
    while q:
        temp = q.popleft()
        if q and temp[0] < max(q)[0]:
            q.append(temp)
        else:
            answer += 1
            if temp[1] == location:
                return answer
~~~
