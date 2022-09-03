---
title: "[Programmers] 오랜 기간 보호한 동물(2)"
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
SELECT I.ANIMAL_ID, I.NAME
FROM ANIMAL_INS AS I, ANIMAL_OUTS AS O
WHERE I.ANIMAL_ID = O.ANIMAL_ID
ORDER BY O.DATETIME - I.DATETIME DESC
LIMIT 2
~~~