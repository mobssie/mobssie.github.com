---
layout: post
title:  "Javascript로 클래스 선택하여 제어하기"
date:   2018-11-09 00:18:23 +0700
categories: [javaScript, Jquery]
---


<br/><br/>
### javascript로 클래스 선택하여 제어하기 (jquery와 비교)
<br/><br/>
기존에 javascript에서 class를 추가하거나 제거하려면 string를 제어해야 하는 문제때문에 불필요한 작업을 해야만 했었다. 물론 jquery를 이용하면, 이러한 쉽게 class를 제어할 수 있었다. 하지만 이제는 javascript에서도 쉽게 class를 제어할 수 있는 방법이 나왔다. 이번에 소개할 것은 classList라는 것이다.<br/><br/>

classList는 add, remove, contains, toggle 함수를 제거한다.<br/>
jquery의 addClass, removeClass, hasClass, toggleClass와 동일하게 추가, 제거, 클래스 포함여부, 토글(on/off)이다. 단 사용법은 조금 다르니 아래의 소스를 확인해 보자.<br/><br/>

먼저 jquery class 제어 소스이다.<br/>
```javascript
$( '#element' ).addClass( 'someclass' );
$( '#element' ).addClass( 'someclass1 someclass2' );
$( '#element' ).removeClass( 'someclass' );
$( '#element' ).removeClass( 'someclass1 someclass2' );
$( '#element' ).hasClass( 'someclass' );
$( '#element' ).hasClass( 'someclass1 someclass2' );
$( '#element' ).toggleClass( 'someclass' );
```
```javascript
var element = document.getElementById( 'element' );

element.classList.add( 'someclass' );
element.classList.add( 'someclass1', 'someclass2' );
element.classList.remove( 'someclass' );
element.classList.remove( 'someclass1', 'someclass2' );
element.classList.contains( 'someclass' );
element.classList.contains( 'someclass1', 'someclass2' );
element.classList.toggle( 'someclass' );
<br/><br/><br/>
```
**참고사이트
: http://blim.co.kr/archives/160

<br/><br/><br/>