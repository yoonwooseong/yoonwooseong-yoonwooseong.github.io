---
layout: post
title:  "[JS]async와 await?"
date:   2020-12-22 11:00:00 +0300
image:  05.jpg
tags:   javascript
---


## 시작하는 말

오늘은 async & await에 대해 공부하였다. 자바스크립트는 싱글 스레드 프로그래밍 언어이므로 비동기 처리가 필수적이다.

***

## async & await 이란?

async와 await은 자바스크립트의 비동기 처리 패턴 중 가장 최근에 나온 문법으로 콜백 함수와 Promise의 단점을 보완하고 가독성을 높여준다.

async & await을 이용하면 개발자들이 익숙하게 코드가 위에서 아래로 흐르는대로 사고할 수 있기 때문에 가독성이 높아진다.


#### async & await 기본 문법


~~~javascript
async function funcAsync() { await funcAwait(); }
~~~


#### async & await 에러 처리

async & await에서 예외처리 하는 법은 try catch이다. 이는 네트워크 통신 오류 뿐 아니라 간단한 타입의 오류 등 일반적인 오류도 잡을 수 있고 발견된 에러는 error 객체에 담겨 유형에 맞게 에러 코드를 처리할 수 있다.


***


##### 추후 포스팅 작성

#### 오늘 성장에 도움을 주신 개발자분

[출처1](https://joshua1988.github.io/web-development/javascript/js-async-await/) 

감사합니다.