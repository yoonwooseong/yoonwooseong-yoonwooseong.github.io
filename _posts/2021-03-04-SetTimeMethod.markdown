---
layout: post
title: "setTimeout, setInterval, clearInterval"
date: 2021-03-04 08:20:00 +0300
image: settimeout.png
tags: javascript
---

## 시작하는 말  

오늘은 자바스크립트에서 시간 지연이 필요할때 사용하는 함수들을 알아보자

***

## setTimeout 메서드  

setTimeout은 일정 시간 후 함수를 실행하는 메서드  

~~~javascript
setTimeout(function, delay);
setTimeout(function(){기능}, 1000) //1초 후 function실행
~~~


## setInterval 메서드  

setInterval은 일정 시간마다 함수를 실행하는 메서드  

~~~javascript
setInterval(function, delay);
setInterval(function(){기능}, 1000) //1초마다 function실행
~~~


## clearInterval 메서드  

clearInterval은 setInterval로 반복하던 함수를 멈추는 메서드  

~~~javascript
clearInterval(var);
~~~

***

#### 오늘 성장에 도움을 주신 개발자분  

[출처](https://squll1.tistory.com/entry/javascript-setTimeout-setInterval-clearInterval) https://squll1.tistory.com/entry/javascript-setTimeout-setInterval-clearInterval  

오늘도 감사합니다.  
