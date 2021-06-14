---
layout: post
title: "Java로 Queue를 사용해보자."
date: 2021-03-26 08:23:00 +0300
image: queue.png
tags: Java
---

## Queue란?  

Queue는 줄을 지어 순서대로 처리되는 자료구조로 First In First Out의 형태를 가진다. 말 그대로 먼저 들어온 뎅터가 먼저 나가는 구조를 말한다. 사용 예제로는 그래프의 넓이 우선탐색인 BFS와 컴퓨터 버퍼(큐)에서 사용되며 맨 앞쪽의 데이터 삭제를 Dequeue, 맨 마지막의 데이터 추가를 Enqueue라 한다.  

***

### Queue 사용법 - 생성  

Queue를 JAVA에서 사용하기 위해서는 Queue와 LinkedList 모두 Import가 필요하다.  

~~~java
    import java.util.LinkedList;
    import java.util.Queue;

    Queue<Integer> queue = new LinkedList<>(); 
    Queue<String> queue = new LinkedList<>();
~~~    


### Queue 사용법 - 값 추가  

Queue에 값을 추가할때는 add(value), offer(value)를 사용하는데 add는 삽입 성공 여부에 따라 true, IllegalStateException을 반환한다.  

~~~java
    Queue<Integer> stack = new LinkedList<>(); 

    queue.add(1);
    queue.add(2);
    queue.offer(3);
~~~


### Queue 사용법 - 값 삭제  

Queue에 값을 삭제할때는 poll(), remove()를 사용하는데 poll()은 큐가 비어있으면 null로 반환하며 맨 앞에 값을 제거한다. clear()시 모든 요소 제거  

~~~java
    Queue<Integer> queue = new LinkedList<>(); 

    queue.offer(1);
    queue.offer(2);
    queue.offer(3);
    queue.poll();
    queue.remove();
    queue.clear();
~~~


### Queue 사용법 - 값 참조  

Queue에 맨 앞의 값을 참조하고 싶을때는 peek() 메서드를 사용한다.  

~~~java
    Queue<Integer> queue = new LinkedList<>();

    queue.peek();
~~~

***

#### 오늘 성장에 도움을 주신 개발자분  

[출처 : ](https://coding-factory.tistory.com/602) https://coding-factory.tistory.com/602   

오늘도 감사합니다.  
