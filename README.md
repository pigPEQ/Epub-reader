# ebook-demo

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
## epubjs的核心工作原理
<img src="imgs/epubjs.png">

## 踩坑与小结
- 中途遇到了这样的报错`Module build failed: TypeError: this.getResolve is not a function at Object.loader`,这个错误的原因是安装的`sass-loader`的版本过高，导致编译失败，查了好久的错误，醉了这也可以，最后将8.0.0版本卸载了装了7.3.1版本就ok啦。
- get到解决eslint问题报错的方法，积累一下。
  - **局部生效:** `/*eslint-disable xxxx*/`。
  - **全局生效:** eslint配置文件中新增一个rule `‘xxxx':'off’`后重启项目。
- vue文件模板设置，积累一下。 
  首选项-代码片段-vue.json中设置
- `reset.scss`是为了消除不同浏览器默认样式的不一致性；
  `global.scss`是规定了整个项目的公共样式、公共方法、公共参数等；
  在`global.scss`中有一个公共的字体转换方法`px2rem`，实现px与rem之间的相互转换，`rem= px / fontSize`。

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
