---
layout: single
title: "Python - Python 문자열1 - 따옴표/문자열연산/인덱싱"
categories: python
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---

## 문자열

문자, 단어등으로 구성. 따옴표로 둘러싸여 있으면 모두 문자열로 치부해도 그만

### **따옴표?**

-> “” or ‘’ or “““ ”””or ‘‘‘ ’’’로 써서 양쪽 둘러싸기

 

- 문자열 안에 따옴표를 포함시키고 싶을때

->

1. 문자열 안에 넣고자하는 따옴표의 반대것으로 둘러싸자(Syntax Error를 발생시키지 않기 위함)

ex1 ) django = “Python’s one is django”

ex2 ) say = ‘“First time with python”he says.’

2. 문자열 안에 넣고자하는 따옴표 바로 앞에 \(백슬래시)를 사용하자

ex ) django = ‘python\’s one is django’

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfALNPQt05vlcDkmwZwUvIo2sPbr83vZApSWXIZiutJ0xvB60Ql8fTDBiM_7k4F94TGl-vpttdzjifxJSc5VsPSE9zbhyQLnu1csH9jHk_w56CLIwPX4ezOFBX2MVohA9KAL4vNU7oYB7L5E2aAXVa_I3nN?key=4uZgYGoLnFSSd3qJBRYl8A)

- 여러줄 문자열

1. 줄 바꾸기 이스케이프 코드 \n
2. 작은 따옴표 3개(‘‘‘ ’’’) or 큰따옴표 3개(“““ ”””)

근데 여기서 따옴표를 = 옆에 붙여서 쓰는 방법과

= 옆에 \를 붙여서 syntax Error를 발현시키지 않게하는 것도 중요하다.

(아무래도 한줄씩 읽어나가는 인터프리터 언어라서 그럴지도 모른다는 생각이 든다.. -> 이는 IDE 에디터 한정 문제일수도 있음, 애초에 여러줄을 한꺼번에 작성이 불가능한 구조니)

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcg-3Ot2O2AkzsvGr4NzbCKkMRCF0xJLmnWJc7QCGwBpBjuRDiR8aWaUliT8RSzVJ0FVndZug7zMgMy0l8HWjfdg_FfYg_BfyQ-w2RpTxD0zA6WpWwbaRMg6Yvf7LOImINtgoihCReLBuKJlptkp-6AAIc?key=4uZgYGoLnFSSd3qJBRYl8A)

### **문자열 연산하기**

\> 더하기(엄밀히 말하면 연결하기)

문자열 변수를 더해버리면 연결이 된다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeW5xLM2CYcoPSVhFdvk3WlLB_OA39qwMH-3uR3z1Kqncxg6dKOadE4kpzsNUWbyLCJSE3gWhBDaMTmm9css8b1sI_Tsa7gseyvsVmh9_oIHs0peOx0HdHPMXCgBBnjiBJ_yfqZEgB47wvMt6ZtRlWzy90z?key=4uZgYGoLnFSSd3qJBRYl8A)

\> 곱하기

문자열 변수를 곱하면 **‘반복’**의 의미를 가진다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXctmSpOMOTXEgjKCePJvT1XGdyavQkOsUKxCIo2OkQ2tatctv2zrlyOz6PEoge0GJoUpzWqiPOxgTAYI2KB-MHyQxTg_76TE-EjnvHeB5hJ_G0RiEV-gHo3nX-jX_UBZU-24gbGxNY5h9fh6SptvPJdoLcY?key=4uZgYGoLnFSSd3qJBRYl8A)

\> 문자열 길이 구하기 : len(변수) 명령어로 구하기.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUPRO15LHRKxQ-Uml-WQZj1Z-8fOWL23Z-hu3Bt3DCxWfCCDPYInrcq11ZE_NYM4FKf_Fy64u0T4kpTp3Ym3U4ccZOb_blzgQpZ3nDmTZ2z5EEbXXz37bul6OtMZa0eIweG2jqz0cOn8DQ3rfmFrfDRy7F?key=4uZgYGoLnFSSd3qJBRYl8A)

### **인덱싱**

‘파이썬은 0부터 숫자를 센다’

\> 변수[몇번째]를 넣어서 문자열의 몇번째 문자를 띄울 수 있다.

ex ) ![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf_VKpM9XqeUIZFREn3Vy3n1yLeiWRkQCXLRA0RmmZa30Uj20jQb1TtwVyMaMZY623pyV3l45_nxCK3BhMFs1PF7TqCoyX8WL85YhQb9DH7REHjToMY4Z6sdyKreN0vhCgxuxcqFQ1Gp2zhyWMTxY6bLQs?key=4uZgYGoLnFSSd3qJBRYl8A)

근데 놀랍게도 공백도 문자로 계산해서 세는듯.

음수를 넣으면 뒤에서 몇번째 문자를 호출하는 그런식이다.

- 슬라이싱 : 인덱싱은 문자를 가리켰다면, 인덱싱 시스템을 합해가지고 단어를 만들어보자

a = 'You need python'인 경우,

1. 인덱싱한것을 더하기

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeoxeXGhCSSohdPM1giRcJ2b3Z9e2cDzvzjqgwRoqRJq6L3hnFpva4T-wFcoveRWG2RArAPLWj0Cx-Y6b8o00Sh6IvqXbsjO4_yDHQVYEDN3e_3oQXBS9bUvNDNC4XTQNhAP4salgCQU5hb1NJix1UXvpY?key=4uZgYGoLnFSSd3qJBRYl8A)

2. 근데 여기서 핵심은 이 방법. 슬라이싱(Slicing)기법이다.

일종의 뭉텅이로 자르는 방법인듯함

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcYLopr13kG4hZ5yZs2MVbPuX01zj-Njx7zK5wmRKRk2whMx8NtS-8l7tpg5FOSLOrMHpS_tXRwRV62pUMqNbvEu4VBPmIGUf4pCGA9cfy9ovdgYcJ_S3agkdBIW4dvIBHaOyDgZCbzpfNR8-8WbLWy9dV5?key=4uZgYGoLnFSSd3qJBRYl8A)

\> 시작 번호가 꼭 0일 필요없음. 

\* 0:3이 가지는 의미는 자리번호 0부터 3까지를 꺼낸다는 의미같지만,

이는 a[0:3] == ‘0 <= a < 3’의미를 가지는데

결정적으로 0,1,2번째자리 문자를 꺼낸다는 의미이다.

이러면 시작번호부터 끝번호 직전자리 문자까지 꺼낸다고 보면 될듯

(-3까지면 -4까지만 꺼낸다고 보면됨)

\> 여러가지 더 응용하면

시작번호를 생략하면 시작번호부터 그 문자열의 끝까지 뽑아내고,

끝번호를 생략하면 처음부터 그 끝 번호까지 뽑아낸다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe1aOd1sCe2yxp9aOXpMz1-r6OfpXPx62elG7loNCnFz1HFYabDxnBw7qfPo6B-kGPbKNXLX8_2CUr7gUIHo0JlpOjqhokgXyjLGpnpjDGQHWnn4BwwDL4TLGGQUyLEAqZvnHrZ3GfRLyG1In_4koP3E7aU?key=4uZgYGoLnFSSd3qJBRYl8A)

게다가 시작번호 양수, 끝 번호 음수 혼종도 산출가능

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcXfO5FMQLJUB5m5IHka0IBUoS_qtufH8FzPskpP8nzkAOAAjPq70M_TMhp4HO9QlTZis_ewlU52-ewAW2RzSndI0j34R6bonyza_tuIAuPM7NAymQIKCt2JeAv1AQUsrEwUiVgombwn2djJONQoP9Nt1ph?key=4uZgYGoLnFSSd3qJBRYl8A)

\> 근데 보통 이렇게 한 문자, 단어만 추출하려고 쓰려기보다

이런 예시를 통해서 슬라이싱이 어떻게 쓰이는지 알 수 있을 듯 싶기도하다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdPbaK_cEtbLqZCjdYf0JUK2EuKL8x_yXStWpgr0x5XgkCRiZw0zFBRQcqOniIHY50ZvSihOStybCqvdWup3LIvQ58BWFj7qpBPPSKlZ87WB1sMQgxtTRLE4THkrU_MiRZQpg_i51M4DhBDJh5Cx-rd3_dn?key=4uZgYGoLnFSSd3qJBRYl8A)

\* 슬라이싱 기법은 문자열의 요소값을 바꿀 수 없는 상황에서도 도움이 될 수 있다. 문자열의 요소값에 오타가 있는 경우, 인덱싱 기능을 통해 인덱싱해온 값만 변경할 수 있을 것 같이 생겼지만 얄짤없이 syntax Error 뱉어낸다.

때문에, 슬라이싱 기법을 사용해서 오타낸 부분만 호출하지 않고 , 오타부분만 다른 문자열로 채워넣는 방법을 쓰는 법이 쓰이는 듯하다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfXdnjjc_37q0ZFiF8GkEbbH9u5fxPeGbR2vAc4LqiJjZ9EdoBG7uJrYD45_tBxyDgGlmnRn19_7Ex-y_nza9w3Qk5SJJYPsZIauNY8jy1yD5zREfogSlpq__-x0rcLulomIOUxwf680gFVUcMJgtd61B36?key=4uZgYGoLnFSSd3qJBRYl8A)