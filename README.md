# app

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


/************************* 注释  *********************/

#  开发中的变更

## 安装的依赖库
npm install fastclick --save   解决点击事件间隔300毫秒的问题
npm install stylus --save      样式
npm install stylus-loader --save  样式
npm uninstall vue-awesome-swiper@2.6.7 --save   轮播图

安装完依赖库需要重启npm  npm run start

## 导入的css样式
border.css  解决在2倍屏或3倍屏下1px显示转化的问题
reset.css   通用的css样式

## 项目结构

res
  assets
    styles
  pages
    home
  router
    index.js
  App.vue
  main.js
  static

