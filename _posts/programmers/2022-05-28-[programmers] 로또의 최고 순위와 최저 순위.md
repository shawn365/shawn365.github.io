---
title: "[Programmers] 로또의 최고 순위와 최저 순위"
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
def solution(lottos, win_nums):
    answer = [6,6,5,4,3,2,1]
    count = 0
    count_zero = 0
    for i in lottos:
        if i in win_nums:
            count += 1
        if i == 0:
            count_zero += 1
    
    return answer[count + count_zero], answer[count]
~~~
