---
title: 7-HTML 初体验---a标签
auther: 布莱恩特科比酱
categories: html
tags: html
abbrlink: 6ee1
date: 2022-09-03 15:56:54
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
---

# a标签

## 超链接

`<a href="http://www.baidu.com">这是百度的超链接</a>`

- 链接

- 下载

- 锚点

## 伪类是什么

给元素添加特殊的效果

- ：link 未访问过的效果，默认的
- ：visited 访问过后的效果
- ：hover 鼠标移入的效果（悬停）
- ：active 鼠标按下时链接的颜色

## a标签的伪类

```css
	a:link {
		color: black;
	}
	a:visited {
		color: pink;
	}
	a:hover {
		color: red;
	}
	a:active {
		color: plum;
	}
```

## 伪类的顺序

**L V H A**

> 看到ＬＶ ＨＡＨＡ大笑
