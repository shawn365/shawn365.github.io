---
title: "[git & github] git command"
categories:
  - git & github
tags:
  - [git & github, blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## 1. Initializing a repository
~~~
git init
~~~
이 명령어는 프로젝트 폴더 내에 숨겨진 .git 디렉토리를 생성하고 이 Git은 현재 저장소에 대한 모든 변경사항을 추적/관리하게 됩니다.

## 2. Checking the status
~~~
git status
~~~
이 명령어는 어떤 파일이 변경되었는지, 어떤 파일이 추가되었는지 등을 전부 보여줍니다.

## 3. Staging files
~~~
git add
~~~
이 명령어를 통해 원하는 파일들을 staging area 로 추가해줄 수 있습니다.  
아래와 같이 특정 파일만 추가할 수 있습니다.
~~~
git add file.py
~~~
여러개의 파일들을 추가하고 싶다면
~~~
git add file.py file2.py file3.py
~~~
파일을 각각 추가하지 않고 한번에 추가하고 싶다면
~~~
git add .
~~~

## 4. Making commits
~~~
git commit -m "commit message"
~~~
이 명령어를 통해 staging area에 있는 파일들을 커밋할 수 있습니다.  
식별을 위해 큰 따옴표안에 커밋 메세지를 작성해야 합니다.  
커밋 메시지는 repository에 커밋하는 변경 사항을 설명하는 짧은 summary 여야 합니다.

## 5. Commit history
~~~
git log
~~~
이 명령어는 프로젝트의 모든 커밋 내역을 보여줍니다.  
git log 명령어를 통해 보여지는 log는 각 커밋에 대한 자세한 정보를 담고 있습니다. (작성자, hash 값, 날짜와 시간, 그리고 커밋 메세지)  
만약 특정 커밋 시점의 코드로 되돌리고 싶다면, 아래 명령어를 사용할 수 있습니다.
~~~
git checkout <commit-hash>
~~~

## 6. Ignoring files
staging area 에 추가하고 싶지 않거나, git 에서 관리하지 않아도 되는 파일이 있다면, .gitignore 파일을 프로젝트 폴더에 생성해주시면 됩니다.  
.gitignore 파일 안에, 해당하는 파일명과 폴더명을 나열하면 됩니다.  
각 파일, 폴더가 새로운 줄에 입력되어야 합니다.

## 7. Creating a new branch
브랜치란 독립적으로 어떤 작업을 진행하기 위해 필요합니다.  
필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 여러 작업을 동시에 진행할 수 있습니다.
~~~
git branch <new-branch-name>
~~~
이 명령어를 통해 새로운 브랜치를 생성할 수 있습니다.

## 8. Changing branches
~~~
git checkout <branch-name>
~~~
이 명령어를 통해 다른 브랜치로 이동할 수 있습니다.  
브랜치가 전환 되었으므로 이후에 남기는 커밋은 전환한 브랜치에 추가됩니다.  
작업한 내용은 해당 브랜치에만 영향을 주게 됩니다.  
그런 다음 다른 브랜치로 이동하여 작업 할 수 있으며, 이전 브랜치의 변경 사항 및 커밋의 영향을 받지 않습니다.  


브랜치 생성과 동시에 생성된 브랜치로 이동하고 싶다면 기존 checkout 명령어에 -b 라는 flag 를 추가해주면 됩니다.
~~~
git checkout -b <new-branch-name>
~~~

## 9. Checking all branches
프로젝트에 존재하는 모든 브랜치를 확인하고 싶다면 이 명령어를 입력하면 됩니다.
~~~
git branch
~~~

## 10. Merging branches
A 라는 브랜치에서 작업한 내용을 B 라는 브랜치에 적용하고 싶을 때, 브랜치 A 와 브랜치 B 를 병합(merge) 할 수 있습니다.  
아래 명령어를 통해 다른 브랜치를 현재 브랜치와 병합할 수 있습니다.
~~~
git merge <branch-name>
~~~

## 11. Deleting a branch
아래 명령어를 통해, 브랜치를 삭제할 수 있습니다. 
~~~
git branch -d <branch-name>
~~~