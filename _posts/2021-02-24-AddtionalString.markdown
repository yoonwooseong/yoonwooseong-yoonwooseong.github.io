---
layout: post
title: "StringTokenizer과 startsWith, endsWith"
date: 2021-02-24 08:30:00 +0300
image: addstring.jpg
tags: JAVA
---

## 시작하는 말

회사에서 txt파일을 이용하면서 알게된 BOM을 검색해보았다.

***

## StringTokenizer이란?  

StringTokenizer 클래스는 문자열을 사용자가 지정한 구분자로 쪼개주는 클래스. 그렇게 쪼개어진 문자열을 토큰(Token)이라 한다.


#### StringTokenizer 생성자  

~~~Java
public StringTokenizer(String str, String delim, boolean returnDelims); 
~~~
  
delim의 default값은 공백문자, delim 포함 여부를 returnDelims로 여부확인  

#### StringTokenizer 매서드  

~~~Java
int countTokens() // 남아있는 toekn 개수 반환
boolean hasMoreElements(), boolean hasMoreTokens() // 다음의 token을 반환. 
//StringTokenizer는 어떤 위치 토큰을 사용했는지 기억하고 있고 그 위치를 다음으로 옮김
Object nextElement(), String nextToken() // 다음 토큰을 반환. 이때, 반환형은 순서대로 Object, String이다.
~~~

***

## startsWith와 endsWith  

~~~JAVA 
boolean startsWith(String prefix);
//string 관련 함수로 비교 대상 문자열이 prefix 값으로 시작되는지 여부를 확인하고 boolean (true / false) 값으로 리턴한다.

boolean endsWith(String suffix);
//마찬가지로 suffix로 문자열이 끝나는지 판별한다.
~~~

***

#### 오늘 성장에 도움을 주신 개발자분  

[출처](https://reakwon.tistory.com/90) https://reakwon.tistory.com/90  

오늘도 감사합니다.  
