---
layout: post
title:  "image src value값 바꾸기"
date:   2018-05-25 00:18:23 +0700
categories: [javaScript]
---
<br><br>

#### How get the image src value

```html
<img id="imgThumb" name="img_thumb" src="/pictures/img_thumb.png"  alt="imgThumb" />
```
```javascript
if (document.getElementById('imgThumb').getAttribute('src') == "pictures/imgThumb.png")
```

<br>

#### 배열에 SRC 값을 추출 해서 넣기 <br>

```javascript
function img_find() {
    var imgs = document.getElementsByTagName("img");
    var imgSrcs = [];

    for (var i = 0; i < imgs.length; i++) {
        imgSrcs.push(imgs[i].src);
    }

    return imgSrcs;

}
```
<br><br><br><br><br><br><br><br>