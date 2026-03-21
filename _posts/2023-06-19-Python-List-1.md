---
layout: single
title: "Python - Python 리스트1 - 리스트와 리스트 슬라이싱"
categories: python
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---



## 리스트 자료형

위에서 서술한 단순 숫자형, 문자열로는

어떠한 모음에 대한 집합을 표현하기는 쉽지가 않다. 각각 하나씩 선언하는 수 밖에 없는데..

이를 해소할 자료형인, 리스트 자료형이 있다.

### **리스트는 어떻게 생겼는가?**

“모음을 대괄호로 감싸 주고 각 요소값은 쉼표로 구분한다.”

- 아무것도 포함하지 않는 빈 형태의 리스트[]도 표현가능.
- 각각 숫자, 문자열을 리스트의 요소값으로 가질 수 있는 것은 당연하지만

숫자와 문자열을 함께 요소값으로 가질 수도 있으며,

리스트 자체를 요소값으로 가질 수도 있다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXebFj1FPD7N6JUdKL6YCqQkcXcBL9eifGwHfT0PlLVg7Rc5Ka2mpBHf1LvDXyXKS9V7jQp7K_BanC66qIy7f02PJ0XGz25QMSHQyh1q_4abC9unGh3pNGNbD7YzMdHAbJR_0TPBTeD9nir4-fPgZYLeeU3n?key=4uZgYGoLnFSSd3qJBRYl8A)

리스트 안에는 어떠한 자료형도 포함시킬 수 있다.

### **인덱싱도 가능**

1. 위에서 예시로 든대로 b = [1, 2, 3]일때,

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdQ5X_sKLli38i8lZAeMwnezBRepIAS-N3M97gIlcnfOqFvp3BMn7O84iP7JWAZlPWXmk_Yk3HTYaWzYNkccrb7-sef-qDj2Ei3IriOqoo9Du1spMcWQnozHc_DSISl5nE2Zxahj205tUmDSwn1sEyMulXV?key=4uZgYGoLnFSSd3qJBRYl8A)

1. 파이썬기준 0번째(사람 셈으로 첫번째) - 1
2. 1 + 3 = 4
3. b[-1] = 리스트 b 중 뒤에서 첫번째 요소 = 3

1. 리스트 구성요소가 숫자 + 문자열 일때,

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc6cMnPS3fY-Q4k_vR9UdvJscaT7YvBJehxs6LiL2PPdfs3agxa0GAtwFfqw2gzL7ACGU2qRSUWD9u_p1cUzR0W46sxWB9hlXNlsw5ZdKryZpso6yheLQrICh3JB28K5F38MS06kblaDAMLchOIfHaDXRyI?key=4uZgYGoLnFSSd3qJBRYl8A)

문제없이 숫자, 문자열 요소 하나하나씩 인덱싱 가능하다

1. 리스트내 리스트에서 요소 하나를 끄집어내고 싶을때,

위와 동일하게 a = [1, 2, 3, [‘a’, ‘b’, ‘c’]]

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdWMGPZp33ce7gSnFT9L0C6ndEx0BCVmhh4OGdoXEKQm6RUerR45Y63eDr8RhZKYJrUyAxiiSGowJGcs9FlcTG0zE-CkUkLOuDJS--do4Dc3HtqeQ8CsR2NLjaoKp26h31EkwpNcwBjH74OVvRMbM6oQ2NT?key=4uZgYGoLnFSSd3qJBRYl8A)

연속으로 대괄호를 사용하면 하위 리스트에서 인덱싱이 가능한듯하다

\* 삼중도 삽가능

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcy4iDQcW3MN0Urda7tk5CyjES7LCsUhepN6MeGz3j_-uIqbj1MmVzHxhvrLZBhmMJqUQcFi7WxJsM4VWk3r5tINEYZIMvHXDhFmCrmv11T_54i0EyBxh-xcWyEgYUznoJRO4GqkA-2PSXjQo3edPchPMyp?key=4uZgYGoLnFSSd3qJBRYl8A)

- ### **리스트 슬라이싱**

문자열 슬라이싱과 사용방법 자체는 동일하다, 

다만 자료형 차이로 이제 [문자열과 다르게](https://luvchipmunk.github.io/python/Python-DataType-String-1/) 

리스트 형태로 결과값이 나오느냐 아니냐에 따른 차이다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfwwdPG1WHk1h_EGUMUp6sPcJg9a1NHvdT4-_oWLEH6uJMfS7fUGobitM24kt-gwvlVxo3OArD6S4sWdiyTVwVNzXqZcK13C1BJRWNdw1dyVvMekGgvcxoHOM-DKcaO4s0-LLwfAOOmTw4yk6sDZAG93SIm?key=4uZgYGoLnFSSd3qJBRYl8A)

\* 역시 중첩된 리스트에서 슬라이싱도 가능하다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXejnKvSp9ij304R6sW1hz-aDHT00JgV8foEqc-Id7JGxrM6xV5rubQbxlheJ8Ctpz9fH274zRA6Oxml18thB_O_bnENLeSRSmnQFDfdOxedNFZ00NH0qL-ByDULFxCEYbTgJE0OZ1a0KD_FvcY7fCOTgk_5?key=4uZgYGoLnFSSd3qJBRYl8A)

a[3][:2]의 경우를 설명해보면,

리스트 a의 4번째 요소(숫자상으론 3으로 표시되지만) - [‘a’,’b’,’c’]에서의

2번째 요소까지 표시(:2)를 하여 [‘a’, ‘b’]가 최종적으로 출력이 된 것이다.