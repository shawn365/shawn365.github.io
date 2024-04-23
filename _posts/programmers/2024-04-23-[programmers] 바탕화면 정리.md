---
title: "[Programmers] 바탕화면 정리"
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
def solution(wallpaper):
    x = []
    y = []
    for i in range(len(wallpaper)):
        for j in range(len(wallpaper[i])):
            if wallpaper[i][j] == "#":
                y.append(i)
                x.append(j)

    return [min(y), min(x), max(y) + 1, max(x) + 1]
```
