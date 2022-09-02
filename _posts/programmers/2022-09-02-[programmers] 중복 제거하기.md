---
title: "[Programmers] 중복 제거하기"
categories:
  - Programmers
tags:
  - [Programmers, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## SQL
~~~sql
SELECT count(distinct name) 
FROM ANIMAL_INS  
WHERE NAME IS NOT NULL
~~~