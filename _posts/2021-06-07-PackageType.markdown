---
layout: post
title: "패키지 유형"
date: 2021-06-07 08:53:00 +0300
image: 02.jpg
tags: Spring
---

## 시작하는 말

패키지 구성은 크게 레이어 계층형과 도메인형이 있다고 합니다.

---

## 계층형  

```
└── src
      ├── main
      │   ├── java
      │   │   └── com
      │   │       └── example
      │   │           └── test
      │   │               ├── testApplication.java
      │   │               ├── config
      │   │               ├── controller
      │   │               ├── dao
      │   │               ├── domain
      │   │               ├── exception
      │   │               └── service
      │   └── resources
      │       └── application.properties
```

위와 같이 Controller는 controller별로 service는 service 별로 구성하는 방법을 말합니다. 계층형 구조는 패키지 구조를 이해하기 쉬우나 프로젝트가 커지면 커질수록 많은 클래스들이 모이게 되는 단점이 있습니다.


## 도메인형  

```
└── src
      ├── main
      │   ├── java
      │   │   └── com
      │   │       └── example
      │   │           └── test
      │   │               ├── testApplication.java
      │   │               ├── mypage
      │   │               │   ├── controller
      │   │               │   ├── domain
      │   │               │   ├── exception
      │   │               │   ├── repository
      │   │               │   └── service
      │   │               ├── display
      │   │               │   ├── controller
      │   │               │   ├── domain
      │   │               │   ├── exception
      │   │               │   ├── repository
      │   │               │   └── service
      │   │               └── order
      │   │                   ├── controller
      │   │                   ├── domain
      │   │                   ├── exception
      │   │                   ├── repository
      │   │                   └── service
      │   └── resources
      │       └── application.properties
```

위와 같은 구조는 도메인형으로 기능별로 나눠 관련된 코드들이 응집된 구조를 말합니다. 도메인형으로 표현했을 경우 더 직관적으로 알 수 있습니다.  

global과 domain으로 나누어 common과 config 같이 프로젝트 전체에서 사용되는 클래스들을 따로 관리하는 구조로 사용할 수 있습니다.  
	
***

#### 성장에 도움을 주신 개발자분  

[출처 : ](https://www.popit.kr/spring-guide-directory-%EA%B0%80%EC%9D%B4%EB%93%9C/) https://www.popit.kr/spring-guide-directory-%EA%B0%80%EC%9D%B4%EB%93%9C/  

오늘도 감사합니다.