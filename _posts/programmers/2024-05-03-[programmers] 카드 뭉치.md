---
title: "[Programmers] 카드 뭉치"
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
def solution(cards1, cards2, goal):
    answer = ''
    card1 = 0
    card2 = 0
    for i in goal:
        if card1 < len(cards1) and i == cards1[card1]:
            card1 += 1
        elif card2 < len(cards2) and i == cards2[card2]:
            card2 += 1
        else:
            return "No"

    return "Yes"
```
