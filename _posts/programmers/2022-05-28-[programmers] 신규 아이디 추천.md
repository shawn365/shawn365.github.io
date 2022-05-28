---
title: "[Programmers] 신규 아이디 추천"
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
import re
def solution(new_id):
    answer = new_id.lower()
    answer = re.sub('[^a-z0-9-_.]', '',answer)
    answer = re.sub('[\.]+', '.', answer)
    answer = answer.strip('.')
    if answer =='':
        answer='a'
    answer = answer[:15].rstrip('.')
    answer += answer[-1] * (3 - len(answer))
        
    return answer
~~~
