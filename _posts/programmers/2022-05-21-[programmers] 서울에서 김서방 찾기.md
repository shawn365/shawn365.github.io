---
title: "[Programmers] 서울에서 김서방 찾기"
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
def solution(seoul):
    for i in range(len(seoul)):
        if seoul[i] == 'Kim':
            return f'김서방은 {i}에 있다'
~~~
