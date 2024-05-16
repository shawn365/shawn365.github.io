---
title: "[Programmers] 둘만의 암호"
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
def solution(s, skip, index):
    answer = ''
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    for i in skip:
        alphabet = alphabet.replace(i, '')

    for i in s:
        idx = (alphabet.index(i) + index) % len(alphabet)
        answer += alphabet[idx]

    return answer
```
