# node-koa2-axios

### 技术栈
* http.request：node http 模块的request方法可以作为httpclient向服务器发起http请求，爬虫需要向目标链接发起http请求来获得页面信息
 * cheerio：通过 http 请求到的页面信息，由于缺乏浏览器的dom解析，看起来就是一段凌乱的字符串，实在糟糕好在我们可以使用 cheerio 库将其解析为 dom ，这样我们就可以使用类似 jquery 的语法去分析页面信息
* koa2-static: koa-static静态资源中间件，可以访问到我们项目中的静态资源
* koa2-cors: 实现数据跨域ajax请求，这个方法关键是在服务器端进行配置
*  axios + promise：由于node单线程的特性，不可避免的需要用到大量异步编程的写法，层层嵌套的回调写法已经 low 了，来试试 promise 的写法

### 掘金文章，帮助你理解
[koa2+node+axios演绎前端数据大戏](https://juejin.im/editor/drafts/5b4160f4f265da0f83646849)
