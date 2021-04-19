---
layout: post
title:  "Eclipse JAVA와의 호환성 문제 해결하기"
date:   2020-12-18 16:38:00 +0300
image:  01.jpg
tags:   Setting
---

## 시작하기 전에

간혹 프로젝트를 Import하면 호환성 문제로 인해 많은 이슈가 발생한다.

이를 해결하기 위한 몇가지 방법을 소개합니다.

***

## How?

#### 첫번째 방법

1. 프로젝트 우클릭 Build Path(Configure Build Path) - Java Build Path(Libraries 탭) - Tomcat 버전 확인 - JRE System library 버전 확인 (추가시 installed JREs)

2. 이클립스 Preferences - Server - runtime Environment - 톰캣 Edit - JRE 버전 확인

3. 다시 Build Path(Configure Build Path) - Project Facets - Java 버전 및 Dynamic Web Module 확인

4. 셋 다 동일한 Java version으로 맞춰주기



#### 두번째 방법

1. 이클립스 - Window - Show View - Other - Markers

2. 콘솔창 옆 Markers에서 에러나는 부분 Quick 솔루션 클릭

