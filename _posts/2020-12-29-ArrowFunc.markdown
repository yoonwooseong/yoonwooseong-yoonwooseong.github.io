---
layout: post
title: "Arrow Function?"
date: 2020-12-29 17:40:00 +0300
image: arrow.png
tags: javaScript
---

## 시작하는 말

 코드 중간중간 화살표로 된 것을 본 적 있을 것이다. 그 궁금증을 간단히 해결해보고자 한다.

***

## 화살표 함수 () => (ArrowFunction)이란?  

자바스크립트에서는 함수를 생성하기 위해 function을 사용한다고 한다.


### 함수 선언(Function Declaration)  

```javascript
function fu(){
  console.log("hi!");
}
```


### 함수 표현(Function Expression)  

```javascript
var fu2 = function(){
  console.log("hi!");
};
//여기서 fu2를 화살표 함수로 생성하면
var fu2 = () => console.log("hi!");
```


## 화살표 함수 특징  

* 함수 내용이 한줄인 경우 함수내용을 감싸는 {}를 사용하지 않아도 됩니다.
* {}가 없는 경우 해당 함수의 실행결과를 자동으로 이천 합니다.
* 함수 내용이 한줄 이상인 경우 return을 사용해서 결과를 리턴합니다.
* 파라미터가 한개인 경우 파라메터를 감싸는 ()를 생략할 수 있습니다. (파라메터가 없는 경우에는 위의 fu2의 경우 처럼 파라미터 없이 빈 ()를 표시하여야 합니다.)


화살표 함수 덕에 __this__ 로 인해 헷갈리는 부분이 줄게 된다. 자세한 사항은 this를 console로 학습해 보자.

***

#### 오늘 성장에 도움을 주신 개발자분  

[출처](https://www.a-mean-blog.com/ko/blog/%ED%86%A0%EB%A7%89%EA%B8%80/_/Javascript-%ED%99%94%EC%82%B4%ED%91%9C-%ED%95%A8%EC%88%98-Arrow-Functions) https://www.a-mean-blog.com/ko/blog/%ED%86%A0%EB%A7%89%EA%B8%80/_/Javascript-%ED%99%94%EC%82%B4%ED%91%9C-%ED%95%A8%EC%88%98-Arrow-Functions

감사합니다.
