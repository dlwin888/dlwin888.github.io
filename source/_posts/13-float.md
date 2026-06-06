---
title: 浮动
auther: 布莱恩特科比酱
categories: css
tags: css
abbrlink: 1dcc
date: 2022-09-13 02:10:49
img:
top:
cover:
coverImg:
password:
toc:
mathjax:
summary:
---

# 浮动介绍及基本语法

float:

- left
- right
- none
- inherit

**文档流是文档中可显示对象在排列时所占用的位置**

## 浮动的定义

使元素脱离文档流，按照指定方向发生移动，遇到父级边界或者相邻的浮动元素停了下来

## 浮动清除

clear: 

- left
- right
- none
- inherit
- both 左右两侧都不能有浮动

元素的某个方向不能有浮动

## float特征

1. 块在一行显示
2. 内联支持宽高
3. 默认内容撑开宽度
4. 脱离文档流
5. 提升层级半层

## 清除浮动的方法

1. 加高

   - 扩展性不好

2. 父级加浮动

   - 页面中所有元素加浮动，margin左右自动失效(float bad!)

3. inline-block清浮动

   - margin左右自动失效

4. 空标签清除浮动

   - ie6下最小高度19px,解决后还有2px偏差

5. .br清浮动

   - 不符合工作中：结构、样式、行为三者分离的要求

6. after伪类

   **最优雅的解决方案**

   ```css
   .clearfix {
       *zoom:1;
   }
   .clearfix:after{
        content: "";
        display:block;
        clear:both;
   }
   ```

7. overflow:hidden清除浮动

   - 需要配合宽度或者zoom兼容IE6 7
   - 溢出隐藏

   ## BFC haslayout

   BFC(Block formatting context) 标准浏览器

   1. float的值不为none
   2. overflow的值不为visible
   3. display的值为table-cell、table-caption,inline-block中的任何一个
   4. position的值不为relative和static
   5. width|height|min-width|min-height:(!auto)

   haslayout IE浏览器

   1. writing-mode:tb-rl
   2. -ms-writting-model:rb-rl
   3. zoom:(!normal)

   只要触发了bfc/haslayout那么这个区域就是一个独立的渲染区域，不受外界影响

