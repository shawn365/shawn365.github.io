---
title: "[Programmers] 핸드폰 번호 가리기"
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
def solution(phone_number):
    answer = '*' * (len(phone_number) - 4) + phone_number[-4:]

    return answer
~~~
