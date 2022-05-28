---
title: "[Programmers] 크레인 인형뽑기 게임"
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
def solution(board, moves):
    answer = 0
    temp = []
    for i in moves:
        for j in board:
            if j[i - 1] != 0:
                if temp and temp[-1] == j[i - 1]:
                    answer += 1
                    temp.pop()
                else:
                    temp.append(j[i - 1])
                j[i - 1] = 0
                break
                
    return answer * 2
~~~
