---
layout: post
title: "java.util.properties"
date: 2021-02-26 08:05:00 +0300
image: 03.jpg
tags: JAVA
---

## 시작하는 말

회사에서 사용하는 properties에 대해 알아보았다.

***

## properties class란?  

Map 계열의 컬렉션 프레임워크와 같이 동작하는 파일로 "Key=Value" 형태인 "파일이름.properties" 또는 ".xml"파일  

key를 주면 value로 반환한다.  

DB의 연결정보 등 저장해두는 용도로 사용한다.  


### 사용 목적  

열거형 클래스나 컬렉션 API와 비슷한 파일로 코드를 수정하지 않고 이 파일의 값만 바꿔 정보를 변경하는 목적으로 사용


### 매서드  

~~~Java
vode load(FileInputStream file) // 스트림으로 열린 properties의 객체를 로드
vode load(FileReader file ) // 스트림으로 열린 properties의 객체를 로드
string getProperty(String key) // key값을 제공하면 해당하는 Vaule를 문자열로 반환
Object setProperty(String key, value) // Properties 객체에 key와 vaule를 저장
void store(스트림객체, 주석) // 객체에 저장된 내용을 파일에 씀 (OutputStream, Writer 계열만 가능)
~~~

***

#### 오늘 성장에 도움을 주신 개발자분  

[출처](https://codevang.tistory.com/163) https://codevang.tistory.com/163  

오늘도 감사합니다.  
