# eggforfun
# 参考文档地址：<a href="https://eggjs.org/zh-cn/intro/quickstart.html" target="_blank">https://eggjs.org/zh-cn/intro/quickstart.html</a>

1.初始化如教程中：
```
mkdir egg-example && cd egg-example
npm init egg --type=simple //过程中有四个问号阶段，直接敲回车即可
npm i
```
2.启动服务：
```
//项目目录下敲入命令：
npm run dev
open http://localhost:7001 //默认端口号为7001
```
3.按照文档进行开发即可

## 4.egg-sequelize的用法教程中，有一点比较坑的是使用npx sequelize init:model命令创建的model文件夹下默认有个index.js，如果不将此文件删除，或者不在配置文件config.default.js中进行excloud项配置,运行服务时会报错：app.model.define is not a function
```
config.sequelize = {
        dialect: 'mysql',
        host: '127.0.0.1',
        port: '3306',
        database: 'egg-sequelize-example-dev',
        "username": "root",
        "password": "1234567890",
        exclude:"index.js"
    };
```
