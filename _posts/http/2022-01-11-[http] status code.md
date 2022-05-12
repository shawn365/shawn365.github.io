---
title: "[HTTP] Status Code"
categories:
  - HTTP
tags:
  - [HTTP, Blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## 1. 200: OK
가장 자주 보게되는 Status Code  
문제없이 요청에 대한 처리가 백엔드 서버에서 이루어지고 나서 오는 응답코드

## 2. 201: Created
무언가가 잘 생성되었을 때에(Successfully Created) 오는 Status Code  
대게 POST 메소드의 요청에 따라 백엔드 서버에 데이터가 잘 생성 또는 수정 되었을 때에 보내는 코드

## 3. 400: Bad Request
해당 요청이 잘못되었을 때 보내는 Status Code  
주로 요청의 Body에 보내는 내용이 잘못되었을 때 사용되는 코드

## 4. 401: Unauthorized
유저가 해당 요청을 진행하려면 먼저 로그인을 하거나 회원가입이 필요하다는 의미 

## 5. 403: Forbidden
유저가 해당 요청에 대한 권한이 없다는 뜻  
접근 불가능한 정보에 접근했을 경우

## 6. 404: Not Found
요청된 URI 가 존재하지 않는다는 의미

## 7. 500: Internal Server Error
서버에서 에러가 났을 때의 Status Code