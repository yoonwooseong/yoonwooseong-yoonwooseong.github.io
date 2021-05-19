---
layout: post
title: "object태그란?"
date: 2021-04-05 16:05:00 +0300
image: objectImg.jpg
tags: HTML
---

## object 태그란?  

object 태그는 HTML안에 멀티미디어 객체, 다른 HTML문서나 pdf, 플러그인을 넣을 수 있는 태그이다. 그러나 object는 iframe을 사용할 수 없을 상황에 쓰이는 퇴화 태그로 간주된다. object태그는 설정을 업데이트 해도 반영되지 않는다.  

~~~html
<div id="orgBroadcast" class="sizeclass" style="position: absolute; top: 0px; left: 0px; width: 1280px; height: 720px;">
	<object id="broadcast" type="video/broadcast" style="position: absolute; width: 100%; height: 100%;">
		<param name="zindex" value="0" />
	</object>
</div>
<div id="video" class="sizeclass" style="position: absolute; top: 0px; left: 0px; width: 1280px; height: 720px;">
	<object type="video/mpeg" id="videoObj" style="position: absolute; width: 100%; height: 100%; z-index: 1; ">
		<param name="zindex" value="1" />
	</object>
</div>
~~~


### vs iframe  

iframe도 마찬가지로 HTML 내에 다른 HTML 또는 플래쉬 플레이어를 넣어 재생 시킬 수 있는 태그이다. iframe은 HTML 4.01부터 모든 브라우저에서 지원한다. 차이점은 object태그와 달리 iframe은 사용자 환경설정에 맞춰 역동적으로 반응하고 삽입된 객체도 실시간으로 업데이트된다.


### vs embed  

embed 태그는 정식으로 기술된 요소는 아니었으나 HTML5에서 정식으로 제정되었다. object 태그와는 달리 종료퇴그가 없으므로 자식 태그를 둘 수 없는 차이점이 있다.

***

#### 오늘 성장에 도움을 주신 개발자분  

[출처](https://devbin.kr/html-object-%EC%99%80-iframe-%ED%83%9C%EA%B7%B8/) https://devbin.kr/html-object-%EC%99%80-iframe-%ED%83%9C%EA%B7%B8/  

오늘도 감사합니다.  
