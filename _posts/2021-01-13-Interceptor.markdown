---
layout: post
title: "Interceptor(인터셉터)란?"
date: 2021-01-13 16:15:00 +0300
image: interceptor.png
tags: Spring
---

## 시작하는 말

회사 Return server에서 interceptor를 처음 보았다. 지금까지 해왔던 프로젝트에서는 interceptor를 사용하지 않았으나 이번에 알게 되어 간단히 요약해 본다.

---

## 인터셉터(Interceptor)란?

Controller에 들어오는 요청과 응답을 가로채는 역할로 DispatcherServlet이 실행된 뒤 호출된다.

Interceptor는 HandlerInterceptor 인터페이스를 반드시 implements 해야한다.

Interceptor는 세션에 로그인 정보 여부와 권한 여부 등을 체크하는 역할을 수행하는데 사용한다.

HandlerInterceptor안에 있는 메서드인 preHandle()은 Controller보다 먼저 실행되는 메서드이며, postHandle()은 Controller가 수행되고 화면에 보여지기 직전 실행되는 메서드이므로 원하는 사이클에 코드를 작성하면 된다.

---

#### 오늘 성장에 도움을 주신 개발자분

[출처](https://developer-jjun.tistory.com/16) https://developer-jjun.tistory.com/16

오늘도 감사합니다.
