---
layout: single
title: "Python - Python 문자열3 - 포맷 코드와 숫자 함께 사용"
categories: python
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---

### **포맷 코드와 숫자 함께 사용**

\> 포맷 코드 자체가 문자열 안에 어떤 값을 삽입하기 위해 사용이 되는데, 포맷 코드를 숫자와 함께 사용하면 더 유용하게 사용가능하다

- 정렬과 공백

포맷코드 앞 숫자의 절대값이 문자열 공간을 의미하게되고, 그에 대입되는 값에 대해

1. 포맷코드 앞에 양수숫자를 넣는 경우, 오른쪽 정렬 후 나머지는 공백처리
2. 포맷코드 앞에 음수숫자를 넣는 경우, 왼쪽 정렬 후 나머지는 공백처리

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcLb90jbjZNbfJxXE8fCSFG0h_z8Gff6QIoVFeDWeiPUwRMoCE470MYljU6KaGWOhFUoSr5_H8vM6qRvAn_PqC1Kpi0-qGZ9PFGv3VVQRN2kPrq11DBbluGzXPBW8YmA3B51FVasox3XdR4mt9gF21nc2Y?key=4uZgYGoLnFSSd3qJBRYl8A)

- 소수점 표현하기

소수점 몇 번째 자리까지만 나타내고 싶은지에 따라, 소수점 포인트 이후에 표시를 원하는 자릿수를 입력해준다.

역시 포맷코드 앞에 붙는 숫자는 최소한의 문자열 전체길이를 의미하는 듯 싶다.

예시를 제외하고 포맷코드 앞에 붙는 숫자를 공백으로 두거나, 숫자를 조금 바꾸어 보았는데 참고하면 좋을 듯 싶다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeq0JR36ro-24OmypjM5q43qqnvKL-lfzkpy_exh-6G2QrimAd18ON6MT4sNzUaU-iCHeGb1RaY7IwrYzKmY-nM6eCsQl0LrcL_Sh41eI3GMh5EVc8jmsIwmq8cfJyQGYt9dLxZfo1ssIO7JGHuWJVtD1Y?key=4uZgYGoLnFSSd3qJBRYl8A)

- (문자열) format 함수를 사용한 포매팅

1. 숫자 대입
2. 문자열 대입
3. 숫자 값을 가진 변수로 대입
4. 2개 이상의 값 넣기

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeE2iAEPTC9Hh9eCQ0seY8cUDA1oSzfsmfaPzeflLY5fUg-1AY3Ikw_1hfWsZ9zd-7xFuPEqs0tq4mD-og5UIg9O38uBMNc4Ju9VHud1JetpGGfBbdPmOoxmEdahUG9NmNi1GpmE5xo4rjq7H1ZHHxXRVvq?key=4uZgYGoLnFSSd3qJBRYl8A)

5. 이름으로 넣기

인덱스 대신에 {name=value} 형태의 format 함수 통째로 대입하는 듯

6. 인덱스와 이름을 혼용해서 넣기

결과는 똑같다. 다만 하나는 인덱스 형태로 숫자 바로 대입 & 다른 하나는 {name=value}형태로 name함수에 문자열 함수 대입

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdb9vYmJWRyaAQOE4hO0fPzJCHX9ifblybi2EMz7eXwh50KJ5hR1NueWoOaWQ6y9zNBsmjPEwqS9noQlhk_C2GhhZVbAQlN8CQM-ubRfL7_VwZ-KEx_3wRzQThAK3QkmEpVwOfM_TBQrWYjgE-pB6yipls?key=4uZgYGoLnFSSd3qJBRYl8A)

7. 왼쪽 정렬 - :<

8. 오른쪽 정렬 - :>

9. 가운데 정렬 - :^

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcPXUQcw8rYmMak56V9tl4ja3q5WVFk_HXc-VnOS11Y36D3dSJImWDAZwThNbg0eJTE6gRBTEqsYZCi2azTts5_ZYqIQamYy-5B16SimRrDzv6YFA7QSwnT0F2Vq-A_ZCsawgZqg9C89TiTyRqNDwbQ0Nrx?key=4uZgYGoLnFSSd3qJBRYl8A)

10. 공백 채우기

채워 넣을 문자 값은 정렬 문자 <.>,^ 바로 앞에 넣어야한다.

(ex - 가운데정렬에 ^ / 왼쪽 & 오른쪽 정렬 ! 채워넣기 = 아래예시참조)

 ![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXes_Qj5__M06A_uMDaPw6xQkDU6i4REb9q16MccWRdpx_lbDyrUlZQ80Rqa4Tsy-a25q3u_8LlEfctcA6TPNbgK3BO9DC1JU6JcbRm11EqllELJqfklL_lql82vaGZRa97azLU2FYsRbA0UP8yVatyIgPkX?key=4uZgYGoLnFSSd3qJBRYl8A)

11. 소수점 표현하기

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcdMGkBUU1hrdsiC1uwoKQXVOSeXzubbFP3yxbc6tHqMadD23Ep7K61VzCLC5n2ve3HQKcmYG2WMTrwPLwfzOEgtWiJZxU5JIOneCxgFxCOD__wWPPH2j-SnJB4s9xtkLlMiCkw7uDtllGTj_Gkw2ChS9Ad?key=4uZgYGoLnFSSd3qJBRYl8A)

\> 모두 소수점 4자리까지만 표현하는 것은 동일한데,

아래의 경우 [여기서](https://docs.google.com/document/d/18i9nImWmKBLhy-B9rAgSPDXbJR5NAho4efW5dQgbB-Y/edit#bookmark=id.oop0ud1bnyw5) 이야기한대로 자릿수 10자리 맞추기

12. ‘{‘ 또는 ‘}’ 문자 표현하기

{}를 포매팅 전용이 아닌 문자 그대로 쓰고 싶을때는,

{{ }} 로 2개를 연속해서 사용하면 된다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfsCq_juxbSDH7R0asYBW2SNpxsGzpbUlWVbTsSZ99bs0jnaxXbrbJF1RSwZ1sIWnyD1FghwTlnMvQslhtoy8wbUM6Pmw_J-6CO6Gz_VK-T3x7aHbJpgPlsKDB8JOuYisOIHid-Hz1HUmqcCgv8wi4JWTdL?key=4uZgYGoLnFSSd3qJBRYl8A)

- f 문자열 포매팅 (Python 3.6이상부터만 가능)

문자열 앞에 f 접두사를 붙이는게 포인트.

다만, 문자열을 선언하기전에 변수 값을 생성해서 참조할 수 있음.

(format 함수를 사용한 포매팅과는 다르게, 문자열 뒤에서 format함수를 통해서 뒤에서 대입시키는 것이 아니다.)

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeuZfUKq1l5kvU3W_G8Zu_AZR7Nq2r7hAc5cTqtp8Hjb_W75-dxwyW3U9Ge4z_pkKL3yfTjKycbOCjSZB2fmj0oQVkcH9ObwEj4lNRGfoe6QGQ_L61fxJu0YQ12VtZ6frtpK9gUu59nKwYlax_CtLEneD1q?key=4uZgYGoLnFSSd3qJBRYl8A)

\* 문자열 포매팅은 표현식(문자열 안에서 변수에 +,-와 같은 수식을 함께 사용하는것)을 지원한다. 때문에 이런 것도 가능

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXemuSH5Brdgx5_riG61XC8itMlhcx3prnKSZLQW7nvnPW9Cxa7UY0r7vzpl1fAtLogh7intmyOt3R5YxOKVF1rNqsC_wM1G25iNFvjQeuC0PQUhPYZL7TAKBCLqm1I3pTiq2e18CfIrQ4aOSOUoRaoMDAvx?key=4uZgYGoLnFSSd3qJBRYl8A)

\* 딕셔너리(Key와 Value라는 것을 한 상으로 갖는 자료형)는 f 문자열 포매팅에서 다음과 같이 사용가능

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcPkX1ZHZtdCujRnVwHOVqxQQZ4E_vAHCQSZ6nz63k3kM6utBqiOnX3bM5pW4inPsI1p1nuaP09DTwhPDwHaYvD4nwE_cOa0C5SJNEUHjiIhYwmPe0X3-7WH4qERx592eHG76m5S87WYFBh1Qx4K-dEro4o?key=4uZgYGoLnFSSd3qJBRYl8A)

1. 정렬하기

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfYL7cFWPxB2UHt1AZY7YhISEw8ddFPKIJDwRSx0KhXYje6NWCd-JqnOMCbgO5tbTmgU5KISzcqlAV28nSND_bKdUhLUOcbnRPMQ1sdsF5Uu0QOZxPjIxO5HF7OCHvanTwjZAEvQzElJkGH7ORlAYniFFWX?key=4uZgYGoLnFSSd3qJBRYl8A)

[아까](https://docs.google.com/document/d/18i9nImWmKBLhy-B9rAgSPDXbJR5NAho4efW5dQgbB-Y/edit#bookmark=id.fyxwbrtw6jyx)랑 <(왼쪽정렬),>(오른쪽정렬),^(가운데정렬)을 하는 것은 동일하지만

뒤에서 format 함수형태로 포맷하는 것과 달리 문자 값을 문자열안에 표현하는 	것이 큰 차이점으로 보인다.

2. 공백 채우기

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdILZ4BlCYHtenpLOq0HdHVLvkgpkdYOw6Oe3h0VIzLytFn1qTCd71ImK5rKTPVb1nPHAVRniOJ-t5e8R8V1GDcxwkeTmBzkYr9GtGlIK1UlqaSSv6RDuaoZRd9jKvrZPF5B_aslVb1NIGpHNv12JCPLEte?key=4uZgYGoLnFSSd3qJBRYl8A)

3. 소수점 표현 - 책에서는 변수 생성/참조만 이야기했지만, 변수 생성없이 문자열 안에서 바로 소수표현하고 작성해도 문제없는 것으로 보인다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcQMIorzfD6UWMHrSXH_w7UuclB59hpitN-bckNNqVpeMOba5IvsHN-A89-WGzqUB-VutrR6_LxvthdG5DcAo2Eo4fz5f0cBvSMbnixAjG9fCxlUS93T1Wz3zkKk3l2UUPNOz9Ze7JffNrE3lhraN8iPfE?key=4uZgYGoLnFSSd3qJBRYl8A)

4. 역시 {}를 문자열안에서 문자로 표시하려면 두개 동시사용은 동일하다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfyO5kwiQa7Sp43x1NHlVXCPDiZQLjDLdPmhy_Qd3KKpmoLJpe5NkZeIaeVs4BzVqRzGa7oCRzgKULQEc3QmIeeYJPAXr-3Xp4XHfWP3_Dat-wAGRyHa6Dy9zeVVHcX60NiUy9s7YBnl0f5Th-TFiXplRJs?key=4uZgYGoLnFSSd3qJBRYl8A)