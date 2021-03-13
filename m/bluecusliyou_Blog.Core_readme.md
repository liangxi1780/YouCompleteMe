Dev Build:: 

  [![Front](https://img.shields.io/badge/Front-VUE-d.svg)](#) [![sdk](https://img.shields.io/badge/sdk-3.1-d.svg)](#)  [![Build status](https://github.com/anjoy8/blog.core/workflows/.NET%20Core/badge.svg)](https://github.com/anjoy8/Blog.Core/actions) [![codecov](https://codecov.io/gh/anjoy8/Blog.Core/branch/master/graph/badge.svg)](https://codecov.io/gh/anjoy8/Blog.Core)  [![License MIT](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/anjoy8/Blog.Core/blob/master/LICENSE) [![Language](https://img.shields.io/badge/language-csharp-d.svg)](#) 
[![star this repo](http://githubbadges.com/star.svg?user=anjoy8&repo=blog.core&style=flat)](https://github.com/boennemann/badges) 
[![fork this repo](http://githubbadges.com/fork.svg?user=anjoy8&repo=blog.core&style=flat)](https://github.com/boennemann/badges/fork) 
[![博客园](https://img.shields.io/badge/博客园-老张的哲学-brightgreen.svg)](https://www.cnblogs.com/laozhang-is-phi/)


&nbsp;
&nbsp;


![Logo](http://apk.neters.club/logocore.png)
![MVP](http://apk.neters.club/MVP_Logo_Horizontal_Preferred_Cyan300_CMYK_72ppi.png)


BCVP（Blog.Core&Vue Project）开箱即用的企业级前后端分离【 .NET Core3.1 Api + Vue 2.x + RBAC】权限框架。 

&nbsp;

### 功能与进度

- [x] 采用仓储+服务+接口的形式封装框架；
- [x] 使用Swagger做api文档；
- [x] 使用MiniProfiler做接口性能分析；
- [x] 使用Automapper做Dto处理；
- [x] 接入SqlSugar ORM，封装数据库操作； 
- [x] 项目启动，自动生成seed种子数据； 
- [x] 五种日志记录，审计/异常/请求响应/服务操作/Sql记录等；  
- [x] 支持自由切换多种数据库，Sqlite/SqlServer/MySql/PostgreSQL/Oracle；
- [x] 异步async/await开发；
- [x] 支持事务；
- [x] AutoFac接入做依赖注入；
- [x] 支持AOP切面编程；
- [x] 支持CORS跨域；
- [x] 支持T4代码模板，自动生成每层代码；
- [x] 支持一键创建自己项目；
- [x] 封装 JWT 自定义策略授权；
- [x] 使用Log4Net日志框架+自定义日志输出；
- [x] 使用SingleR推送日志信息到管理后台；
- [x] 搭配前端Blog项目，vue开发；
- [x] 搭配一个Admin管理后台，用vue+ele开发；
- [x] IdentityServer4 认证;
- [x] API 限速;
- [x] 作业调度 Quartz.net;
- [x] Sqlsugar 读写分离;
- [ ] 支付;
- [ ] Redis/RBMQ 队列;
- [ ] 数据部门权限;


&nbsp;

## 给个星星! ⭐️
如果你喜欢这个项目或者它帮助你, 请给 Star~（辛苦星咯）



&nbsp;

## 官方文档 📕

还在陆续整理中，不过基本操作都在,包括如何新手入门，配置数据，连接DB等等    

[官方文档](http://u.720life.cn/g/707962ff1ff1e6425734f9909dd2a69ec6b35c5b907f10393563da576f540c40)   




&nbsp;

### 系统架构图


![系统架构图](http://apk.neters.club/Blog.Core.System.Architecture.png)

&nbsp;

&nbsp;
### 系统压测结果报告


&nbsp;
其他接口压测内存占用在：220~350 m 之间，具体的，自行压测即可。
&nbsp;



   

这只是 .netCore 后端部分，前端部分请看我的另三个Vue工程项目
 
&nbsp;
&nbsp;
&nbsp;
&nbsp;

|个人博客Vue版本|tBug项目Nuxt版本|VueAdmin权限管理后台|
|-|-|-|
|[https://github.com/anjoy8/Blog.Vue](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467f3e906e677b9963603693da15b43f594b082072efce3fe5410d25a3536a56db90d469d221198142de256e8e4f1cb1c050a9285aa40eb3ed4982d855d62c4cea767d169e54e50fa716c0811979b3b5804ec624662bef54bd942a020102a14dbb9bd79a06bbf91cedb01067489c3f1dc33f8c01960b8d01403e32b46aecceb707677442d62779a2c0eb7cb81c6c129be69cb70dd3eee4e417e3698ac229580f915ef7f43f8b36a1059fc4643db0959550 
|[http://vueblog.neters.club](http://u.720life.cn/g/e10fde1eb560ede81665e88b343691473295a9bd37a0afb212456c0f2ea7a3d35b791b583e2e0cb0d87859b9a43f3bb941dfef28450ec26099eb9da53f6b526bcea26a913eb1c04f76c41334bb500241a4ef12d1b449f9f765c9120e4bfbcc4a98b4c6d01528f8e0f9a2aa90de00cd04e1d54065c68e8a36d5690e65de8d7ad0b43454f26aaa6176e64138cfdbc751c4 



&nbsp;

### 初始项目

#### 不要再使用 .sql 文件了，用下边动图的方法，直接 seed data.

数据查看：[Blog.Core.Data.json](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462175738d4c390e7d421ce2babbdb15782bd09cc62910c2c324371ca2e7e6b5ea900d7d0e999af9bea35bc8baf28902f7d0a9ab6a486bd30f5a4bf23ac87d0996) 

文章讲解：[支持多种数据库 & 快速数据库生成](http://u.720life.cn/g/3e44a884c1d792dd0ec1ac531ed36da98c22769ab16f048e731770f459d0a832346e5ab94e0146f5b2161d0beda23b243efd0168d35917b55cff6dc6b88f86ef) 
 
&nbsp;

 


![操作流程](http://apk.neters.club/operateFlow.gif)


&nbsp;

## Nuget Packages

| Package | NuGet Stable |  Downloads |
| ------- | -------- | ------- |
| [Blog.Core.Webapi.Template](https://www.nuget.org/packages/Blog.Core.Webapi.Template/) | [![Blog.Core.Webapi.Template](https://img.shields.io/nuget/v/Blog.Core.Webapi.Template.svg)](https://www.nuget.org/packages/Blog.Core.Webapi.Template/)  | [![Blog.Core.Webapi.Template](https://img.shields.io/nuget/dt/Blog.Core.Webapi.Template.svg)](https://www.nuget.org/packages/Blog.Core.Webapi.Template/) |


关于如何使用，点击这里：https://www.cnblogs.com/laozhang-is-phi/p/10205495.html

&nbsp;
&nbsp;

## 其他后端框架
目前一共开源四个框架项目，感兴趣的可以看看

|单层项目|简单仓储框架|仓储+服务+接口|DDD框架|
|-|-|-|-|
|CURD+Seed|CURD+Seed+DI|CURD+Seed+DI+AOP等|DDD+EFCore+DI+EventBus等|
|[NetCore-Sugar-Demo](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b1b0cdbcbf86e61f8c3b216e393f2c5ff557f120271cb3afab91a9e5c2f5d6c309ce8f199c3689336d9d947adca1a1b2d4b5afd35ca1c5208759e597142747f88acae368e7f20db5d8e6ce8f2043a3d853536a4ad2067a63ac2305372d2a5588c1c4beaa0ce0cd121c5ab1903dfec7c9e636c2879d24773ad78d799333f1159b4bb11f5c437565f808a20b3a32fa0dcc9251bbe6bc8e821cd6732728326e2615a79b2b527ba8462534e9e613c26751baad1fab562d6cd1f60908956f2ec9c393346d2f0c861320dae37e56b8af30bd79 
| -|[Blog-EFCore-Sqlite](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f2ed3e15746fc974f5dbc27d47f65762ee95854393d57a72c7f4623ab299d935  | -|


&nbsp;



&nbsp;

## 售后服务与支持  

打赏支持，入微信群，随时随地解答我框架中（NetCore、Vue、DDD、IdentityServer4等）的疑难杂症。  
打赏的时候，备注自己的微信号，我拉你进群，两天内没回应，QQ私聊我（3143422472）；  

[赞赏列表](http://u.720life.cn/g/707962ff1ff1e6425734f9909dd2a69ea9ce6957c2ab7aec198ac4bae4e365ef69caa0e979081d64f43de52ac752d569)   

 
 



*****************************************************
### 文章+视频+直播

博客园：https://www.cnblogs.com/laozhang-is-phi/

 Bilibili：https://space.bilibili.com/387802716  
 
 直播间：https://live.bilibili.com/21507364

```
```


&nbsp;

如果你感觉看着这整个项目比较费劲，我单抽出来了几个子Demo，方便学习，项目地址 ：[https://github.com/anjoy8/BlogArti](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304696266af5b70502ea5eab7dbcf79897eaa203ba831d0470d277575a7b8ef73934) 



 
 .NetCore与Vue 框架学习目录如下 
 
 
 后端 .net core 概览 
 
  框架之二 || 后端项目搭建   
  Swagger的使用 3.1  
  Swagger的使用 3.2  
  Swagger的使用 3.3 JWT权限验证【修改】  
  36 ║解决JWT权限验证过期问题  
  API项目整体搭建 6.1 仓储模式  
  API项目整体搭建 6.2 轻量级ORM  
  API项目整体搭建 6.3 异步泛型仓储+依赖注入初探  
  依赖注入IoC学习 + AOP切面编程初探  
  AOP面向切面编程浅解析：简单日志记录 + 服务切面缓存  
  AOP自定义筛选，Redis入门 11.1  
  三种跨域方式比较，DTOs(数据传输对象)初探  
  DTOs 对象映射使用，项目部署Windows+Linux完整版  
  三十二║ 四种方法快速实现项目的半自动化搭建  
  三十三║ ⅖ 种方法实现完美跨域  
  三十四║ Swagger 处理多版本控制，所带来的思考  
  三十五║ 完美实现全局异常日志记录  
  37 ║JWT完美实现权限与接口的动态分配  
   38 ║自动初始化数据库  
  39 || 想创建自己的dotnet模板么？看这里  
  40 || 完美基于AOP的接口性能分析  
   41 || Nginx+Github+PM2 快速部署项目(一)  

  42&nbsp;  ║   完美实现 JWT 滑动授权刷新  
  43 ║ 支持多种数据库 &amp; 快速数据库生成  
  43 ║最全的部署方案 &amp; 最丰富的错误分析【再会】  
  45 ║ 终于解决了事务问题  
  46 ║ 授权认证：自定义返回格式   












 

















 
 
 前端 Vue 概览 
 
  十四 ║ VUE 计划书 &amp; 我的前后端开发简史  
  十五 ║Vue基础：JS面向对象&amp;字面量&amp; this字  
  十六 ║Vue基础：ES6初体验 &amp; 模块化编程  
  十七 ║Vue基础：使用Vue.js 来画博客首页+指令(一)  
  十八║Vue基础: 指令(下)+计算属性+watch  
  十九║Vue基础: 样式动态绑定+生命周期  
  二十║Vue基础终篇：组件详解+项目说明    
 👆 上边的这些基础，可以不用看，如果你只想快速入门 Vue 的话   
  二十一║Vue实战：开发环境搭建【详细版】  
  二十二║Vue实战：个人博客第一版(axios+router)  
  二十三║Vue实战：Vuex 其实很简单  
  二十四║ Vuex + JWT 实现授权验证登陆  
  二十五║初探SSR服务端渲染（个人博客二）  
  二十六║Client渲染、Server渲染知多少{补充}  
  二七║ Nuxt 基础：框架初探  
  二八║ Nuxt 基础：面向源码研究Nuxt.js  
  二九║ Nuxt实战：异步实现数据双端渲染  
  三十║ Nuxt实战：动态路由+同构  
  三十一║ Nuxt终篇：基于Vuex的权限验证探究  
  

















 

















 

















 


 
**************************************************************

 系统环境

    windows 10、SQL Server 08+、Visual Studio 2019、Windows Server 2008 R2

    后端技术：

      * .Net Core 3.1 API（因为想单纯搭建前后端分离，因此就选用的API，如果想了解.Net Core MVC，也可以交流）
      
      * Swagger 前后端文档说明，基于RESTful风格编写接口

      * Repository + Service 仓储模式编程

      * Async和Await 异步编程

      * Cors 简单的跨域解决方案

      * AOP基于切面编程技术

      * Autofac 轻量级IoC和DI依赖注入

      * Vue 本地代理跨域方案，Nginx跨域代理

      * JWT权限验证

 

    数据库技术

      * SqlSugar 轻量级ORM框架，CodeFirst

      * T4 模板生成

      * AutoMapper 自动对象映射

 

    分布式缓存技术

      * Redis 轻量级分布式缓存

 

    前端技术

      * Vue 2.0 框架全家桶 Vue2 + VueRouter2 + Webpack + Axios + vue-cli + vuex

      * ElementUI 基于Vue 2.0的组件库

      * Nuxt.js服务端渲染SSR



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)