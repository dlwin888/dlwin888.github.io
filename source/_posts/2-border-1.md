---
title: 边框
auther: dlwin888
abbrlink: '5652'
date: 2022-08-29 07:50:34
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
categories: css
tags: css
---

# 边框

## 边框的语法规则、边框的单一方向条件设置

**语法**：

**边框的语法规则**

​		1.边框的粗细

​        2.边框的样式

​        3.边框的颜色

​	边框的方向

​		top right bottom left

border

- border-top
  - border-top-width
  - border-top-style
  - border-top-color
- border-right
  - border-right-width
  - border-right-style
  - border-right-color
- border-bottom
  - border-bottom-width
  - border-bottom-style
  - border-bottom-color
- border-left
  - border-left-width
  - border-left-style
  - border-left-color

```css
	<style type="text/css">
		div {
			width: 400px;
			height: 400px;
			border: 1px solid red;
			border-right: 5px dashed blue;
			border-top-color: blue;
		}
	</style>
```



## 边框的特性、使用边框实现三角形

**边框的形状**：非矩形

```
#div1 {
    width: 0;
    height: 0;
    border: 20px solid red;
    border-color: black blue green red;
}
```

<img src="/uploads/image-20220828184404871.png" alt="image-20220828184404871" style="zoom:200%;" />

```css
#div2 {
    width: 0;
    height: 0;
    border: 10px solid #fff;
    /*border-top-color: #ccc;*/
    border-left-color: #ccc;
}
```

<img src="/uploads/image-20220828184832604.png" alt="image-20220828184832604" style="zoom:200%;" />



## 边框样式练习

1. 先分析设计图的结构
2. 根据所分析的结构，进行结构编码
3. 根据所书写的结构，进行css编码
4. 利用ps工具，对设计图上的模块进行测量以及颜色的拾取
5. 样式添加
