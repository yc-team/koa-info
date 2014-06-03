koa-info
========

## 简介：

1. 使用 koa 编写 web 应用，通过组合不同的generator，可以免除重复繁琐的回调函数嵌套，并极大地提升常用错误处理效率。
2. Koa 不在内核方法中绑定任何中间件，它仅仅提供了一个轻量优雅的函数库。


## 安装

node >= 0.11.9，要支持generator

```shell
npm install koa
node app.js --harmony
```

## 代码级联：

Koa 的做法不是简单的将控制权依次移交给一个又一个的中间件直到程序结束，
Koa 执行代码的方式有点像回形针，用户请求通过中间件，遇到 yield next关键字时，会被传递到下一个符合请求的路由（downstream），在 yield next 捕获不到下一个中间件时，逆序返回继续执行代码（upstream）


## 配置：

* app.name 				 应用名称
* app.env 				 执行环境 
* app.proxy              哪些proxy header参数会被加入到信任列表里面
* app.subdomainOffset    
* app.outputErrors




