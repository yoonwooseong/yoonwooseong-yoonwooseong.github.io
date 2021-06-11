---
layout: post
title: "[Eclipse] Gradle Import"
date: 2021-06-11 09:45:00 +0300
image: 05.jpg
tags: Gradle
---

## 시작하는 말

Gradle project는 이클립스에서 gradle import로 하지 않으면 spring부터 시작해 많은 에러가 발생할 것이다. 헤맸던 부분을 정리해보자.

***

##

1. 먼저 이클립스에서 File -> Import로 가자.  
![eclipseGradle](/images/eg1.png)  

2. 다음 화면에서 Gradle -> Existing Gradle Project 선택 후 Next 버튼 선택. 
![eclipseGradle](/images/eg2.png)  

3. 다음 팝업 창에서 Next를 눌러주자.  
![eclipseGradle](/images/eg3.png)  

4. Prohect root directory에서 로컬 경로를 찾은 뒤 Finish를 선택.  
![eclipseGradle](/images/eg4.png)  

5. 시간이 좀 소요가 되며 이클립스 오른쪽 하단에 보이는 진행사항이 끝나면 이클립스에 Gradle 프로젝트가 잘 Import 되었을 것이다.

***

#### 성장에 도움을 주신 개발자분  

[출처 : ](https://java.ihoney.pe.kr/301) https://java.ihoney.pe.kr/301

오늘도 감사합니다.