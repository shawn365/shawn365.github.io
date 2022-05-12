---
title: "[Programmers] x만큼 간격이 있는 n개의 숫자"
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
def solution(x, n):
    sum = 0
    answer = []
    for i in range(n):
        sum += x
        answer.append(sum)
    return answer
~~~

## Java
~~~java
class Solution {
    public long[] solution(int x, int n) {
        long[] answer = new long[n];
        long num = x;
        for(int i = 0; i < n; i++) {
            answer[i] = num * (i + 1);
        }
        return answer;
    }
}
~~~

## Javascript
~~~javascript
function solution(x, n) {
    var answer = [];
    let sum = 0;
    for(let i = 0; i < n; i++) {
        sum += x;
        answer.push(sum);
    }
    return answer;
}
~~~