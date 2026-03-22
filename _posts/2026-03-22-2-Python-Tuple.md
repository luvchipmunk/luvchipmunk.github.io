---
layout: single
title: "Python - Python 튜플 자료형"
categories: python
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---

## 튜플 자료형

- 리스트는 대괄호 []로 둘러싸지만 튜플은 소괄호 ()로 둘러싼다.
- 리스트는 값의 생성/삭제/수정이 가능하지만 튜플은 그 값을 바꿀 수 없다.

=> 프로그램이 실행되는동안 그 값이 항상 변하지 않기를 바란다거나 값이 바뀔까 걱정하고 싶지 않다면 주저하지 말고 튜플을 사용해야한다.

vs

수시로 그 값을 변화시켜야할 경우라면 리스트를 사용해야한다.

(실제 프로그램에서는 값이 변경되는 형태의 변수가 훨씬 많아, 평균적으로는 튜플보다는 리스트를 더 많이 사용한다.)

![img](/images/Untitled/img1.png)

(요소를 삭제/수정을 시도하려고하면 튜플에서는 지원 안한다고 안내문이 떠버린다)

\* 튜플은 1개만의 요소를 가질때에도 요소 뒤에 콤마(,)를 반드시 붙여야한다.

\* 튜플은 소괄호를 생략해도 무방하다.

### **튜플 다루기**

전체적으로 이 기능은 리스트와 차이가 없는 듯 해보인다

1. 인덱싱하기

![img](/images/Untitled/img2.png)

2. 슬라이싱하기 - 인덱싱 / 슬라이싱 모두 리스트와 다를게 없다

![img](data:image/png;base64,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)

3. 튜플 더하기 - 요소를 생성,삭제,수정이 불가능하지만 다른 튜플과의 연산은 가능해보임

4. 튜플 곱하기

![img](/images/Untitled/img3.png)

5. 튜플 길이 구하기

![img](/images/Untitled/img4.png)

전체적으로 리스트와 추가기능적인 차이는 없어보이는데,

아무래도 항목 값 변화 가능/불가능에 따른 용도차이가 크게 작용하는 듯 싶다.
