---
layout: post
title:  "javascript concat과 apply 사용하기"
date:   2018-11-11 00:18:23 +0700
categories: [javaScript]
---
<br/><br/><br/><br/><br/>
```javascript
var num = [];
    num[0] = [1,2];
    num[1] = [3,4];
    num[2] = [5,6];
    num[3] = [7,8];
    // 평평해진 배열
    var newArray = num.concat.apply([],num);
    document.write("결과 : ");
    document.write(newArray[5]);
    document.write("<br><br>");
```
1. concat()메서드는 한 개 이상의 배열을 매개 변수로 받아서, 메서드를 호출한 부모 배열의 끝에 변수로 받은 배열 요소를 추가함.<br/>
```javascript
    var newArray = num[0].concat(num[1],num[2],num[3]);
```
<br/><br/>
2. 장황하고 오류나기 쉬움. (루프나 재귀도 마찬가지)<br/>
3. apply() 메서드는 한수에 주어진 배열 인수들로 concat() 메서드 호출<br/>