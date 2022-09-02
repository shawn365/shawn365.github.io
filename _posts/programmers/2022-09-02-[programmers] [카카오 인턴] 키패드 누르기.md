---
title: "[Programmers] [카카오 인턴] 키패드 누르기"
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
def solution(numbers, hand):
    answer = ''
    phone = {1:(0, 0), 2:(0, 1), 3:(0, 2),
             4:(1, 0), 5:(1, 1), 6:(1, 2),
             7:(2, 0), 8:(2, 1), 9:(2, 2),
           '*':(3, 0), 0:(3, 1), '#':(3, 2)}
    left, right = '*', '#'
    for number in numbers:
        if number in [1, 4, 7]:
            answer += "L"
            left = number
        elif number in [3, 6, 9]:
            answer += "R"
            right = number
        else:
            dist_l = abs(phone[left][0] - phone[number][0]) + abs(phone[left][1] - phone[number][1])
            dist_r = abs(phone[right][0] - phone[number][0]) + abs(phone[right][1] - phone[number][1])
            if dist_l > dist_r:
                answer += "R"
                right = number
            elif dist_l < dist_r:
                answer += "L"
                left = number
            else:
                if hand == "right":
                    answer += "R"
                    right = number
                else:
                    answer += "L"
                    left = number
    
    return answer
~~~