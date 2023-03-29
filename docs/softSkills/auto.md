---
title: vant ui 自适应
nav:
  title: 前端软技能
  order: 1
group:
  title: h5 开发的注意事项
  order: 1
---

# vant ui 自适应

在开发 `H5` 网页的时候，我们通常会选择已有的 `UI` 框架来快速搭建。但是 `UI` 框架的默认像素单位大多都是使用 `px` 的，而为了做各个手机端的适配，我们通常会使用如 `rem、vw、vh` 等单位。这其中就出现了第一个问题，我们应该怎么样进行单位的相互转换呢？

## 单位转换

> 由于我通常是使用 `rem` 来做适配的，这里的例子也使用 `rem`。

1. 首先，我们需要使用到两个插件 [postcss-pxtorem](https://www.npmjs.com/package/postcss-pxtorem) 和 [amfe-flexible](https://www.npmjs.com/package/amfe-flexible)。

   - `postcss-pxtorem`：将 `px` 转换成 `rem`
   - `amfe-flexible`：用来设置 `rem` 的一个基准值

2. 当我们下载好这两个插件时，就可以进行使用了

   - 在 `main.js` 中引入 `amfe-flexible`

     ```js
     import 'amfe-flexible';
     ```

   - 在当前项目的根目录中添加 `postcss.config.js` 文件

     ```js
     module.exports = {
       plugins: {
         'postcss-pxtorem': {
           rootValue({ file }) {
             // 如果设计稿的尺寸不是 375，而是 750 或其他大小，就可以如下设置
             return file.indexOf('vant') !== -1 ? 37.5 : 75;
           },
           propList: ['*'],
         },
       },
     };
     ```

当完成这些配置时，我们就可以在写的时候可以直接根据设计稿中的 `px` 来编写，而不需要不用手动计算 `rem` 了。
