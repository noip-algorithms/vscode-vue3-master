---
title: 七、Float浮动
tags: CSS
date: January 11 2021
commit: true
---
## 1.文档目录

### 1.1 什么是 CSS 浮动

1. 设计的初衷是为了实现文字环绕效果；

2. 浮动元素只能在水平方向浮动

+ `float: left` or `float-right`;

+ 详见： `01-float-left.html` and `02-float-right.html`

3. 浮动元素将会脱离文档流；

+ 详见： `01-float-off-stream.html`

4. 浮动元素会生成一个块级框，直到该块级框的外边缘碰到包含框或者其他的浮动框为止；

### 2. 浮动引起的问题

1. 在父级元素未设置高度时，父元素高度由子元素高度决定，当子元素浮动时父级元素高度塌陷；

2. 因浮动脱离文档流，浮动元素之后的元素会被浮动元素覆盖；

3. 两栏布局,左边固定宽度，因为左边栏左浮动，脱离了文档流，而右边栏不设宽，因此右边栏的宽度自适应，随浏览器窗口大小的变化而变化，这样造成右边栏内容被左边栏覆盖；

### 3. 解决办法

#### 3.1 清除浮动

1. 给父级元素设置高度： (不推荐)；

+ 详见：`05-float-father-height.html`;

2. 父级元素定义 伪类:after 

+ 详见： `06-float-after.html`

4. 父级元素块级格式化上下文(BFC): `overflow: hidden;`;

+ `07-float-father-overflow.html`

#### 3.2 浮动元素脱离文档流

1. 在浮动元素结尾处加空div标签 clear:both

+ clear属性

  1) none： 默认值，不做任何清除浮动的操作；

  2) left： 清除前面元素左浮动带来的影响；

  3) right： 清除前面元素右浮动带来的影响；

  4) both： 清除前面元素所有浮动带来的影响；

+ 详见： `08-float-clear.html`

2. 给浮动元素添加一个父级元素，并且使之块级格式化上下文(BFC): `overflow: hidden;`

#### 3.3 BFC

1. 给父级元素设置;

## 2.参考文档

[CSS教程]()

## 3. 联系方式
Email:yuanmin8888@outlook.com