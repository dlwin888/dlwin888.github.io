---
title: 文字
auther: dlwin888
abbrlink: 90a6
date: 2022-08-31 02:04:24
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary: 文字着重、文字倾斜、文字大小、字体、行高
categories: css
tags: css
---

# 文字

## 文字着重

font-weight 

- bold 加粗
- normal 正常

## 文字倾斜

font-style 

- talic 斜体
- normal 正常

## 文字大小

font-size

## 字体

font-family

## 行高

line-height：文字在一行里所占用的位置

当行高的值与高度一致时，文字会**垂直居中**

**多行文字测量行高的方法**：

1. 确认文字大小

2. 确认两行文字之间的大小

3. 空隙大小除以2，得出来的值就是每行文字的上下的空隙大小

   1. 当行高为奇数时，那么文字的上方要比下方少一个像素
   2. 当行高为偶数时，上下空隙值一致

4. 画辅助线测量

   

```css
div {
    font-weight: normal;
    font-style: italic;
    font-size: 16px;
    font-family: "微软雅黑";
    line-height: 16px;
    border: 1px solid red;
}

/*复合样式 要注意书写顺序*/
div {
    font: bold italic 26px/32px "楷体"；
}
```



