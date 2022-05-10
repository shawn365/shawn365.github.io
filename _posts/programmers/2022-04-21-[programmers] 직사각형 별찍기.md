---
title: "[programmers] 직사각형 별찍기"
categories:
  - programmers
tags:
  - [programmers, blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

##Python
~~~python
a, b = map(int, input().strip().split(' '))
for i in range(b):
    for j in range(a):
        print('*', end='')
    print();
~~~

##Java
~~~java
import java.util.Scanner;

class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        for(int i = 0; i < b; i++){
            for(int j = 0; j < a; j++){
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
~~~

##javascript
~~~javascript
process.stdin.setEncoding('utf8');
process.stdin.on('data', data => {
    const n = data.split(" ");
    const a = Number(n[0]), b = Number(n[1]);
    let answer = "";
    for (let i = 0; i < b; i++) {
        for (let j = 0; j < a; j++) {
            answer += "*";
        }
        answer += "\n";
    }
    console.log(answer);
});
~~~