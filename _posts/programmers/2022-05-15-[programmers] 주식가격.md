---
title: "[Programmers] 주식가격"
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
def solution(prices):
    answer = []
    q: deque = collections.deque(prices)
    while q:
        count = 0
        temp = q.popleft()
        for i in q:
            count += 1
            if temp > i:
                break
        answer.append(count)
    return answer
~~~
