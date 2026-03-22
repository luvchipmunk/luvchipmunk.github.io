---
layout: single
title: "Python - Python 딕셔너리"
categories: python
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
published : false
---

## 딕셔너리 자료형

대응관계로써 나타내는 자료형 -> 파이썬에선 ‘딕셔너리(Dictionary)’

Key , Value의 {}로 둘러싸여있다. 쌍으로서 존재하는것

따라서 , 각각의 요소는 {Key : Value}의 형태로 이루어져 있고 요소는 쉼표(,)로 구분되어있다.

(ex - a = {1: ‘hi’} or a = {‘a’ : ‘hi’} or a = {‘a’: [1,2,3]})

\* 예시와 같이,Value에 리스트도 넣을 수 있다.

\* 다만 Key에는 리스트를 넣을 수 없다.

1. 쌍 추가 - {숫자:문자열}, {문자열:문자열}, {문자열,리스트} 형태 모두 쌍 형태로 추가가능.

양식은 

// 변수명[Key] = ‘Value’ // 이다.

![img](/images/2026-03-22-3-Python-Dictionary/img1.png)

1. 요소 삭제 - 삭제의 경우는 Key값만 입력하면 되는 듯 하다.

양식은 // del 변수명[Key] //

![img](/images/2026-03-22-3-Python-Dictionary/img2.png)

### **딕셔너리 사용법**

1. Key를 통해서 Value 얻기 - ‘변수이름[Key]’

리스트, 튜플, 문자열에서 다루던 인덱싱과 슬라이싱 기법들을 사용할 수 없고,

Value를 얻기위해서는 Key를 이용해야만 한다.

![img](/images/2026-03-22-3-Python-Dictionary/img3.png)

![img](/images/2026-03-22-3-Python-Dictionary/img4.png)

![img](/images/2026-03-22-3-Python-Dictionary/img5.png)

2. Key 리스트 불러오기 - 변수명.keys()

위 dic변수로한 예시에서,![img](/images/2026-03-22-3-Python-Dictionary/img6.png)dict_keys([key명]) **객체** 형태로 결과를 내놓는다.![img](/images/2026-03-22-3-Python-Dictionary/img7.png)

-> 이를 리스트 형태로 변환하려면,

list(변수명.keys()) 형태로 불러내야한다.![img](/images/2026-03-22-3-Python-Dictionary/img8.png)

\* 애초에 리스트 형태로 불러오던때가 있었는데, 리스트 자체가 메모리 낭비성을 띄고 있는듯 하다. 때문에, 현 버전에서는 객체형태로 돌려주는 듯 하다.

**<<주의사항>>

- Key가 중복으로 등록되면, 기존 앞의 쌍이 무시된다.![img](/images/2026-03-22-3-Python-Dictionary/img9.png)
- 위에서 이야기했듯, Key에 리스트는 쓸 수 없다. but, 튜플은 가능하다. 리스트는 값이 변할 수 있기 때문에 Key로 쓸 수 없는 것이다.![img](/images/2026-03-22-3-Python-Dictionary/img10.png)

3. value 리스트 만들기도 가능한데,

변수명.values() << 형태로 가능하다.

![img](/images/2026-03-22-3-Python-Dictionary/img11.png)

4. Key, Value 쌍으로 다 얻기 - 변수명.items()![img](/images/2026-03-22-3-Python-Dictionary/img12.png)

5. Key, value 쌍 모두 지우기 - 변수명.clear()

6. Key로 Value 얻기 - 변수명.get(‘key명’)

[일반적인 value 얻는 방법](https://docs.google.com/document/d/18i9nImWmKBLhy-B9rAgSPDXbJR5NAho4efW5dQgbB-Y/edit#bookmark=id.7zpmjnbrzreh)과 얻는 값은 동일한데,

존재하지 않는 key를 get 형태로 불러오려고 하면, None을 돌려준다는 차이가 존재한다.![img](/images/2026-03-22-3-Python-Dictionary/img13.png)

\* 딕셔너리 안에 찾으려는 Key 값이 없을 경우, 미리 정해둔 디폴트 값을 대신 가져오고 싶을때는 get(요소, ‘디폴트값’) 방식으로 가능하다고 설명이 되어있는데, 책에는 왜 이런 과정이 필요한지 따로 설명이 안되어 있다.

추측해 보건데, 존재하지 않는 key 값을 print 함수가 아닌 객체를 불러오는 방식으로 시도하는 경우

아무런 값도 뱉어내지 않는다. 하지만, 존재하는 Key에 아무 디폴트 Value값이랑 같이 입력해서 불러오는 경우 해당 디폴트 Value 값을 무시하고 실질적인 Value값을 불러낸다.

![img](/images/2026-03-22-3-Python-Dictionary/img14.png)

다만 뭔가 유의해야할점은 Value값에 들어가야할 디폴트 값이 다른 Key값의 Value값과 겹치지 않아야할 것이다.

그래야 디폴트 값을 뱉어낼때, 이게 디폴트 방법을 통해서 없는 key인지 인지할 수 있기 때문이다.

7. Key가 딕셔너리 안에 있는지 조사하기. - ‘Key명’ in 변수명

![img](/images/2026-03-22-3-Python-Dictionary/img15.png)

존재하면 True를 돌려주고, 존재하지 않는다면 False를 돌려준다.