---
title: ccc写类似冬瓜圆效果
date: 2021-04-08 15:10:41
tags: ccs3
---

### html布局：
```js
<h3>200px的正方形</h3>
<!--方法一：-->
<div class="square"></div>
<!--方法二:-->
<div class="product">
    <section class="pro1 pro"></section>
    <section class="pro2 pro"></section>
</div>
```

### css样式
 方法1：用一个div实现
``` css
.square {
width: 240px;
height: 240px;
margin-bottom: 20px;
position: relative;
}
.square::before {
content: '';
position: absolute;
left: 20px;
top: 0px;
width: 200px;
height: 240px;
background-color: #EEA29D;
border-radius: 100px/40px;
}
.square::after {
content: '';
position: absolute;
left: 0;
top: 20px;
width: 240px;
height: 200px;
background-color: #EEA29D;
border-radius: 40px/100px;
}
```
方法2：用三个div叠加实现
``` css
.product {
width: 240px;
height: 240px;
border: 1px solid #9ca6c2;
position: relative;
}
.pro {
width: 200px;
height: 200px;
position: absolute;
background-color: plum;
left: 50%;
top: 50%;
transform: translate(-50%, -50%);
}
.pro1 {
height: 240px;
border-radius: 100px/40px;
}
.pro2 {
width: 240px;
border-radius: 40px/100px;
}
```

 ### 展示效果

 ![方法1效果](https://freedomflyflower.github.io/2021/04/08/ccc写类似冬瓜圆效果/xiaoguo1.png)

 ![方法1效果](https://freedomflyflower.github.io/2021/04/08/ccc写类似冬瓜圆效果/xiaoguo2.png)
