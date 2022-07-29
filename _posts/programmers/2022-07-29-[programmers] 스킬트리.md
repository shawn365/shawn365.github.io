---
title: "[Programmers] 스킬트리"
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
def solution(skill, skill_trees):
    answer = 0
    for skills in skill_trees:
        temp = list(skill)
        boolean = True
        for j in skills:
            if j in temp:
                if j != temp.pop(0):
                    boolean = False
                    break
        if boolean:
            answer += 1
        
    return answer
~~~
