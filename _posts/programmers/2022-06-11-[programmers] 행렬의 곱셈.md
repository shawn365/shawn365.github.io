---
title: "[Programmers] 행렬의 곱셈"
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
def solution(arr1, arr2):
    answer = []
    for i in range(len(arr1)):
        list = []
        for j in range(len(arr2[0])):
            temp = 0
            for k in range(len(arr2)):
                temp += arr1[i][k] * arr2[k][j]
            list.append(temp)
        answer.append(list) 
        
    return answer
~~~
