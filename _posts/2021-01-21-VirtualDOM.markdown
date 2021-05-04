---
layout: post
title: "Virtual DOM이란?"
date: 2021-01-21 12:10:00 +0300
image: virtualDOM.png
tags: javascript
---

## 시작하는 말

DOM과 가상DOM을 한번 쯤 들어보았을 것이다. 그 궁금증을 해소하기 위해 간단히 알아보도록 하자.

***

## Virtual DOM이란?  

Virtual DOM은 실제 DOM 변화를 최소화 시켜주는 역할을 합니다.

DOM이란, 브라우저는 HTML 파일을 스크린에 보여주기 위해 DOM 노드 트리 생성, 랜더트리 생성, 레이아웃, 페인팅 과정을 거친다. DOM 노드는 HTML의 각 엘리먼트와 연관되어 있어 HTML 파일에 20개 변화가 생기면 DOM 노드가 변경되고 20회 다시 이루어 진다. 작은 변화에도 매우 많은 과정들이 다시 실행되어 DOM 변화가 잦으면 성능이 저하된다.


Virtual DOM은 View에 변화가 있으면, 그 변화가 실제 DOM에 적용되기 전 Virtual DOM에 적용시키고 최종 결과만 실제 DOM에 전달한다. 따라서 변화된 부분만 모아 실제 DOM에 그 변화를 1회로 인식하게 하여 단 한번의 렌더링 과정만 거치게 됩니다.


Virtual DOM을 사용하는 프레임워크로 Vue와 React가 있다.  

***

#### 오늘 성장에 도움을 주신 개발자분

[출처](https://library.gabia.com/contents/infrahosting/8284/) https://library.gabia.com/contents/infrahosting/8284/

오늘도 감사합니다.
