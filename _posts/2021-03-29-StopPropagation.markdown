---
layout: post
title: "[javascript] event.stopPropagation이란?"
date: 2021-03-29 14:40:00 +0300
image: stopPropagation.png
tags: javascript
---

## event.stopPropagation란?  

먼저 propagation이란 파동, 전파란 의미로 예측해보면 stopPropagation은 더이상의 전파를 막는다고 생각할 수 있다. 실제로 예측한 바와 같이 동작하는데 다음 코드를 보며 이해해보자.  

~~~html
<ul onclick="ClickUl()">
    <li>
        <div onclick="ClickDiv()"></div>
    </li>
</ul>
~~~

위의 코드에서 div를 클릭하게 되면 ClickDiv가 실행되는데 __event.stopPropagation()__ 를 사용하면 li 태그를 거친 후 ul 태그까지 이벤트가 전달되는 것을 막아 ul의 ClickUl 실행을 막아주는 역할을 수행한다.  

***

#### 오늘 성장에 도움을 주신 개발자분  

[출처](https://ismydream.tistory.com/98) https://ismydream.tistory.com/98   
[이미지 출처](https://joshua1988.github.io/web-development/javascript/event-propagation-delegation/) https://joshua1988.github.io/web-development/javascript/event-propagation-delegation/
오늘도 감사합니다.  
