---
layout: single
title: "Python - Python 문자열2 - 문자열 포맷팅(String format method)"
categories: python
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---

### **문자열 포맷팅**

\> 앞 포스트와는 조금 다르게. 문자열 안에 어떤 값을 삽입하는 방법이다.

예시를 이행해본걸로 보면,

숫자 대입 / 문자열 대입 / 값(여기선 숫자)를 나타내는 변수로 대입(이 경우 변수포맷코드의 값을 따라가야함)

추가로, 2개 이상의 값을 넣는 법 차례로 작성해봤다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcIhbUEGPfkJVuYWoYGKj0myQFFkC9slFf2yxvtG4rtXWl1Ksqe_u_ORkX7ETN2MX1hfUR0C4j3LlAaK38tpCUA8cK_f2oKK7vIfC2PmV0bYE-VDwtXY-NRnpAYXg4kSJG1iOslyPt67PjCSty2YYzzRSGP?key=4uZgYGoLnFSSd3qJBRYl8A)

| **코드** | **설명**                 |
| -------- | ------------------------ |
| %s       | 문자열(string)           |
| %c       | 문자 1개(character)      |
| %d       | 정수(Integer)            |
| %f       | 부동소수(floating-point) |
| %o       | 8진수                    |
| %x       | 16진수                   |
| %%       | Literal % (문자 % 자체)  |

근데 %s 포맷 코드의 경우는 어떤 형태의 값이든 변환가능.

%d, %f를 넣어야하는 경우에 땜빵으로 써도 된다는 의미인데, %는 자동으로 % 뒤에 있는 값을 문자열로 바꾸기 때문이다.

\* 문자열 안에 %를 표현하고자 하는데 포매팅 연산자 %d를 같이 써야할때

-> 문자열에 %를 표현하고자하는 자리에 %%를 요소값을 작성해준다.

예시 그대로 따라하면 재미없을 것 같아서 Tron 영화에서 봤던

Master control Program의 대사가 기억나서 정수값에 맞춰서 수정했다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeMX9mZiDtr--DI-yuPMdxm0LWjwyNEhM9m5bBvtxVaXNMIgSJwLd9z3Zlo0n-GZdeIJ4jw3EtK3fDODZbrBgHO4N7RJB7QVs-4vyeU7NAeCqwKiWnBvAqYWIW66f3uSwkD5E6WijhsOYXws2aFkmQgalq2?key=4uZgYGoLnFSSd3qJBRYl8A)