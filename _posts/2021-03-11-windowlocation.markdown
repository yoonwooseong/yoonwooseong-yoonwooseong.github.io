---
layout: post
title: "window.location 이란?"
date: 2021-03-11 08:15:00 +0300
image: window.jpg
tags: javascript
---

## window.location에 대해서  

### Properties  

* hash : 주소값에 붙어있는 anchor값 반환 #test  

* host : URL의 도메인과 포트 반환 www.test.com:8080  

* hostname : URL의 도메인 반환 www.test.com  

* href : URL반환 http://www.test.com:8080/search?q=child#test  

* origin 프로토콜 + URL의 도메인 + 포트 반환 http://www.test.com:8080  

* pathname : URL 경로 반환 /search  

* port : 서버포트 반환 8080  

* protocol : 프로토콜 반환 http:  

* search : URL에 붙은 매개변수 반환 ?q=child  


### Methods  

* assign(url) : 새로운 주소로 이동  

* reload(forceget) : 현재 페이지 새로고침  

* replace(url) : 새로운 주소 이동 (세션 히스토리가 남지 않아 뒤로가기 불가)  


***

#### 오늘 성장에 도움을 주신 개발자분  

[출처](https://august5pm.tistory.com/8) https://august5pm.tistory.com/8  

오늘도 감사합니다.  
