---
title: CSS 动画权威笔记
tags: css
categories: css
comments: false
date: 2026-04-22 18:47:13
---

### 📖 CSS 动画权威笔记

## 一、CSS 动画两大核心（90% 动画都靠它）

### 1. transition（过渡动画）

**作用**：两个状态之间的平滑变化（hover / 显示隐藏）

```css
/* 基础写法 */
transition: 变化属性 时长 速度曲线 延迟;

/* 实用写法 */
transition: all 0.3s ease;
```

**能做什么**

- 按钮 hover 放大、变色
- 弹窗淡入淡出
- 滑入滑出侧边栏
- 输入框聚焦效果

------

### 2. @keyframes（关键帧动画）

**作用**：自定义一段连续动画（循环、自动播放）

```css
@keyframes 动画名 {
  from { 初始状态 }
  to { 结束状态 }
}

/* 或百分比 */
@keyframes move {
  0%  { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
  100%{ transform: translateY(0px); }
}
```

**使用**

```css
animation: move 2s infinite;
```

**能做什么**

- 加载动画
- 呼吸灯
- 打字机
- 脉冲、漂浮、抖动

------

## 二、动画三大神技（必须背下来）

### 1. transform（变形）

```css
transform: translateX(10px);   /* 左右移动 */
transform: translateY(10px);   /* 上下移动 */
transform: scale(1.1);         /* 缩放 */
transform: rotate(45deg);      /* 旋转 */
transform: skew(10deg);        /* 倾斜 */
```

**所有动画 90% 都靠它！**

------

### 2. opacity（透明度）

淡入淡出必备

```css
opacity: 0;   /* 隐藏 */
opacity: 1;   /* 显示 */
transition: opacity 0.5s;
```

------

### 3. animation 常用组合

```css
animation: 名称 时长 曲线 延迟 次数 方向;

例子：
animation: breath 2s ease-in-out infinite;
```

常用值：

- `infinite` 无限循环
- `ease` 慢快慢（最自然）
- `linear` 匀速
- `ease-out` 快到慢（退场用）
- `ease-in` 慢到快（进场用）

------

## 三、接单最常用 12 个动画模板（直接复制）

### 1. 按钮 hover

```css
.btn {
  transition: all 0.3s;
}
.btn:hover {
  transform: scale(1.05);
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}
```

### 2. 加载动画

```css
.loader {
  width:30px; height:30px;
  border:3px solid #eee;
  border-top:3px solid blue;
  border-radius:50%;
  animation: spin 1s linear infinite;
}
@keyframes spin {
  to { transform:rotate(360deg) }
}
```

### 3. 呼吸灯

```css
.breath {
  animation: breath 2s infinite;
}
@keyframes breath {
  0%,100% { transform:scale(1); opacity:1; }
  50% { transform:scale(1.1); opacity:0.7; }
}
```

### 4. 漂浮动画

```css
.float {
  animation: float 2s infinite ease-in-out;
}
@keyframes float {
  0%,100% { transform:translateY(0); }
  50% { transform:translateY(-8px); }
}
```

### 5. 抖动（错误提示）

```css
.shake {
  animation: shake 0.5s;
}
@keyframes shake {
  0%,100%{transform:translateX(0)}
  25%{transform:translateX(-5px)}
  75%{transform:translateX(5px)}
}
```

### 6. 淡入上移

```css
.fade-in {
  opacity:0;
  transform:translateY(30px);
  transition:0.8s;
}
.fade-in.show {
  opacity:1;
  transform:translateY(0);
}
```

### 7. 3D 翻转

```css
.flip {
  transform-style: preserve-3d;
  transition: 0.6s;
}
.flip.active {
  transform: rotateY(180deg);
}
```

### 8. 脉冲扩散

```css
.pulse::after {
  content:'';
  position:absolute;
  border-radius:50%;
  animation:pulse 1.5s infinite;
}
@keyframes pulse {
  to{transform:scale(1.5);opacity:0}
}
```

### 9. 打字机

```css
.type {
  width:0;
  overflow:hidden;
  white-space:nowrap;
  border-right:2px solid #000;
  animation:typing 2s steps(15) forwards;
}
```

### 10. 扫光效果

```css
.shine::after {
  content:'';
  position:absolute;
  left:-100%; width:50%; height:100%;
  background:linear-gradient(to right,transparent,#fff5,transparent);
  animation:shine 2s infinite;
}
```

### 11. 缩放弹入

```css
.zoom {
  transform:scale(0.3); opacity:0;
  transition:0.5s cubic-bezier(0.34,1.56,0.64,1);
}
.zoom.show {
  transform:scale(1); opacity:1;
}
```

### 12. 展开 / 收起

```css
.collapse {
  max-height:0; overflow:hidden;
  transition:max-height 0.5s;
}
.collapse.open {
  max-height:300px;
}
```

------

## 四、JS + CSS 动画黄金公式

```javascript
元素.addEventListener('点击', () => {
  目标元素.classList.toggle('动画类名')
})
```

**所有交互动画都靠这一行！**

------

## 五、接单动画性能规则（必看）

- 只动画：`transform` 和 `opacity`
- 不要动画：`width` `height` `top` `left` `margin`
- 动画越简单，页面越流畅
- 循环动画尽量加 `will-change: transform`