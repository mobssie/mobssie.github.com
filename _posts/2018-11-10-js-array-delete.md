---
layout: post
title:  "javascript 배열 요소 삭제 또는 치환"
date:   2018-11-10 00:18:23 +0700
categories: [javaScript]
---
<br/><br/><br/><br/><br/>
Array 객체의 index()와 splice()를 사용해 배열 요소를 삭제/치환.

```javascript
var fruits = new Array("apple", "banana", "pineApple", "orange", "banana");
    // 배열에서 요소 삭제하기
    fruits.splice(fruits.indexOf("apple"),1);
    document.write("결과 : ");
    document.write(fruits.toString());
    document.write("<br>");
    // 새로운 요소 삽입하기
    fruits.splice(fruits.lastIndexOf("banana"),1,"berry");
    document.write("결과 : ");
    document.write(fruits.toString());
    document.write("<br><br>");
```
1. concat()메서드는 한 개 이상의 배열을 매개 변수로 받아서, 메서드를 호출한 부모 배열의 끝에 변수로 받은 배열 요소를 추가함.<br/>
```javascript
    var newArray = num[0].concat(num[1],num[2],num[3]);
```
<br/><br/>
2. 장황하고 오류나기 쉬움. (루프나 재귀도 마찬가지)<br/>
3. apply() 메서드는 한수에 주어진 배열 인수들로 concat() 메서드 호출<br/>