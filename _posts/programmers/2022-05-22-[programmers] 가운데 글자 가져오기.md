---
title: "[Programmers] 가운데 글자 가져오기"
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
    if len(s) % 2 != 0:
        return s[int(len(s)/2)]
    else:
        return s[int(len(s)/2) - 1:int(len(s)/2) + 1]
~~~
