---
title: "[Programmers] 기능개발"
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
def solution(progresses, speeds):
    answer = []
    day = 0
    count = 0
    
    while len(progresses) > 0:
        if progresses[0] + speeds[0] * day >= 100:
            progresses.pop(0)
            speeds.pop(0)
            count += 1
            
        else:
            day += 1
            if count > 0:
                answer.append(count)
                count = 0
    answer.append(count)
    
    return answer
~~~
