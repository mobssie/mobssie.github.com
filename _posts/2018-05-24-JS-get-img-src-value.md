---
layout: post
title:  "How get the image src value"
date:   2018-05-24 00:18:23 +0700
categories: [javaScript]
---

#### How get the image src value
```html
<img id="imgThumb" name="img_thumb" src="/pictures/img_thumb.png"  alt="imgThumb" />
```
```javascript
if (document.getElementById('imgThumb').getAttribute('src') == "pictures/imgThumb.png")
```
