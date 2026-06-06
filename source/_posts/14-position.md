---
title: 定位
auther: 布莱恩特科比酱
categories: css
tags: html css
abbrlink: '3720'
date: 2022-09-14 01:16:17
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
---

# 定位

## 定位的思考

## 相对定位的特征

position:`relative`;

- 不影响元素本身的特性
- 不使元素脱离文档流（元素移动之后原始位置被保留）
- 如果没有定位偏移量，对元素本身没有任何影响
- 提升层级

## 绝对定位的特征

`position`:absolute;

- 使元素完全脱离文档流
- 使内联元素支持宽高
- 块属性标签内容撑开宽度
- 如果有定位父级相对于定位父级发生偏移，没有定位父级相对于document发生偏移
- 相对定位一般都是配合绝对定位使用
- 提升层级

## z-index:[number] 定位层级

## 固定定位

与绝对定位的特性基本一致，但差别是始终相对于整个文档进行定位

问题; IE6不支持固定定位

## 定位其它值

- static	默认值
- inherit 从父元素继承定位属性的值（不兼容）



## 定位清浮动

position:absolute;绝对定位子元素子级的浮动可以不用写清浮动的方法

position:fixed;  固定定位元素子级的浮动可以不用写清浮动的方法



## 遮罩弹窗（优酷弹窗）

标准 不透明度 ： opacity: 0~1;

IE滤镜： filter: alpha(opacity=0~100)；

