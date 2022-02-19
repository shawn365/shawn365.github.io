---
title: "[python] django"
categories:
  - python
tags:
  - [python, blog, django]
toc: true
toc_sticky: true
toc_label: "목차"
---

## 1. Django란?
Djano란 웹사이트를 신속하게 개발하는 하도록 도움을 주는 파이썬 웹 프레임워크입니다.

## 2. Framework vs Library
프레임워크는 전체적인 흐름을 자체적으로 가지고 있고 사용자는 그 안에서 필요한 코드를 짜 넣으며 반면에 라이브러리는 사용자가 전체적인 흐름을 만들며 필요한 라이브러리를 가져다 쓰는 것이라고 할 수 있습니다.

## 3. MVT
웹 프로그램 개발시 일반적으로 언급되는 MVC (model view controller)패턴이란 데이터(Model), 사용자(View), 데이터를 처리하는 로직(Controller)을 구분해서 한 요소가 다른 요소들에 영향을 주지 않도록 설계하는 방식입니다.  
파이썬도 이러한 MVC개념을 그대로 받아들였는데, 용어는 다르게 사용하고 있습니다.  
Django framework에서는 View를 Template, Controller는 View라고 표현하며, MVC를 MVT 패턴이라고 합니다.
- Models: 모델은 Django가 처리하는 데이터 구조를 정의하고 데이터베이스의 기록을 관리(추가, 수정, 삭제) 합니다
- View: 뷰는 HTTP 요청을 수신하고 HTTP 응답을 반환하는 요청 처리 함수입니다. 뷰는 Model을 통해 요청을 충족시키는데 필요한 데이터에 접근합니다. 그리고 탬플릿에게 응답의 결과를 전달합니다.
- Template: 템플릿은 사용자에게 보여지는 UI부분을 의미합니다.
