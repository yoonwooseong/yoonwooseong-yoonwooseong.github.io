---
layout: post
title: "Logging 하는법?"
date: 2020-12-24 13:37:00 +0300
image: imgPromiseall.png
tags: javaScript
---

## 시작하는 말

지원했던 백엔드 서버 개발 파트와는 달리 회사에서 현재 서비스 앱 파트를 담당하느라 아무래도 javaScript에서 배우는 부분이 많은 것 같다. 그럼 지난번 배운 promise에서 여러 API를 불러올때 유용한 Promise all에 대해 배워보자.

---

## Promise.all이란?

쉽게 예를 들면, 동시에 API에 접속해 데이터를 가져와 resolve로 반환해주는 것으로 생각한다.

Promise.all() 메서드는 순회 가능한 객체에 주어진 모든 프로미스가 이행한 후, 혹은 프로미스가 주어지지 않았을 때 이행하는 Promise를 반환합니다.

### 왜 사용할까?

쉽게 그림을 보며 이해해보자. 사용 전(빨간 부분)

![No use Promise All](./images/Nonpromise.png)

위 그림과 같이 사용 전은 위에 API를 불러온 뒤 다음에 처리한다.

##### 사용 후

![use Promise All](./images/usePromise.png)

위 그림은 사용 후 API를 동시에 불러오는 작업을 진행한다.

## 예제

```javascript
Promise.all([p1, p2, p3]).then((values) => {
  console.log(values);
});
```

---

#### 오늘 성장에 도움을 주신 개발자분

[출처](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise/all) https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise/all

감사합니다.
