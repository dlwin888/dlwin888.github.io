---
title: 块元素和内联元素
auther: 布莱恩特科比酱
categories: html
tags: html css
abbrlink: d054
date: 2022-09-07 23:46:17
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
---

# 块元素和内联元素

## 块元素特征

1. 默认独占一行
2. 没有宽度时，默认撑满一行
3. 支持所有css命令

## 内联元素特征

1. 同排可以继续跟相同类型的标签
2. 内容撑开高度
3. 不支持宽高
4. 不支持上下的margin
5. 代码换行被解析--空格

## 块和内联的转换

display

- block        显示为块，使行块属性标签具备内联元素的特性
- inline        显示为内联，使内联元素具备块属性标签的特性

```css
div {
	width: 100px;
	height: 100px;
	background: pink;
	display: inline;
}

span {
    width: 100px;
	height: 100px;
	background: pink;
    display: block;
}
```

