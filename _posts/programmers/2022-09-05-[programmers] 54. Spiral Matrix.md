---
title: "[Programmers] 54. Spiral Matrix"
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
class Solution:
    def spiralOrder(self, matrix: List[List[int]]) -> List[int]:
        answer = []
        while matrix:
            answer += matrix.pop(0)
            if matrix and matrix[0]:
                for i in matrix:
                    answer.append(i.pop())
            if matrix:
                answer += matrix.pop()[::-1]
            if matrix and matrix[0]:
                for i in matrix[::-1]:
                    answer.append(i.pop(0))
        
        return answer
~~~