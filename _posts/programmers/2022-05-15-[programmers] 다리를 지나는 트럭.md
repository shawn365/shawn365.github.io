---
title: "[Programmers] 다리를 지나는 트럭"
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
def solution(bridge_length, weight, truck_weights):
    answer = 0
    q = [0] * bridge_length
    while q:
        answer += 1
        q.pop(0)
        if truck_weights:
            if sum(q) + truck_weights[0] <= weight:
                q.append(truck_weights.pop(0))
            else:
                q.append(0)
        
    return answer
~~~
