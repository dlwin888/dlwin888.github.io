---
title: 标签样式初始化
auther: 布莱恩特科比酱
categories: html
tags: html css
abbrlink: '17e2'
date: 2022-09-06 01:47:08
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
---

# 标签样式初始化

**css reset 原则：**

但凡是浏览器默认的样式，都不要使用。

因为每个浏览器下标签的默认样式可能会出现不一致的情况。



人为的将所有样式全部统一（清除），再根据实际情况（设计稿）统一设置。

哪些样式是需要重置的

​	与盒模型相关的样式

- margin
- padding
- border

标签特有的样式

- ​	ul>li
- ​	ol>li			

	书写原则：
	用到什么标签就清除所用标签的默认样式
	建议不要直接将所有标签全部加上。
	不要将所有标签全部统一设置一致的reset，需根据标签默认样式特征来分类设置。

```css
	<style>
		body, h1, h2, h3, h4, h5, h6, p, dl, dd{
			margin: 0;
		}
		ul, ol{
			margin: 0;
			padding: 0;
			list-style: none;
		}
		img{
			border: none;
			vertical-align: top;
		}
		a{
			text-decoration: none;
		}
	</style>
```



