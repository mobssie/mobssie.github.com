---
layout: post
title:  "Node.js File System Module"
date:   2018-05-24 00:18:23 +0700
categories: [nodeJS,javaScript]
---

#### Node.js as a File Server
Node.js file system module을 사용하면 컴퓨터의 파일 시스템을 사용하여 작업 할 수 있다.<br>
파일 시스템 모듈을 포함하려면 `require()` 을 사용할 것.

```javascript
var fs = require('fs');
```
<br>

#### 파일 시스템 모듈의 일반적인 사용 : <br>
* 파일 읽기 <br>
* 파일 만들기 <br>
* 파일 업데이트 <br>
* 파일 삭제 <br>
* 파일 이름 바꾸기 <br>
<br>

#### 파일 읽기 <br>
`fs.readFile()`방법은 컴퓨터 파일을 읽는데 사용된다.<br>
Node.js와 같은 폴더에 HTML 예시<br>

```html
demofile.html

<html>
<body>
    <h1>My Header</h1>
    <p>My paragraph.</p>
</body>
</html>
```
HTML 파일을 읽고, 내용을 반환하는 Node.js 파일 만들기<br>

```javascript
var http = require('http');
var fs = require('fs');
http.createServer(function (req, res) {
  //Open a file on the server and return it's content:
  fs.readFile('demofile1.html', function(err, data) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write(data);
    return res.end();
  });
}).listen(8080);
```
<br>
위의 코드를 "readfile.js"파일에 저장하고 파일을 시작.<br>

```
$ node demo_readfile.js
```
[http://localhost:8080](http://localhost:8080)<br>
<br><br>

#### 파일 만들기 <br>
파일 시스템 모듈에서 새 파일을 만든 방법 세가지 <br>
1. fs.appendFile() <br>
2. fs.open() <br>
3. fs.writeFile() <br><br>

`fs.appendFile()`메서드 : <br>
지정된 내용을 파일에 추가한다.
파일이 존재 하지 않으면 파일으 생성된다. <br>


#### Ref.

##### appendFile() 메서드를 사용하여 새 파일을 만듭니다.

```javascript
var fs = require('fs');
fs.appendFile('mynewfile1.txt','Hello content!',function(err){
    if(err) throw err;
    console.log('Saved!');
});
```

###### - throw 문(JavaScript) : try...catch...finally 문에서 처리할 수 있는 오류 조건을 만듬<br>
<br>
`fs.open()`메서드 : <br>
두 번째 인수로 "플래그"를 사용하고, 플래그가 "쓰기"에 대해 "w"이면 지정된 파일이 쓰기 위해 열림.파일이 없으면 빈 파일이 만들어짐. <br>

###### - 플래그(flag) : 컴퓨터에서 무언가를 기억하거나 또는 다른 프로그램에게 약속된 신호를 남기기 위한 용도로 프로그램에 사용되는 미리 정의된 비트<br>

#### Ref.

##### open () 메서드를 사용하여 비어있는 새 파일을 만들기

```javascript
var fs = require('fs');
fs.open('mynewfile2.txt', 'w',function(err,file){
    if(err) throw err;
    console.log('Saved!');
});
```










