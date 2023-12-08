---
layout: single
title: "깃 저장소 관리"
categories: Git
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---

# 깃 저장소 관리[^1]


1. ## git init - 깃 초기화(Initialized empty Git repository)[^2]

   -> .git 숨김 디렉터리[^3] 생겨나며, 버전이 저장될 repository 역할을 가져감.
   
   

2. ## 작업트리 / 스테이지 / 리포지토리

   - 작업 트리에서 문서 작업 후 스테이지로 넘겨 커밋을 통해 리포지토리로 넘어가는 형태

   - 커밋을 하기전에 스테이지에 저장을 함.(커밋될 예정인 내용)

   - Staging Area(스테이지) = Working Directory에서 제출된 파일들을 관리 및 임시로 저장하는 공간.(실제로 저장/기록 공간 이전의 임시공간), 파일 컨텐츠 내용을 직접 가지고 있는 것이 아닌 ‘커밋 하려는 파일의 추적 상태 정보들만 기록’

     

3. ## git status / git diff

   - git status : 깃 상태를 나타내는 메시지

   - git log : 커밋 기록 자세히 살펴보기 (커밋한 버전 정보 확인)

   - git diff : 변경 사항 확인하기(최신 버전과의 비교)

     

4. ## git log

   - --stat : 상세변경(변경된 파일 목록 / 변경된 파일 내 변경량) 

   - --oneline : 한 줄에 한 커밋씩 나타내주며, 커밋 간략히 확인할때 사용(브랜치 구분) [^4]

   - --oneline --branches : 각 브랜치의 커밋을 함께 볼 수 있음.

   - --oneline --branches --graph : 브랜치,커밋관계를 그래프 형태로 표시

   - git log 브랜치이름..브랜치이름 : 브랜치 이름 사이에 마침표 두 개 ‘..’를 넣는 명령으로 차이점을 쉽게 확인가능.

     (마침표 왼쪽에 있는 브랜치를 기준으로 오른쪽 브랜치와 비교)
     
     

5. ## git add / git commit / git commit -am(-a -m) / git checkout

   - git add : Git에게 버전 만들 준비를 하라고 알려주는 스테이징[^5]

   - git commit : 스테이지에 올라온 파일 커밋하기[^6]

     \> -m “msg” : 커밋과 함께 적용할 메시지

     - git commit -am “msg” : 스테이지 + 커밋 과정을 한꺼번에.

       (다만, 한 번이라도 커밋한 적이 이는 파일을 다시 커밋할때만 가능)

       \>“msg” : 커밋과 함께 적용할 메시지

   - git checkout(스테이징 하기전) -- 파일명 : 작업 트리 수정 파일 되돌리기[^7]

     (다만, checkout은 최신 버전에서는 잘 안쓰이는 방법 인듯함.

     애초에 checkout에 관련된 명령어 안내가 제공되지 않고 있고, restore를 이용한 안내가 CLI화면에서 제공되어 있음.)[^8]

   - git reset HEAD 파일명 : 스테이징 되돌리기

     (다만 이것도 요새 잘 안 쓰이는 추세 같음.[^9])

   - git reset HEAD^ : 스테이징하고 커밋까지 진행했을때, 커밋까지한 내용 되돌리기[^10]
   
   - git reset --hard [commit hash] : 해당 커밋해시의 특정 커밋으로 되돌리기(git log를 이용해서 추출-중간 커밋들은 모두 삭제됨.)
   
   - git revert [commit hash] : 위 방법 과는 다르게 해당 커밋 해시의 특정 커밋으로 되돌리되, 중간 커밋들이 삭제되지 않고 log에 남은채로 존재함.(즉, revert 방법으로 돌리는 것은 뒤는 돌아볼 수 있도록 안전장치를 가진 방법의 커밋 되돌리기 방법이라고 볼 수 있음.)
   
------

[^1]: HEAD - HEAD는 브랜치의 마지막 커밋 즉 현재 속한 브랜치의 가장 최신 커밋을 의미 , <br/>pwd - print working directory / ls - list + (options -a : 숨김파일/디렉터리 함께 표시 / -l : 상세정보 함께 표시 / -r : 파일 정렬 거꾸로 표시 / - t : 작성 시간 순으로 내림차순 표시
[^2]: git init 파일명 : 새로운 디렉터리를 만들고 저장소를 초기화하는 과정까지 한번에 처리.
[^3]:  .git init를 취소하기 위해서는, 디렉터리 내에서 ‘rm -r .git’를 통해서 Git 로컬 저장소 해지가 가능하다. 참고 : (https://wnsgml972.github.io/git/2018/01/22/git_init/) <br/>다만 안에 파일이 있으면, ‘rm -rf .git’로 제거하는 방법도 있겠음.(물론 보통 아예 버려버리는 Git 리포지토리만 삭제할때 써야할듯?)
[^4]: 다만, 단순 --oneline을 통한 커밋 확인에서는 현재 브랜치의 커밋 로그만 확인되는 듯 하다.(연관되지 않은 브랜치는 --branches의 옵션을 별도로 필요로 하는듯)
[^5]:  git add . <- 마침표(.)를 통해서 현재 저장소에서 수정된 파일을 한꺼번에 스테이지로 올릴 수 있음.
[^6]: --amend : 방금 커밋한 메시지 수정하기(VIM 형태로 메시지를 수정할 수 있음.)
[^7]: git checkout의 경우는 오히려 다른 용도(브랜치 이동 등)로 많이 쓰이는 듯 함.
[^8]:git switch branch명 / git restore [파일명] 을 통해서 checkout 기능이 분할되어감.
[^9]:git restore --staged [파일명] 을 통해서 사용하는 추세인듯.
[^10]:git reset HEAD~3 와 같은 방법으로 최근 3개의 커밋을 취소 할 수 있음.

