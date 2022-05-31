---
title: "[Programmers] K번째수"
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
def solution(array, commands):
    answer = []
    for command in commands:
        temp = sorted(array[command[0] - 1:command[1]])
        answer.append(temp[command[2] - 1])
        
    return answer
~~~
