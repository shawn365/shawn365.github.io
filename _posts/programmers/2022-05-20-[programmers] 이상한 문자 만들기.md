---
title: "[Programmers] 이상한 문자 만들기"
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
def solution(s):
    answer = ''
    temps: list = s.split(' ')
    for temp in temps:
        for i in range(len(temp)):
            if i % 2 == 0:
                answer += temp[i].upper()
            else:
                answer += temp[i].lower()
        answer += ' '
        
    return answer[:-1]
~~~
