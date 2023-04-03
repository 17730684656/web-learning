---
title: 常用 CSS
nav:
  title: 前端常用代码
  order: 4
group:
  title: css
  order: 1
---

1. 首行缩进

   ```css
   /* 值可以是负数，负数的话将第一行左缩进 */
   /* 该值是可以被 继承 的 */
   /* 属性值有三种： */
   /*   1. length：固定的缩进，默认值是 0 */
   /*   2. %：基于父元素宽度的百分比缩进 */
   /*   3. inherit：从父元素继承 text-indent 的属性值 */
   text-indent: 2em;
   ```

2. 文本溢出隐藏

   ```css
   /* 单行文本缩进 */
   overflow: hidden; /* 超出部分进行隐藏 */
   white-space: nowrap; /* 使文本不进行换行 */
   text-overflow: ellipsis; /* 超出部分的文字使用省略号代替 */

   /* 多行文本缩进 */
   overflow: hidden; /* 超出部分进行隐藏 */
   text-overflow: ellipsis; /* 超出部分的文字使用省略号代替 */
   display: -webkit-box; /* CSS3 属性，流体布局 --- 弹性盒子 */
   -webkit-line-clamp: 3; /* 可以展示的行数 */
   -webkit-box-orient: vertical; /* 子元素的排列方式  vertical：垂直   orhorizontal：水平 */
   ```
