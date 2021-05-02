---
layout: post
title: "DispatcherServlet이란?"
date: 2021-01-14 17:02:00 +0300
image: dispatcherServlet.png
tags: Spring
---

## 시작하는 말

Interceptor를 공부하면서 DispatcherServlet을 간단하게 다시 복습해보자.

---

## Dispatcher-Servlet 이란?

Servlet Container에서 HTTP프로토콜을 통해 들어오는 모든 요청을 프레젠테이션 계층의 제일 앞에서 둬 중앙집중식으로 처리해주는 프론트 컨트롤러

이 말이 무엇이냐? 간단히 클라이언트가 URL을 호출을 하면 Controller 오기 전에 무조건 먼저 거치 듯 클라이언트와 서버 사이에 있는 녀석

이 녀석은 해당 어플리케이션으로 들어오는 모든 요청을 핸들링해주며 일일이 url을 등록해줘야 했던 방식을 쉽게 만들어 주었다.

단 점이 있다면 모든 요청을 처리하다 보니 전부 Controller로 넘겨버리는데 `<mvc:resources/>` 를 사용하여

---

#### 오늘 성장에 도움을 주신 개발자분

[출처](https://mangkyu.tistory.com/18) https://mangkyu.tistory.com/18

오늘도 감사합니다.
