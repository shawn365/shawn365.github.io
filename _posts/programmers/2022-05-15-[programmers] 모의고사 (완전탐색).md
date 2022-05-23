---
title: "[Programmers] 모의고사 (완전탐색)"
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
def solution(answers):
    result = []
    one = [1, 2, 3, 4, 5]
    two = [2, 1, 2, 3, 2, 4, 2, 5]
    three = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5]
    temps = [0, 0, 0]
    for answer in range(len(answers)):
        if one[answer % len(one)] == answers[answer]:
            temps[0] += 1
        if two[answer % len(two)] == answers[answer]:
            temps[1] += 1
        if three[answer % len(three)] == answers[answer]:
            temps[2] += 1
    for i, temp in enumerate(temps):
        if temp == max(temps):
            result.append(i + 1)
            
    return result
~~~
