---
title: "[Project] 1차 프로젝트 회고록"
categories:
  - Project
tags:
  - [Project, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

<img class="img-fluid" src="/img/posts/kikea.png" alt="print-image">

## 1. 프로젝트 소개
홈 퍼니싱 제품 판매 기업 이케아 클론 프로젝트
- [유튜브 시연 영상](https://www.youtube.com/watch?v=2w99doEHCzE&feature=youtu.be)
- [백엔드 깃허브](https://github.com/wecode-bootcamp-korea/29-1st-KIKEA-backend)
- [프론트 깃허브](https://github.com/wecode-bootcamp-korea/29-1st-KIKEA-frontend)
### 1-1. 개발 기간
22.01.24 ~ 22.02.11

### 1-2. 개발 인원
- 백엔드 - 김성수, 주다희
- 프론트 엔드 - 신수녕, 문지원, 박혜린

### 1-3. 백엔드 기술 스택
- 언어: Python
- 웹 프레임 워크: Django
- 데이터 베이스: MySQL

## 2. 내가 구현한 기능
- 회원가입 및 로그인
- 정규 표현식을 통한 아이디 및 비밀번호 유효성 검사
- Bycrpt를 이용한 비밀번호 암호화 및 JWT 발급
- 요청 헤더에 담긴 토큰을 통해 로그인 여부를 검사하는 데코레이터 구현
- 프론트에서 넘어오는 Query String에 따라 Q객체를 이용해 판매 상품 조회, 조건에 따른 필터링, 정렬 기능 구현
- 특정 상품에 대한 상세 정보 데이터 제공
- 제품 리뷰 작성 기능 구현 및 평균 리뷰 점수, 총 리뷰 갯수 구현

## 3. 잘한점
- 프론트엔드와 통신을 빠르게 시작하고 Postman을 이용해서 만들어진 Api Url을 공유했다
- 역할 분담을 잘 해놔서 개발도중 Merge 과정에서 문제가 안생겼었다
- 백엔드간 소통을 통해 지식이나 막히는 부분에서 서로 도와가면서 프로젝트를 진행했다

## 4. 아쉬웠던 점
- 프로젝트를 진행하면서 Modeling을 수정해야되는 경우가 많아서 기능구현을 할시간에 Modeling에 시간을 많이 빼았겼다
- 소통을 많이 했다고 생각 했지만 통신을 해보니 소통이 부족했었다, 프론트에서 생각하는 기능과 내가 생각하는 기능에 차이가 조금 있어서 수정하는데 시간을 많이 썼다