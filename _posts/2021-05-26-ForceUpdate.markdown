---
layout: post
title: "Vue $forceUpdate, $NextTick"
date: 2021-05-26 08:20:00 +0300
image: vue.png
tags: Vue
---
 
## 시작하는 말  

회사의 기획전 개발을 진행하면서 Vue에 대한 매서드들의 개념을 다뤄보려고 한다.

***

## vm.$forceUpdate  

이 메서드는 인스턴스를 강제로 다시 렌더링시킨다. 다른 컴포넌트나 인스터스에 영향을 끼치지 않고 해당 메서드가 실행된 인스턴스만 다시 렌더링된다.  

### 언제 사용할까?  

Vue의 상태는 변경되었으나 화면에 변경된 상태가 반영되지 않는 경우 이 메서드를 사용하며 다시 렌더링하며 반영시킬 수 있다.

### 하지만..  

렌더링은 작업 자체가 비용이 많이 들기 때문에 과도하게 사용할 시 애프리케이션의 성능이 하락할 수 있다.

***

## vm.$nextTick  

해당 메서드는 다음 렌더링 사이클 이후 실행될 콜백 함수를 등록할 수 있느 기능을 제공한다. 이말은 즉 $nextTick의 콜백 함수에 DOM을 조작하면 데이터를 그리기 전에 DOM이 생성되며 해당 태그(?)를 찾지 못하는 오류를 막을 수 있다.  

~~~javascript
created : function() {

    this.$nextTick(function(){
        var item = document.getElementById('textBox');
        item.style.backgroundColor = 'green';
    });
}
~~~

$nextTick은 await/async와도 함께 사용 가능하다고 한다.  

~~~javascript
methods : {
    async doSomething(){
        await this.$nextTick();

    }
}
~~~

***

#### 성장에 도움을 주신 많은 개발자분 감사합니다!

[출처 1 : ](https://y-chyachya.tistory.com/11) https://y-chyachya.tistory.com/11  

[출처 2 : ](https://doozi316.github.io/vuejs/2020/08/10/Vue4/) https://doozi316.github.io/vuejs/2020/08/10/Vue4/  

오늘도 감사합니다.  
