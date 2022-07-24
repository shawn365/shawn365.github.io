---
title: "[Programmers] 피로도"
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
from itertools import permutations
def solution(k, dungeons):
    answer = 0
    for dungeon in permutations(dungeons):
        num = k
        count = 0
        for i in dungeon:
            if num >= i[0]:
                num -= i[1]
                count += 1
                answer = max(count, answer)
            
    return answer
~~~
