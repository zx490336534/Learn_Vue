# hello-Vue

# 2019-3-20：开始Vue的学习

### 环境
- 浏览器：Chrome
- IDE：WebStorm
- Node.js 8.9+ npm

### Vue CLI
- npm install -g @vue/cli
- vue create hello-world
- cd hello-world
- npm run serve


# 2019-3-21：Vue组件的核心概念
**Vue组件 = Vue实例 = new Vue(options)**
## 属性
- 自定义属性 props
组件props中声明的属性
- 原生属性 attrs
没有声明的属性，默认自动挂载到组件根元素上，设置inheritAttrs为false可以关闭自动挂载
- 特殊属性 class style
挂载到组件根元素上，支持字符串，对象，数组等多种语法
## 事件
- 普通事件
@click，@input，@change，@xxx等事件，通过this.$emit('xxx',...)触发
- 修饰符事件
@input.trim,@click.stop,@submit.prevent等，一般用于原生HTML元素，自定义组件需要自行开发支持
## 插槽
- 普通插槽
`<template slot="xxx">...</template>`
`<template v-slot="xxx">...</template>`
- 作用域插槽
`<template slot="xxx" slot-scope="props>...</template>`
`<template v-slot:xxx="props">...</template>`

### 双向绑定
- model更新view
- view更新model
### 单向数据流
- model更新view
#### ⚠️注意
- Vue是单向数据流，不是双向绑定
- Vue的双向绑定不过是`语法糖`
- Object.defineProperty是用来做响应式更新的，和双向绑定没关系
