---
layout: post
title:  "웹소켓이란?(Web Socket) Socket(2)"
date:   2020-12-21 10:50:00 +0300
image:  websocket.png
tags:   Network
---


## 시작하는 말

필자가 웹소켓을 처음 접하게 된 계기는 회사의 클라우드의 서버에서 단말과 연동하기 위해 사용되었기 때문이다.

그럼 양방향 통신을 지원하는 웹소켓에 대해 적어보려 한다.


***


## 웹 소켓(Web socket)이란?

HTML5 순수 웹 환경에서 연결 지향 양방향 통신을 지원하는 것 - Stateful protocol

AJax, Comet은 모두 Polling 방식이다. - Stateless protocol

* Polling : 클라이언트가 일정 주기마다 요청을 보내고 서버가 응답받는 방식, 불필요한 응답과 트래픽 발생
* Long Polling : 이벤트시에만 응답, 불필요한 트래퍽 x 그러나 이벤트 많으면 과부하
* Streaming : 응답 완료시키지 않고 계속 연결, 길어질수록 유효성 관리 부담

웹 소켓은 웹 서버와 웹 브라우저가 지속적으로 연결된 TCP라인을 통해 실시간으로 데이터를 주고 받을 수 있도록 하는 HTML5의 새로운 사양이다. 따라서 웹 소켓을 이용하면 일반적인 TCP소켓과 같이 연결지향 양방향 전이중 통신이 가능하다.

클라이언트 : 웹 소켓이 제공하는 자바스크립트 API를 이용해 서버에 연결하고 데이터를 송/수신하는 코드를 구현

서버 : 웹 소켓 프로토콜에 맞는 전용 장치 구축

지원되는 브라우저 최신 사파리, 파이어폭스 및 크롬

##### 웹 소켓 클라이언트

브라우저에서 WebSocket의 기본 스펙


서버 연결

~~~javascript
var wSocket = new WebSocket("ws://domain/demo"); //wss 보안 통신
~~~

데이터 송신

~~~javascript
wSocket.send("메세지");
~~~

데이터 수신
서버에서 푸시하는 데이터를 받으려면 message 이벤트를 구현

~~~javascript
wSocket.onmessage = function(e) - e
~~~

을 통해 수신된 데이터 조회 e.data 클라이언트 측 코드는 직관적이다. 
그러나 클라이언트와 통신하는 서버가 존재해야 한다.


##### 웹 소켓 서버
일반적인 TCP 소켓과는 다른 프로토콜로 설계된 웹 소켓. 따라서 웹 소켓 서버 사양에 맞게 구현해야 한다. ws모듈 이용 : 처음에 웹소켓이 연결될 때, wss.on('connection', callback) 함수가 실행 다양한 오픈소스가 제공되고 있다. pywebsocket, phpwebsocket, jWebSocket, web-socket-ruby 와 같은 모듈을 이용하면 쉽게 구축 가능

자바로 구현된 jWebSocket의 jWebSocketClient를 받는다.
([jWebSocket 라이브러리](http://jwebsocket.org/))

아파치 웹서버 or 톰켓으로 구동 / 자바 가상 머신 설치 필요
(다음의 [퀵스타트](http://code.google.com/p/jwebsocket/wiki/QuickStart)를 참고 하자)


***


## socket.io

socket.io란 위에서 설명한 WebSocket과 같이 클라이언트와 서버의 양방향 통신을 가능하게 해주는 모듈.
(다양한 방식의 실시간 웹 기술을 손쉽게 사용할 수 있는 모듈 (웹 클라이언트로의 푸쉬를 지원하는 모듈)) 통신을 시작할때 가장 적절한 방법을 찾아 메세지를 보내준다.

Socket.io는 현재 바로 사용 가능.

개발자가 Socket.io로 개발을 하고 클라이언트로 푸쉬 메세지를 보내면 다양한 방법으로 내부적으로 푸쉬 메세지를 보내준다.

어느 브라우저와 상관 없이 일관적으로 통신할 수 있다.


***


## 일반 TCP Socket과의 차이점Permalink

일반 HTTP Request를 통해 handshaking 과정을 거쳐 최초 접속이 이루어진다.


***

#### 오늘 성장에 도움을 주신 개발자분들 
[출처1](https://m.mkexdev.net/98) 
[출처2](http://www.secmem.org/blog/2019/08/17/websocket-socketio/)

감사합니다.