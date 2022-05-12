---
title: "[Python] sys.modules, sys.path"
categories:
  - Python
tags:
  - [Python, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## 1. sys.module

+ 파이썬이 제일 먼저 모듈이나 패키지를 찾는곳
+ 단순한 딕션너리 구조 그리고 이미 import된 모듈과 package들을 저장
+ 즉 한번 import된 모듈과 패키지를 다시 안 찾아도 된다
+ 새로 import 하는 모듈은 sys.modules 에서 찾을 수 없다


## 2. sys.path

+ 마지막으로 보는 장소가 바로 sys.path 이다
+ sys.path는 기본적으로 list이며 string 요소들을 가지고 있는 list 이다
+ 각 string 요소들은 경로를 나타내는데 list의 각 경로를 하니식 확인하면서 해당 경로에 import 하고자 하는 package가 위치해 있는지 확인한다 (e.g. '/Users/shawn/anaconda3/bin')
+ 만약 마지막으로 보는 장소인 sys.path 에서도 못찾으면 ModuleNotFoundError 에러를 리턴한다

---
Python에서는 아래와 같은 순서로 module/package를 찾는다.

+ sys.modules => built-in modules => sys.path

