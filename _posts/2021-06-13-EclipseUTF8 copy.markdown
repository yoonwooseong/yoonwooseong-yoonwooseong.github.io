---
layout: post
title: "[Eclipse] 한글 깨짐 해결방법"
date: 2021-06-13 16:00:00 +0300
image: 07.jpg
tags: Eclipse
---

## 시작하는 말

이클립스에서 한글이 깨지는 경우 해당 포스트를 읽어보자.

---

## UTF-8 인코딩 설정

이클립스를 사용할때 한글 깨짐 현상이 종종 나타난다. 그것은 환경을 UTF-8로 설정해줘야 한다. 인코딩 방식이 UTF-8로 설정하는 방법을 알아보자.

1. Window -> Preferences에 들어간다.  
   ![UTF-8](/images/UTF8e1.PNG)

2. General -> Content Types -> Java Class File 클릭 후 아래의 Default encoding 칸 : UTF-8 을 타이밍 후 적용시킨다.  
   ![UTF-8](/images/UTF8e2.PNG)

3. General -> Workspace에서 Text file encoding을 UTF-8로 바꿔준다. (필자는 여기서 해결되었다.)  
   ![UTF-8](/images/UTF8e3.PNG)

4. General -> Editors -> Text Editors -> Spelling 에서 Encoding을 UTF-8로 변경  
   ![UTF-8](/images/UTF8e4.PNG)

5. Web -> CSS Files에서 Encoding을 ISO 10646/Unicode(UTF-8)로 바꿔준다.  
    여기서 HTML Files와 JSP Files도 같이 변경해준다.
   ![UTF-8](/images/UTF8e5.PNG)

6. XML -> XML Files에서 Encoding을 ISO 10646/Unicode(UTF-8)로 변경해주면 된다.
   ![UTF-8](/images/UTF8e6.PNG)

끝. 간단한 인코딩 변경 방법이다. 가장 중요한건 Apply를 해줘야 한다. 꼭!

---

#### 성장에 도움을 주신 개발자분

[출처 : ](https://suzxc2468.tistory.com/174) https://suzxc2468.tistory.com/174

오늘도 감사합니다.
