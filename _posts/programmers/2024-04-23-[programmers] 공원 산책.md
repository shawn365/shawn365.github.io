---
title: "[Programmers] 공원 산책"
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
def solution(park, routes):
    row = col = 0

    for i, row_value in enumerate(park):
        if 'S' in row_value:
            row = i
            col = row_value.index('S')
            break

    for route in routes:
        direction, steps = route.split()
        steps = int(steps)

        start_row, start_col = row, col

        for _ in range(steps):
            if direction == "E":
                if col + 1 < len(park[row]) and park[row][col + 1] != "X":
                    col += 1
                else:
                    row, col = start_row, start_col
                    break
            elif direction == "S":
                if row + 1 < len(park) and park[row + 1][col] != "X":
                    row += 1
                else:
                    row, col = start_row, start_col
                    break
            elif direction == "W":
                if col - 1 >= 0 and park[row][col - 1] != "X":
                    col -= 1
                else:
                    row, col = start_row, start_col
                    break
            elif direction == "N":
                if row - 1 >= 0 and park[row - 1][col] != "X":
                    row -= 1
                else:
                    row, col = start_row, start_col
                    break

    return [row, col]
```
