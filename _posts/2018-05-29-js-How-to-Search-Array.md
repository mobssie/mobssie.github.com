---
layout: post
title:  "javascript 배열 검색하는 방법"
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

#### Array 메서드를 이용해 배열을 검색해서 특정값을 찾을 수 있다.<br><br><br>


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
<br><br>

#### 5. `forEach()`
`forEach()` 메서드는 배열 요소마다 한 번씩 주어진 함수를 실행한다. 

```javascript
var array1 = ['a', 'b', 'c'];

array1.forEach(function(element) {
  console.log(element);
});

// expected output: "a"
// expected output: "b"
// expected output: "c"
```
```javascript
arr.forEach(callback(currentValue[, index[, array]])[, thisArg]);
```
<br>

> `callback`  <br>
> 각 요소에 대해 실행할 인수 세개를 취하는 함수:  
>> `currentValue`  <br>
> 배열에서 처리될 현재 요소의 값  
>>`index Optional`  <br>
> 배열에서 처리될 현재 요소의 인덱스.  
>> `array Optional`  <br>
> forEach()가 적용되는 배열.  
> `thisArg Optional`  <br>
> callback을 실행할 때 this (예: 참조 객체)로서 사용하는 값.  

<br><br>

#### 6. `map()`
`map()` 메서드는 배열 내의 모든 요소 각각에 대하여 주어진 함수를 호출한 결과를 모아 새로운 배열을 반환한다.<br><br>
```javascript   
var array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]   
```
```javascript   
arr.map(callback(currentValue[, index[, array]])[, thisArg])
```   
> callback
> 새로운 배열 요소를 생성하는 함수. 다음 세 가지 인수를 가집니다.
>> currentValue
> 처리할 현재 요소.
>> index Optional
> 처리할 현재 요소의 인덱스.
>> array Optional
> map()을 호출한 배열.
> thisArg Optional
> callback을 실행할 때 this로 사용되는 값.



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


**참고 사이트**  
: https://developer.mozilla.org/
<br><br><br><br><br><br><br><br>