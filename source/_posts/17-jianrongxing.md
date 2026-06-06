---
title: 浏览器兼容性
auther: 布莱恩特科比酱
categories: html
tags: html css
abbrlink: 5b9
date: 2022-09-22 02:48:42
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
---

# 浏览器兼容性

- H5标签兼容

- 元素浮动后，能设置宽度的话就给元素加宽度，如果需要宽度是内容撑开，就给它里面的块元素加上浮动

- 第一块元素浮动，第二块元素加margin值等于第一块元素，在IE6下会有间隙问题

- IE6 下子元素超出父级宽高，会把父级的宽高撑开

- P包含块元素嵌套规则 td h标签

- margin传递 叠压

- 元素浮动后再加margin，IE6 7 会产生双倍边距

  > 添加 *display:inline;

- li浮动元素4px问题 IE6

  > *vertical-alin: top

- IE6文字复制问题 

  - 两个浮动元素中间有注释或者内联元素
  - 和父级宽度相差不超过3px
  - 解决方案：两个浮动元素避免注释或者内联元素
  - 和父级宽度相差超过3px以上

- IE6父级元素的overflow:hidden是包不住子级的relative

- IE6下绝对定位元素父级宽高是奇数，绝对定位元素的right和bottom值会有1px的偏差

- IE6下input的空隙

- IE6下输入类型表单控件背景问题 

- CSS Hack

  - \9 所有的IE10以下的
  - \+ \* IE7及以下的
  - \_ IE6及以下的

```css
div {
	background-color:red;
	background-color:blue\9;
	*background-color:green;
	_background-color:yellow;
}
```

- IE6不支持png24图片
  - js插件
  - 滤镜
- ！important 提升样式优先级权重
