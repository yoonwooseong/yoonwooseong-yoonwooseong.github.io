---
layout: post
title: "SerialVersionUID란"
date: 2021-02-02 17:16:00 +0300
image: SerialVersionUID.jpg
tags: JAVA
---

## 시작하는 말

가끔 클래스에서 SerialVersionUID를 본 적 있는가? 갑자기 궁금해서 구글링을 해보았다.

---

## SerialVersionUID란?

직렬화(implements Serializable)를 할 때 사용하는 것으로 IDE에서 Serializable을 구현 시 사용하라고 한다.

SerialVersionUID를 지정하지 않아도 컴파일러가 값을 부여하고 클래스 변경 시 SerialVersionUID도 변경될 수 있다. 객체를 저장하고 불러올때 이 SerialVersionUID 값으로 불러오게 된다. 결론은 고유 번호라 해야하는건가..?

JVM에 의한 디폴트 serialVersionUID 계산은 클래스의 세부 사항을 매우 민감하게 반영하기 때문에 컴파일러 구현체에 따라서 달라질 수 있어 deserialization 과정에서 예상하지 못한 InvalidClassException을 유발할 가능성이 있다.

---
