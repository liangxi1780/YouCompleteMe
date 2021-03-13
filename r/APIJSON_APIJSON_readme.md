
 
  APIJSON
 
 
 🏆码云最有价值开源项目 🚀后端接口和文档自动化，前端(客户端) 定制返回JSON的数据和结构！ 

 
     
     
     
     
     
 
 
     
     
     
     
     
     
 
 
     
     
     
 
 
   English 
   通用文档 
   视频教程 
   在线工具 
 

 
   
 

---


APIJSON是一种专为API而生的 JSON网络传输协议 以及 基于这套协议实现的ORM库。 
为 简单的增删改查、复杂的查询、简单的事务操作 提供了完全自动化的API。 
能大幅降低开发和沟通成本，简化开发流程，缩短开发周期。 
适合中小型前后端分离的项目，尤其是 BaaS、Serverless、互联网创业项目和企业自用项目。 

通过自动化API，前端可以定制任何数据、任何结构！ 
大部分HTTP请求后端再也不用写接口了，更不用写文档了！ 
前端再也不用和后端沟通接口或文档问题了！再也不会被文档各种错误坑了！ 
后端再也不用为了兼容旧接口写新版接口和文档了！再也不会被前端随时随地没完没了地烦了！

 
     
 


### 特点功能

#### 在线解析
* 自动生成接口文档，清晰可读永远最新
* 自动校验与格式化，支持高亮和收展
* 自动生成各种语言代码，一键下载
* 自动管理与测试接口用例，一键共享
* 自动给请求JSON加注释，一键切换

#### 对于前端
* 不用再向后端催接口、求文档
* 数据和结构完全定制，要啥有啥
* 看请求知结果，所求即所得
* 可一次获取任何数据、任何结构
* 能去除重复数据，节省流量提高速度

#### 对于后端
* 提供通用接口，大部分API不用再写
* 自动生成文档，不用再编写和维护
* 自动校验权限、自动管理版本、自动防SQL注入
* 开放API无需划分版本，始终保持兼容
* 支持增删改查、模糊搜索、正则匹配、远程函数等

 

![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_Auto_get.jpg) 
 
   多表关联查询、结构自由组合、多个测试账号、一键共享测试用例 
 

![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_Auto_code.jpg) 
 
   自动生成封装请求JSON的Android与iOS代码、一键自动生成JavaBean或解析Response的代码 
 

![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_Auto_doc.jpg) 
 
   自动保存请求记录、自动生成接口文档，可添加常用请求、快捷查看一键恢复 
 

![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_Auto_test.jpg) 
 
   一键自动接口回归测试，不需要写任何代码(注解、注释等全都不要) 
 

![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_Auto_summary.jpg) 
 
   一图胜千言 - 部分基础功能概览 
 

  
[以下Gif图看起来比较卡，实际在手机上App运行很流畅]
 
![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_App_MomentList_Circle.gif) 
![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_App_Moment_Name.gif) 
![](https://raw.githubusercontent.com/TommyLemon/StaticResources/master/APIJSON_App_Moment_Comment.gif)

 


### 为什么要用APIJSON？
[前后端 关于接口的 开发、文档、联调 等 10 大痛点解析](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c714925441984264a7ec5b3f53dbe395a8eaa5af20410c19) 


### 常见问题
#### 1.如何定制业务逻辑？
在后端编写 远程函数，可以拿到 session、version、当前 JSON 对象、参数名称 等，然后对查到的数据自定义处理  
https://github.com/APIJSON/APIJSON/issues/101

#### 2.如何控制权限？
在 Access 表配置校验规则，默认不允许访问，需要对 每张表、每种角色、每种操作 做相应的配置，粒度细分到 Row 级  
https://github.com/APIJSON/APIJSON/issues/12

#### 3.如何校验参数？
在 Request 表配置校验规则 structure，提供 NECESSARY、TYPE、VERIFY 等通用方法，可通过 远程函数 来完全自定义  
https://github.com/APIJSON/APIJSON/wiki#%E5%AE%9E%E7%8E%B0%E5%8E%9F%E7%90%86

 
其它问题见 Closed Issues  
https://github.com/APIJSON/APIJSON/issues?q=is%3Aissue+is%3Aclosed


### 快速上手

#### 1.后端部署
可以跳过这个步骤，直接用APIJSON服务器IP地址 apijson.cn:8080 来测试接口。 
见&nbsp; [APIJSON后端部署 - Java](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c7149254419842647a8b6438117b3f8c18b1085904b329bc35ba087cd795dffe2c0c0e32c29c24ff3c9b59ad3eaa7142581936b35e593e95)  

#### 2.前端部署
可以跳过这个步骤，直接使用 [APIAuto-自动化接口管理工具](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c7149254419842646a86a2fda435530c857e7ef40ac42889)  或 下载客户端App。 
见&nbsp; [Android](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c7149254419842647a8b6438117b3f8c18b1085904b329bc7476ce3af38bf60a33bef2f82c791d1c9a68f7e1e5d416c76aa969014139860d)  &nbsp;或&nbsp; [iOS](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c7149254419842647a8b6438117b3f8c18b1085904b329bc6d304e891092f63b237790b16701e2b0)  &nbsp;或&nbsp; [JavaScript](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c7149254419842647a8b6438117b3f8c18b1085904b329bc0a90a8cab9ddfd1a7ec8e58ea093bb93fd49763a77363477ec6a29445c0e6e55)  


### 下载客户端App

仿微信朋友圈动态实战项目 
[APIJSONApp.apk](http://u.720life.cn/g/22e61b846feea038439da3ff01d64b525c9894e40e9d0c35c132603db0b6f829e1a17a13bf79fbb8f8309240f2104414a1f2d53fdb98a3d4de59f902c91397c8) 

测试及自动生成代码工具 
[APIJSONTest.apk](http://u.720life.cn/g/22e61b846feea038439da3ff01d64b525c9894e40e9d0c35c132603db0b6f829e1a17a13bf79fbb8f8309240f2104414049d0572d8e3e776ec1e93d10f227f9c) 


### 使用登记
 
     
     
     
     
     
     
     
     
     
     
 

[更多 APIJSON 使用者](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c714925441984264181e0afbef4dc1ee8aaf38e760ca0abd) 


### 贡献者们
 
     
     
     
     
     
     
     
     
     
     
     
     
   
     
     
     
     
     
     
     
     
     
 
 
感谢大家的贡献。


### 规划及路线图
https://github.com/APIJSON/APIJSON/blob/master/Roadmap.md


### 我要赞赏
如果你喜欢 APIJSON，感觉 APIJSON 帮助到了你，可以点右上角 ⭐Star 支持一下，谢谢 ^_^  
你也还可以扫描下面的二维码，赞助点服务器和域名的购买及维护费用，或者请作者喝一杯咖啡~

  

> 如果希望捐赠之后能获得相关的帮助，可以选择加入下面的付费群来取代普通捐赠，可以获得作者的直接帮助。

如果在捐赠留言中备注名称，将会被记录到列表中~ 如果你也是 Github 开源作者， 
捐赠时可以留下 Github 项目地址或者个人主页地址，链接将会被添加到列表中起到互相推广的作用。


### 技术交流
如果有什么问题或建议可以 [提ISSUE](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c7149254419842640346a5f3b2df895fba90ef4f2f0958fc)  或 加群，交流技术，分享经验。 
如果你解决了某些bug，或者新增了一些功能，欢迎 [贡献代码]https://github.com/TommyLemon/APIJSON/pulls)，感激不尽~

#### QQ解决群 - 607020115（付费）
自开群以来，还是有很多的朋友提出了很多问题，我也解决了很多问题，其中有大半问题是本库的Bug导致，也有些是使用者项目本
身的环境问题，这花费了我大量的时间，经过我的观察和测试，到目前为止，本库的bug已经越来越少，当然不能说完全没有，但是
已经能满足很大部分项目的需求。所以从现在起，我做出一个决定：把之前的讨论群改成解决群，并开启付费入群功能，专为解决大
家在使用本库时遇到的问题，不管是本库bug还是特殊的项目环境导致（包含项目本身的bug）。
我也有自己的工作和娱乐时间，只有大家理解和支持我，我才能专心的为大家解决问题。不过也不用担心，我已经建立了另一个可以免费
进入的QQ讨论群。

#### QQ讨论群 - 734652054（免费）
这个群，免费进入，大家可以相互讨论本库的相关使用和出现的问题，群主也会在里面解决问题，如果提出的问题，群成员不能帮助
解决，需要群主解决，但是要花费群主五分钟以上的时间（本库Bug除外），群主将不会解决这个问题，如果项目紧急，请付费进入解
决群解决（不过注意，付费群中群主会很认真很努力的解决问题，但也不能保证已经能完美解决）或者转换使用其他的开源库。


### 相关推荐
[APIJSON, 让接口和文档见鬼去吧！](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb1736134fc4a722c32d275bba97a3a46434f06ea3fe5d1c81364b21fdd24d6b42c57) 

[仿QQ空间和微信朋友圈，高解耦高复用高灵活](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb1736134fc4a722c32d275bba97a3a46434f63afdb2cca6dfb96bc6462d5760a7777) 

[后端开挂:3行代码写出8个接口！](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb1736134fc4a722c32d275bba97a3a46434ff456d549ba368a4aaec27b969b56bc21) 

[后端自动化版本管理，再也不用改URL了！](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb1736134fc4a722c32d275bba97a3a46434f0f0968691e5bebbca50b9ef39aab4df5) 

[3步创建APIJSON后端新表及配置](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb1736134fc4a722c32d275bba97a3a46434f597bd34bb7e502d3adb0655cf8f0760e) 

[APIJSON 自动化接口和文档的快速开发神器 （一）](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedb31dcc57246cae0262377eb287fa53b392aec8053ffa32b390b7ac9f50b6136bb45ce441f84cd33e0a49dabc95d3bde3) 

[APIJSON在mac电脑环境下配置去连接SQL Server](http://u.720life.cn/g/8a35642bd69eb006eb1f0259b3a6f6f07aac9e1e813866c5ea7a3d36989ba42df8c332fb10df48381074e90c8fb824c8) 

[APIJSON复杂业务深入实践（类似12306订票系统）](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79dedee0bd3bdc4355aebe0b432ae9f977bcfa6b4ee266fc0c934aab2a9a2b0bd96d7a2c0d44e58c7b35cbdb66e54bdcb599a) 


### 生态项目
[APIAuto](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c7149254419842646a86a2fda435530c857e7ef40ac42889)  机器学习测试、自动生成代码、自动静态检查、自动生成文档与注释等，做最先进的接口管理工具

[UnitAuto](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e56d2037be5c320b0b5c2b4b0116244387270007157bc281f1b29912a0ac8fec)  机器学习自动化单元测试平台，零代码、全方位、自动化 测试 方法/函数 的正确性和可用性

[apijson-doc](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046681e01df340d13c078175d8f0fe919c40df65c06955efb713c8ea09267723697)  APIJSON 官方文档，提供排版清晰、搜索方便的文档内容展示，包括设计规范、图文教程等

[APIJSONdocs](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304697d9502be5bd369657991cd522ce4b27b9bdfabfea6f4aa5697c55d799354d2f)  APIJSON 英文文档，提供排版清晰的文档内容展示，包括详细介绍、设计规范、使用方式等

[apijson.org](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461369241104b60be8f6b123aebbbf693fc309df1979ddac5eb40a086a0cb943ab)  APIJSON 官方网站，提供 APIJSON 的 功能简介、登记用户、作者与贡献者、相关链接 等

[APIJSON.NET](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304656970335990a05b01dd2baadfca1f9a6de229295baa69d8d152178ac28496d9c)  C# 版 APIJSON ，支持 MySQL, PostgreSQL, SQL Server, Oracle, SQLite

[apijson-php](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461958acde739646900520e6e27b5caa76c780a590c81cfa53c3b1b7baf5939f77)  PHP 版 APIJSON，基于 ThinkPHP，支持 MySQL, PostgreSQL, SQL Server, Oracle 等

[apijson-node](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e62370e4e5a72023a2b1505521ae325519c801de9075272d05fa850b355e37c7)  Node.ts 版 APIJSON，提供 nestjs 和 typeorm 的 Demo，支持 MySQL, PostgreSQL, SQL Server, Oracle

[uliweb-apijson](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304610dd49a511ff3bd68d3a536de275bca011103afa36bdc73ffbfd4ea6750c0731)  Python 版 APIJSON，支持 MySQL, PostgreSQL, SQL Server, Oracle, SQLite 等

[APIJSON](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046628ba9b2ee84c9c4159310ad50a1bdc7c90d084f75b08651dcef8068be42ad2b)  Go 版 APIJSON，功能开发中...([不可用且长期未更新，期待热心开发者帮助完善或新增项目](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461370b5450d55c91754656777fcd539e5a1a6124333980662ad495489b9aced72) 

[APIJSONKOTLIN](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b6b1cbece7c2f2d4e071a222e63099a502728050fd98155785516d94223d890c)  Kotlin 版 APIJSON，基础框架搭建中...(不可用且长期未更新，期待热心开发者帮助完善或新增项目)

[APIJSONParser](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461e2431b45d942bd8801f6d0d48ad060ee4b6f669bf2bdb2035cc90985b767330)  第三方 APIJSON 解析器，将 JSON 动态解析成 SQL

[ApiJsonByJFinal](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eeaf175e46888e4cb46f3a13faf447baf8b54a74884863f38370e016f4a43b6a5)  整合 APIJSON 和 JFinal 的 Demo

[SpringServer1.2-APIJSON](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d62e80295624325f7847a597401af56da63340b2a6ea78b27a8b7aa006056e3299f07cbcc7c5d1f9dbc429cb261fe1c3)  智慧党建服务器端，提供 上传 和 下载 文件的接口

[AbsGrade](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469e2b69facedbbbb605ebeb22ae8d7eff6b870a2ba11a91ec3a27e99f70b4c02f)  列表级联算法，支持微信朋友圈单层评论、QQ空间双层评论、百度网盘多层(无限层)文件夹等

[APIJSON-Android-RxJava](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c714925441984264dce6057eff2db4f3d3f8528d4787856593b500e5a4c7f7199e31c3e003bb8547)  仿微信朋友圈动态实战项目，ZBLibrary(UI) + APIJSON(HTTP) + RxJava(Data)

[Android-ZBLibrary](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046598225aff184d41175dc54d1af238cb87f7875b22ba80496e0400d17c05c9db5)  Android MVP快速开发框架，Demo全面，注释详细，使用简单，代码严谨


感谢热心的作者们的贡献，点 ⭐Star 支持下他们吧。


### 持续更新
[https://github.com/TommyLemon/APIJSON/commits/master](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462227932fd1e90724c714925441984264fe1478a1a999e228817104b5f640b5a9b1314a17501139f345ec1fcd9b054f70) 

### 码云主页
https://gitee.com/TommyLemon/APIJSON



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)