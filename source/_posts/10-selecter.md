---
title: 选择器
auther: 布莱恩特科比酱
categories: html
tags: html css
abbrlink: a05a
date: 2022-09-07 00:20:03
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
---

# 选择器

## id选择器

唯一

`<div id="box"></div>`

`#box {`

`}`

## 类选择器

`<div class="box"></div>`

`.box {`

`}`

可以是多个class加在同一个元素上

## 标签选择器

`div {`

​	`width:100px;`

​	`height:100px;`

`}`

当前页面上所有标签为xxx的元素

## 群组选择器

`div,p,h1 {`

​	`width:100px;`

​	`height:100px;`

​	`color:pink;`

`}`

用逗号分隔，被逗号分隔的元素统一使用相同的样式

## 包含选择器

.box div {

}

目标范围 目标元素

## 通配符

` body *  {`

​	`margin:10px;`

​	`pading:10px;`

​	`border:1px solid #fff;`

`}`

找到页面上符合规则的所有元素

**不建议使用**



## 选择器的优先级

代码执行生效的顺序：

> 行间样式> id选择器 > 类选择器 > 元素选择器

> 行间样式 			1000
>
> id选择器 			100
>
> 类选择器			10
>
> 元素选择器		1
