---
layout: single
title: "Git이란."
categories: Git
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---

## \* ‘버전 관리는 왜 하는가?’ 

- 파일 변화를 시간에 따라 기록했다가 나중에 특정 시점의 버전을 다시 꺼내올 수 있는 시스템이다. <br/>

각 파일 / 프로젝트를 이전 상태로 되돌릴 수 있고, 시간에 따라 수정 내용을 비교해볼 수 있고, <br/>

누가 문제를 일으켰는지도 추적할 수 있고, 누가 언제 만들어낸 이슈인지도 알 수 있다.

<br/>

\* 그러면 Git은 어떻게 관리하는가? - Git은 데이터를 파일 시스템 스냅샷의 연속(Git’s Data = Stream of snapshots)으로 취급하고 크기가 아주 작다.<br/>

Git은 커밋하거나 프로젝트의 상태를 저장할 때마다 파일이 존재하는 그 순간을 중요하게 여긴다. <br/>
파일의 변화가 없으면, Git은 성능을 위해서 파일을 새로 저장하지 않는다. 단지, 이전 상태의 파일에 대한 **링크**만 저장한다. 

## \* Git 프로젝트의 세 가지 단계

Git 디렉토리(.git directory) - **GIt의 핵심**이다. Git이 프로젝트의 메타데이터와 객체DB를 저장하는 곳을 말한다. <br/>
다른 컴퓨터에 있는 저장소를 Clone할 때 Git 디렉토리가 만들어진다.

워킹 트리(Working tree or Working Directory) - 프로젝트의 특정 버전을 Checkout한 것이다.

-> Git 디렉토리는 지금 작업하는 디스크에 있고 그 디렉토리안에 압축된 데이터베이스에서 파일을 가져와서 워킹 트리를 만든다.

Staging Area (Index) - GIt 디렉토리에 있다. 단순한 파일이고 곧 커밋할 파일에 대한 정보를 저장한다.



∴ Git으로 하는 일은 기본적으로 아래와 같다.

1. 워킹트리에서 파일을 수정한다.

2. Staging Area에 파일을 Stage해서 커밋할 스냅샷을 만든다. 모든 파일을 추가할 수도 있고 선택할 수도 있다.

3. Staging Area에 있는 파일들을 커밋해서 Git 디렉토리에 영구적인 스냅샷으로 저장한다.

   

<br/>
\* Git의 세가지 상태 -

Committed - 로컬 DB에 데이터가 안전하게 저장됐다는 것

Modified - 수정한 파일을 로컬DB에 아직 커밋하지 않은 것

Staged - 수정한 파일을 곧 커밋할 것이라고 표시한 상태를 의미한다.

![Git 3 stages](/images/2023-06-01-What-is-Git/Git 3 stages.png)

Git 디렉토리에 있는 파일들은 **Committed** 상태이다.

파일을 수정하고 Staging Area에 추가했다면 **Staged** 이다.

그리고 Checkout 하고나서 수정했지만, 아직 Staging Area에 추가하지 않았다면 **Modified** 이다.

# ![files lifecycles](/images/2023-06-01-What-is-Git/files lifecycles.png)

워킹 디렉토리의 모든 파일은 크게 Tracked(관리대상임)와 Untracked(관리대상이 아님)로 나눈다. 

Tracked 파일은 이미 스냅샷에 포함돼 있던 파일이다. 
Tracked 파일은 또 Unmodified(수정하지 않음)와 Modified(수정함) 그리고 Staged(커밋으로 저장소에 기록할) 상태 중 하나이다. 

간단히 말하자면 Git이 알고 있는 파일이라는 것이다. 그리고 나머지 파일은 모두 Untracked 파일이다. Untracked 파일은 워킹 디렉토리에 있는 파일 중 스냅샷에도 Staging Area에도 포함되지 않은 파일이다. 

처음 저장소를 Clone 하면 모든 파일은 Tracked이면서 Unmodified 상태이다. 
파일을 Checkout 하고 나서 아무것도 수정하지 않았기 때문에 그렇다. <br/>
마지막 커밋 이후 아직 아무것도 수정하지 않은 상태에서 어떤 파일을 수정하면 Git은 그 파일을 Modified 상태로 인식한다. 

실제로 커밋을 하기 위해서는 이 수정한 파일을 Staged 상태로 만들고, Staged 상태의 파일을 커밋한다. 
이런 라이프사이클을 계속 반복한다.