---
title: "[programmers] 평균 구하기"
categories:
  - programmers
tags:
  - [programmers, blog]
toc: true
toc_sticky: true
toc_label: "목차"
---
~~~java
class Solution {
    public double solution(int[] arr) {
        double answer = 0;
        for(int i = 0; i < arr.length; i++){
            answer += arr[i];
        }
        return answer/arr.length;
    }
}
~~~