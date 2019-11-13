#### koa  基于nodejs 平台的下一代web开发框架。

express 原班人马打造的

#### 安装

npm i koa -S

#### koa中间件  异步函数

async (ctx,next) => {
    
}


ctx 封装了 请求体和响应体

>请求体： /search?key=羽绒服

ctx.request.path   请求路径   简写成：ctx.path   /search

ctx.request.url    请求路径   简写成：ctx.url    /search?key=羽绒服

ctx.request.query  get请求传递的参数   简写成：ctx.query {key:'羽绒服'}

ctx.request.querystring  get请求传递的参数 简写成：ctx.querystring  key=羽绒服

>响应体

ctx.response.body 省略写成 ctx.body  响应任何数据类型

>中间件

koa-static

koa-bodyparser  处理前端post请求携带的参数，放到ctx.request.body  切记不能简写

koa-router  处理路由

#### nodemon 自动重启

npm i nodemon -g

nodemon <执行文件的路径>

#### koa-static 处理静态资源

npm i koa-static -S

const static = require('koa-static')

app.use(static(path.join(process.cwd(),'public'))

#### phpStudy

启动mysql数据库

#### navicate  

mysql数据库的可视化工具

1.新建连接  只建一次

2.新建数据库

库 --->  表 至少有一个主键   字段 --->  类型（int  varchar datetime）

主键的作用：用来查找

#### postman  

调试接口的

#### mysql

npm i mysql -S

sql语句：增删改查

1.创建连接对象

2.连接 connect

3.连接对象.query(sql语句,[参数1,参数2，参数3,...],(error,data) => {})

>sql语句：增删改查

查：select <字段名>*(所有的列) from <表名>  where 字段名=?

模糊搜索：select * from <表名> where 字段 like '%${key}%'  %:任意字符

增：insert into <表名> (字段1，字段2，字段3....) values (?,?,?....)

删：delete from <表名> where 字段名=?

改: update <表名> set 字段1=?,字段2=?,.... where  字段名=?










