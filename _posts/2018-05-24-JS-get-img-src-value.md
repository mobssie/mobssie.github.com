---
layout: post
title:  "How get the image src value"
date:   2018-05-24 00:18:23 +0700
categories: [javaScript]
---

#### image src value값 바꾸기
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