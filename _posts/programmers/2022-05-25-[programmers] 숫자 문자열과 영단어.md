---
title: "[Programmers] 숫자 문자열과 영단어"
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
    temp = ['zero', 'one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', 'nine']
    for i in temp:
        s = s.replace(i, str(temp.index(i)))
    return int(s)
~~~
