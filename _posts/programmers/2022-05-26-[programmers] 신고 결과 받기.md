---
title: "[Programmers] 신고 결과 받기"
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
import collections
def solution(id_list, report, k):
    answer = [0] * len(id_list)
    temps = collections.defaultdict(list)
    count_report = collections.defaultdict(int)
    suspended = []
    report = set(report)
    
    for i in report:
        user_id, report_id = i.split(' ')
        count_report[report_id] += 1
        temps[user_id].append(report_id)
        if count_report[report_id] == k:
            suspended.append(report_id)
    
    for i in suspended:
        for j in range(len(id_list)):
            if i in temps[id_list[j]]:
                answer[j] += 1
    
    return answer
~~~
