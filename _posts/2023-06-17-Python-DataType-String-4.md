---
layout: single
title: "Python - Python 문자열4 - 문자열 관련 함수"
categories: python
tag: [githubpages, jekyll]
typora-root-url: ../
toc: true
---

문자열 자료형(문자열 데이터타입)은 자체적으로 함수를 가지고 있는데,

이를 ‘문자열 관련 함수’ 또는 ‘문자열 내장 함수’라고 지칭한다.

문자열 관련 함수(문자열 내장 함수)를 사용하는 방법은 변수 뒤에 ‘.’을 붙이고 자신이 사용하고 싶은 함수이름을 넣어주면 된다.

\* 내장함수는 뒤에서 자세히 서술할 예정이다.

​                                              ***문자열.함수명()***

- 문자 개수 세기(count)

단어 “cherry”를 예시로 들어서 ‘r’을 세기

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfEU0qSlyqtO-vj75rXAekH2er3I38kQewwokMKq7dS8DfdRqJocne0CKkn_O4eN-zB7oWVdNkwMNmOM9yKCiCFMMhIQ-rjsnDhPJ6whSYOpJxQ6adwn9ZT_9yD9XTo2I02b7NXw70VJC9CzwxFxSD0s8E?key=4uZgYGoLnFSSd3qJBRYl8A)

- 위치 알려주기(find / index)

find나 index나 문자열 중 해당 문자가 처음으로 나온 위치를 반환해야한다.

하지만 find는 찾는 문자나 문자열이 존재하지 않는다면 ‘-1’을 반환하지만,

index의 경우는 문자나 문자열이 존재하지 않는다면 syntax Error를 뱉어낸다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfxMbReTuQHB25EPp05W6tPdL3phgnlH0jd5ffqYb3l4d5sRzb16tItndBroWF6uUiUpxBVWe8vz4WnDJjip21RgJ4x-DTn9nIGANKvr-CK3-eyKjQRP5UjlkdzPKb9HFKdvyXWPE99-Vv9ZntdyFEbyTM_?key=4uZgYGoLnFSSd3qJBRYl8A)

- 문자열 삽입(join) - 리스트/튜플에서도 사용가능

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXegXOsO85T1o1MJGEkroPE9lXkWZLMu-rL9Chvt_6Hv0gdT0iB1TRv67x9rwZHOQANstu3X95g_U1F4p28EeDhFGEz7YpGPw8pramBnqeQyKM0LmBcP9z7nN4OLPFs31aZCwpw1fhuTnt5V4lvK_IX-6kKH?key=4uZgYGoLnFSSd3qJBRYl8A)

해당 문자열 각각의 문자 사이에 ‘값’을 삽입하는 것이다.

예시로는 반점만 있어서 문자도 가능한가 싶어,

mrt을 통해 골키퍼 이름 meret을 만들 수 있는지 가능한가 시도해봤다

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJ95jZXduVhgXWHZ2qNjS-Brz6R6AeRgkt7hi1rKCp6ok6kdx-BeTDIL8Us_trfb93lQV1PFRV3rFZdFfqho5mxVBrfhcZe377oGKZNxDaKcsvY3PDjJ1mO7w29ldSENyFi2kvG27nfISvndRvpaLv-U3D?key=4uZgYGoLnFSSd3qJBRYl8A)

너무 당연히 잘된다

- 소문자 -> 대문자로 바꾸기 - upper()
- 대문자 -> 소문자로 바꾸기 - lower()![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcbGazO8tqNTFtn2Vi4BoOlIoeO6y1k7bgTOxIgwFTu1wHnQa1zu-6rQ0L4i-pkvbSEX3p6aTO2W_NCKffpoLI6L3yA6B83U34o6EMVSR3GfLLzo7ruvIHR-FyOmKzVDEkNyNehnG5vvj3taDMpEKIwFtg?key=4uZgYGoLnFSSd3qJBRYl8A)
- 공백 지우기 - (왼쪽 공백 - lstrip() / 오른쪽 공백 - rstrip() / 양쪽 공백 - strip())

문자열 중 가장 끝쪽에 있는 딱 한칸만 지우는 것이 아닌, 한 칸 이상의 연속된 공백을 지우는 것. 

왼쪽이면 문자열 중 가장 왼쪽에 이는 한 칸 이상의 연속된 공백을 지우는 이런식. 양쪽이면 양 쪽에 있는 연속된 공백이 해당이 되는 것이고.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf_5bOl_JwtjIbiGr_kx-OuuAApUhWQR0zfkC8yWdk0uaDGkgoSg-UBf__nAL8uDbNrQPI-cDhI9057Z6QdG4EzO9UuI0ddhf4wlUYNCxIuyNYYSUn2xPwqVTtReSlK8LhAHQmo9_UX1TnBRSz3YBNZ7g1F?key=4uZgYGoLnFSSd3qJBRYl8A)

- 문자열 바꾸기 - replace()

replace(바뀌게 될 문자열, 바꿀 문자열)처럼 사용해서 문자열 안의 특정한 값을 다른 값으로 치환해준다.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfuWeXfVwBEJbU0WKrzypm7_HAA9g6pq4NskUet28pMI9QBFh66APhbpFUqhD5bhTIoRphcNKZHI3hPZH9WIg5LgiCYfnL9AnZ2hL9ZtdUKq8TyRMFs7Xn_rdDBzbsbxB4aGlHYKdc525iW01iw_T0GZL9s?key=4uZgYGoLnFSSd3qJBRYl8A)

- 문자열 나누기 - split() <- 들어가는 값 기준으로 문자열 나눔.

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfHTtBaxsvHyy4F-S9Z2yn1rAArQc7pSPJUM_VOIS9pF3VP47APz7Vj74mSph8NR_fXIdb98jOa2yXlPVe6Eci0D6529GHAd4eu_NxCvWu3NYsoFDipQ5qlprOUCtAHa0Ky_LBQEqn_n8Fth4-Lm_95ZNUq?key=4uZgYGoLnFSSd3qJBRYl8A)

a처럼 공백으로 두면 공백을 기준으로 문자열을 나누고 , b경우는 :을 기준으로 나눈 예시