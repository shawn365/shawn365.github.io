---
title: "[Programmers] 소수 찾기 (완전탐색)"
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
def is_prime_number(a):
    if(a<2):
        return False
    for i in range(2,a):
        if(a%i==0):
            return False
        
    return True
    
def solution(numbers):
    answer = 0
    temp = []
    for i in range(1, len(numbers) + 1):
        permutation = permutations(numbers, i)
        for j in permutation:
            temp.append(int(''.join(j)))
    for t in set(temp):
        if is_prime_number(t):
            answer += 1
            
    return answer
~~~
