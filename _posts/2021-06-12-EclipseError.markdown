---
layout: post
title: "[Eclipse] renaming project error 발생 시 해결방법"
date: 2021-06-12 23:10:00 +0300
image: 06.jpg
tags: Eclipse
---

## 시작하는 말

Gradle project는 이클립스에서 gradle import했을때 다음과 같은 오류가 발생할 수 있다.

```
Description Resource Path Location Type Project at 'D:\Project\stocking-backend' can't be named 'back' because it's located directly under the workspace root. If such a project is renamed, Eclipse would move the container directory. To resolve this problem, move the project out of the workspace root or configure it to have the name 'stocking-backend'. stocking-backend line 0 Gradle Error Marker
```

---

## 해결 방법

다음과 같은 에러가 발생할때는 아래의 순서대로 해결하면 된다.  
![eclipseerror](/images/ee1.PNG)

1. 프로젝트의 settings.gradle을 2번과 같이 수정한다.  
   ![eclipseerror](/images/ee2.PNG)

2. rootProject.name을 맞게 설정해준다.  
   ![eclipseerror](/images/ee3.PNG)

3. 그리고 난 뒤 Refresh Gradle Project를 해준다.  
   ![eclipseerror](/images/ee4.PNG)

끝. 간단한 에러 수정방법이다.

---

#### 성장에 도움을 주신 개발자분

[출처 : ](https://haenny.tistory.com/99) https://haenny.tistory.com/99

오늘도 감사합니다.
