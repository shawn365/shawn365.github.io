---
title: "[Programmers] 더 맵게"
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
import heapq
def solution(scoville, K):
    answer = 0
    heapq.heapify(scoville)
    while scoville[0] < K:
        temp = heapq.heappop(scoville) + heapq.heappop(scoville) * 2
        heapq.heappush(scoville, temp)
        answer += 1
        if len(scoville) == 1 and scoville[0] < K:
            return -1
        
    return answer
~~~
