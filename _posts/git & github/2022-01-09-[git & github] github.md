---
title: "[git & github] github"
categories:
  - git & github
tags:
  - [git & github, blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## Github 란
GitHub은 Git repository를 위한 호스팅 플랫폼입니다.

## Git vs GitHub
- Git은 버전 관리 시스템으로, 시간이 지남에 따라 파일의 변경 사항을 추적하는 도구입니다.
- GitHub은 Git을 사용하는 프로젝트를 위한 호스팅 서비스입니다.

## Using GitHub
1. 로컬에서 add / commit 한다.
2. Github 으로 이동 후 새 repository를 생성한다.
3. 나의 로컬 repository 를 GitHub repository 와 연결한다. (remote 추가)
4. 새 remote 를 이용하여 코드를 Push 한다.

## Repository 생성하기
GitHub repository 를 생성하려면, [github.com](https://github.com) 으로 이동 후 우측 상단 + 버튼을 누른 뒤 'New repository' 라는 옵션을 선택해주세요.  

<img class="img-fluid" src="/img/posts/repository.png" alt="print-image">

repository 를 생성하는 페이지에서 제일 먼저 Repository name 을 설정해주셔야 합니다.  

<img class="img-fluid" src="/img/posts/repository2.png" alt="print-image">

## Repository 에 코드 push 하기
'Create repository' 버튼을 누르게 되면 새로 만든 GitHub repository 의 스타팅 페이지로 이동하게 됩니다.  

<img class="img-fluid" src="/img/posts/repository3.png" alt="print-image">
~~~
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git push -u origin master
~~~
로컬환경에 이미 Git repository 가 있다면 위 명령어를 입력하면 됩니다.

## Repository 삭제하기
<img class="img-fluid" src="/img/posts/repository4.png" alt="print-image">
삭제하고 싶은 repository에서 settings를 눌러줍니다.  
맨 아래로 내려오면 삭제 버튼이 있습니다.
<img class="img-fluid" src="/img/posts/repository5.png" alt="print-image">

## repository 클론하기
clone 을 받아 내 로컬환경에 다운로드 후 프로젝트를 시작하는 방법은, repository 주소를 복사해주고
<img class="img-fluid" src="/img/posts/repository6.png" alt="print-image">

~~~
git clone <github-repo-link>
~~~

이 명령어와 함께 clone 뒤에 repository 주소를 치면 됩니다.  
clone 시점에 remote repository에 존재했던 모든 폴더 및 파일들이 그대로 복제되어 있는것을 확인할 수 있습니다.