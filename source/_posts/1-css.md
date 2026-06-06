---
abbrlink: '0'
title: 样式表
author: dlwin888
tags: css
categories: css
date: 2022-08-29 07:04:00
---
# 1-行间样式、内联样式表、外联样式表

**行间样式**：给单独的标签添加样式

语法：`<div style="……"></div>`



**内部样式表**：写在style标签内,针对当前html文件有效

语法：

```css
	<style type="text/css">
		div {
			width: 100px;
			height: 100px;
			background: pink;
		}
	</style>
```



**外部样式表**：写在外部css文件中，通过link标签引入

语法：

`<link rel="stylesheet" type="text/css" href="style.css">`
