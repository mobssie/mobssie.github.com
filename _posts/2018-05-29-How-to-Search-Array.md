---
layout: post
title:  "How to Search an Array"
date:   2018-05-29 00:18:23 +0700
categories: [javaScript]
---

### 자바스크립트 배열 검색하는 방법
<br>

#### 1. 일반적으로 `for문` 사용

```javascript
var fruit = false;
for(var i = 0 ; i< arr.length ; i++){
    if(arr[i] === "특정값"){
        fruit = true;
    }
}
```
<br><br>

#### Array 메서드를 이용해 배열을 검색해서 특정값을 찾을 수 있다.<br><br>


#### 2. `indexOf()`와 `lastIndex()`

```javascript
var fruit = new Array("Apple","Banana","Orange","kiwi","melon");
console.log(fruit.indexOf("Banana"));
// 1을 출력
```
```javascript
var fruit = (arr.indexOf("특정값") !== -1);
```
<br><br>




#### 3. `findIndex()`
`findIndex()` 요소가 true를 반환할 때까지 배열의 각 요소에 대해 한 번씩 오름차순으로 호출 함수를 호출한다. 요소가 true를 반환하는 즉시 findIndex에서 true를 반환하는 요소의 인덱스 값을 반환함.true를 반환하는 배열의 요소가 없는 경우 findIndex에서 -1이 반환.

```javascript
var nums = [2,5,3,5,6,100,24,50];

var over = nums.findIndex(function(element){
    return (element >= 100);
});

console.log(nums[over]);
```
<br><br>







#### 4. `filter()`

```javascript
function isValue(value){
    return value >= 10;
}
var filtered = [1,3,6,10].filter(isValue);
//
```








#### 5. `forEach()`

#### 6. `map()`

#### 7. `reduce()`

<br><br>




#### 배열의 일부 추출하기

```javascript
var fruit = ["Apple","Banana","Orange","kiwi","melon"];
var elements  =  fruit.slice(1,3);
console.log(elements);
```
`slice()`메소드는 배열의 일부를 복사해 새로운 배열을 만든다.<br>

***
stringObj.slice(start, [end])

***

<br><br>
