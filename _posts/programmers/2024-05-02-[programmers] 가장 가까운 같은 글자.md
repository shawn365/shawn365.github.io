---
title: "[Programmers] 가장 가까운 같은 글자"
categories:
  - Programmers
tags:
  - [Programmers, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## Python

```python
def solution(s):
    answer = []
    s_lst = []
    for idx, val in enumerate(s):
        temp = 0
        if val in s_lst:
            for j in range(idx):
                if val == s[j]:
                    temp = j
            answer.append(idx - temp)

        else:
            s_lst.append(val)
            answer.append(-1)

    return answer
```
