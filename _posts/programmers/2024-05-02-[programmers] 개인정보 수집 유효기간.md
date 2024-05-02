---
title: "[Programmers] 개인정보 수집 유효기간"
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
def cal(date):
    year, month, day = map(int, date.split('.'))
    return year * 12 * 28 + month * 28 + day

def solution(today, terms, privacies):
    answer = []
    term_dict = {}
    for i in terms:
        term, month = i.split()
        term_dict[term] = int(month) * 28

    for idx, privacy in enumerate(privacies):
        date, term = privacy.split(" ")
        temp = cal(date) + term_dict[term]
        if temp <= cal(today):
            answer.append(idx + 1)

    return answer
```
