---
title: "[git & github] commit 수정"
categories:
  - git & github
tags:
  - [git & github, blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

## 1. 마지막 커밋을 수정하기
마지막 커밋을 수정하려면 아래 명령어를 치면 된다
~~~
git commit --amend
~~~

## 2. 커밋 합치기
최근 커밋이 아니라 예전 커밋을 수정하려면 rebase 명령을 이용하면 된다 git rebase 명령에 -i 옵션을 추가하면 대화형 모드로 Rebase 할 수 있다.
~~~
git rebase -i HEAD~
~~~
명령어를 실행하면 Git은 수정하려는 커밋 목록이 첨부된 스크립트를 텍스트 편집기로 열어준다.
~~~
pick b91e257 first commit
pick 0118d46 second commit
pick 1f199b7 third commit

# Rebase 710f0f8..a5f4a0d onto 710f0f8
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
~~~
3개의 커밋을 하나로 합치려면 sqaush를 이용하면 된다.
~~~
pick b91e257 first commit
s 0118d46 second commit
s 1f199b7 third commit
~~~
저장하고 나서 편집기를 종료하면 Git은 3개의 커밋 메시지를 Merge 할 수 있도록 에디터를 바로 실행해준다.
~~~
# This is a combination of 3 commits.
# This is the 1st commit message:

first commit

# This is the commit message #2:

second commit

# This is the commit message #3:

third commit
~~~
이 메시지를 저장하면 3개의 커밋이 모두 합쳐진 커밋 한 개만 남는다. (메시지는 원하는데로 바꾸고 저장할수도 있다)

## 3. rebase중 문제가 생겼을때
rebase중 뭔가를 잘못해서 다시 rebase전으로 되돌려야 할때는 이 명령어를 치면 된다
~~~
git rebase --abort
~~~

## 4. rebase중 conflict가 발생했을때
conflict 가 발생한 파일을 수정하고 git add 를 사용하여 수정된 파일을 추가해 준다 그런후 아래 명령어를 치면 rebase과정을 계속 진행할수 있다.
~~~
git rebase --continue
~~~
