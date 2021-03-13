## Seezoon项目介绍 ##
基于spring,mybatis,shiro面向接口开发的的一套后台管理系统，方便快速开发；采用常用的技术栈，降低学习成本，项目完全前后端分离，后端定义统一的接口格式，统一参数校验，统一权限控制，异常拦截，全局错误码等，让后续开发只需关注业务代码。

项目定位于快速开发，所以不需要复杂的分布式，分模块的的开发方式，方便快速部署升级，项目支持按钮级别权限控制，自动控制按钮隐藏显示，按钮支持父子权限，支持本地和云存储。

前端采用最简单jquery + wayjs(双向数据绑定)，wayjs 只做数据绑定这一件事，所以入门非常快，几分钟就可以熟练使用，这也是没有采用Vue的原因，这里引入nodejs工具gulp 打包工具，方便编译出前端文件。

## srping boot 版本 ##
[https://github.com/734839030/seezoon-fast-framework](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c4b5e98e7277ede6e999e153a324da2a6f018779d3862e91d5823e076d30bf0f261f2387764e0379b2bf740a2e7f13f0) 

官方QQ群：514685454、574933593
## 体验地址 ##
[https://dev.seezoon.com](http://u.720life.cn/g/2be4f6ab31db048936d89dbbfbbb7c5f4846a1c3ef61ea501bf1a41458391f7b)    大家如果觉得做的还可以，麻烦给个star,万分感谢；

### 1M 带宽请大家忍耐下，为了给大家看到最全的功能这里提供超级管理员账号admin 123456 希望大家不要改密码，删默认菜单等，其余可以随意操作。 ###

> 本项目会持续完善更新，麻烦Watch、Star下项目，同时也是对项目最好的支持，谢谢。 

## 功能介绍 ##
* 前后端完全分离，采用node插件gulp 管理
* 前端数据双向绑定wayjs
* 统一异常处理，全局错误码
* RBAC权限管理，精细到菜单，按钮级别权限，支持父子权限
* 数据权限控制，不需要额外代码，框架自动支持，支持手动插拔
* 前后端数据双向校验
* 强大的代码生成，支持富文本，图片，文件,数据字典等复杂控件的生成，生成代码包含，完整的前端，后端，权限控制，校验等
* 文件上传支持本地和阿里云(本人只对阿里云有感觉，所以不考虑其他厂商的)两种模式，通过配置文件转换
* 集成elastic job 分片作业，流式作业，任务调度轨迹等
* 丰富的工具类，excel导入导出，图片裁剪，验证码，二维码，基于线程池的httpclient
* 微信公众号授权登录，js支付，扫码支付(两种模式)，微信小程序授权登录，小程序支付，小程序通过统一请求上送header实现上送cookie
* 易上手，在多个团队中使用，团队成员接受度较高，上手较快

## 常用框架 ##

#### 后端 ####

技术 | 名称 | 文档地址
----|----- |-----
Spring Framework |依赖管理 |[https://docs.spring.io/spring/docs/5.0.6.BUILD-SNAPSHOT/spring-framework-reference/](http://u.720life.cn/g/a8126de486174bbac1604ce886fda0d33163127cc15a75fd56a7a0b8d7ab0ad71fb69218dbd92cb1413244e8e7216668fe2f235c616fac0275aa7c38fd885bae1f5d9320e8f87a541fdece42f61675e3b0647148d6614b7ff68c9178a243aa69) 
Spring MVC | MVC|[https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html](http://u.720life.cn/g/a8126de486174bbac1604ce886fda0d33163127cc15a75fd56a7a0b8d7ab0ad79b92804bdeb6e4214e00d989879d8a5e37d2c85f38ce3b47c9c5705070149b4e7dd0135e7582e5bf88b0a16a86f28606) 
Mybatis | ORM |[http://www.mybatis.org/mybatis-3/zh/index.html](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a215e4d93221eb26b660bea25686b89be63142caf406b6e1c14d3ab51db921e10ca) 
Shiro | 权限、认证|[http://shiro.apache.org/documentation.html#apache-shiro-reference-and-api](http://u.720life.cn/g/c3294dc73186562102bd8975db9e807b24d66f87061b7c2e67506136ab7235779858008a88b5caf9ecacdbf5a6f6cf38a21666699822468224ffea0c8259344fa4422a4a1c177a09c0688eb9cf5d9772) 
Shiro Redis|shiro 缓存|[https://github.com/alexxiyang/shiro-redis](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463849f92d4054e4dd6135067215a8a3ae488c247f697c5783b832e529c948b040) 
Spring session（C端）|分布式会话|[https://docs.spring.io/spring-session/docs/2.0.3.BUILD-SNAPSHOT/reference/html5/](http://u.720life.cn/g/a8126de486174bbac1604ce886fda0d3c11ff9cd2c983439d13aa7ecb66a591776aa82cf444a853183bf0b5d431af48dec7fb7a129dc7fff17324cb6f4585b29ff82be51288fe620c948ac89d3974765) 
PageHelper|分页|[https://github.com/pagehelper/Mybatis-PageHelper](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e46d295ad2841af2558737b9b48e7f525f5d9e37bc321a699ae434b02ff50941) 
Druid |连接池|[https://github.com/alibaba/druid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a) 
AliOSS|云存储|[https://help.aliyun.com/document_detail/32008.html?spm=a2c4g.11186623.6.670.9vnD4m](http://u.720life.cn/g/9b510b4fa1fa50af2c9a0df8a6060239300f269356f82e053d4fa6061ecd054ad0f9a4363fef73ef1517132334d1eda3227833b71a40d181d3f3da71d1816fa29cf10ad3dbac2a79e17ded9653693b37084cefbf1f7c116ca3d8d3aabc111c7b) 
Zxing|二维码|[https://github.com/zxing/zxing](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bedc2941f2a7b389f9bf19f6bba663d9) 
POI|excel|[https://poi.apache.org/spreadsheet/quick-guide.html](http://u.720life.cn/g/543107c2d0ccb7d61d1473c6b2834b822397ea09c1dbf7a7da3af7897af8cfbd5f519f1d01cc18dfc3ebe1b828e2d41e0bfbc666be67cdbb34e90e78ff1428fe) 

#### 前端 ####
技术 | 名称 | 文档地址
----|----- |-----
Bootstrap |CSS/HTML框架|[https://v3.bootcss.com/](http://u.720life.cn/g/76ce37f2b9c55c77168e215bbd34e832a79a69310031c659a46a35e6bbfc8ea5) 
Jquery|JavaScript 库|[http://api.jquery.com/](http://u.720life.cn/g/b38f11420aac35913d92312b7cef1b0de3085bcbca6b0d79b46108d7adb80227) 
Bootstrap table|数据表格|[http://bootstrap-table.wenzhixin.net.cn/documentation/#table-options](http://u.720life.cn/g/d01548d39ecdbf3c595515bbd4e58d9dcec6c2397fb9ccbd4d5b65ebfc2a4fea7b57ebd1ffdb67f629f01e123765b3ebbbb725769ecd1474e0bc54fd530c05fcc24982b23ecf0b6f46f5f7a4d5577538) 
Bootstrap Table Editable|可编辑表格|http://vitalets.github.io/x-editable/docs.html#editable
Bootstrap Select|下拉组件|http://silviomoreto.github.io/bootstrap-select/
AdminLte |后台模板|[https://adminlte.io/themes/AdminLTE/index2.html](http://u.720life.cn/g/8c6d9ee339f2bed9b29ba7bbf38ffcb38bf2f05491778d0b0e361431b3697d9324d17a130b1fd2f3df43c4c57b9b7d04) 
Layer|弹出层|[http://www.layui.com/doc/modules/layer.html#type](http://u.720life.cn/g/330802d232849288787f1cd346adeee36e805390c9f791a422c908874ad30711d5e00710a754ba0ae7efbf922d4736cc) 
Bootstrap DateTimePicker |时间选择器|[http://www.bootcss.com/p/bootstrap-datetimepicker/](http://u.720life.cn/g/5dc63d04a35b84846e193be705862c77a076f23ea8c4288a3cb8acb4ba104581a908f3b6a543c3dfc12fed0c05ae98c4d973134a464d72209af3206ffde9b649) 
Wayjs |双向数据绑定|[https://github.com/gwendall/way.js/blob/master/docs/zh-CN.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304676a7e51f5c1539e87fcf7882db1aa3ecf5f7649cafa4485cead88ed3b3e0c3606d7acb2e69c503799118f0ec4e68daeb) 
Ztree|树组件|[http://www.treejs.cn/v3/api.php](http://u.720life.cn/g/498bbd2d294e9101825c13f60c5e8cb308ad7ad0459e664c9649528b5f28dadc) 
Bootstrapvalidator|表单验证|[https://github.com/nghuuphuoc/bootstrapvalidator](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046980318a0648b97a08a22d99e03ac63e656564c50b97da3c5a9711a896bdc27f8) 
JSON serialize|JSON serialize|[https://github.com/marioizquierdo/jquery.serializeJSON](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a5af31c1536268e1cddba2c6c879cd20a054c031f682cc016df927ae3171759d4ff0e85e6e8d3661618a5d23daa97ce4) 
Jquery-treegrid|树形表格|[jquery-treegrid](jquery-treegrid)
JQuery-File-Upload|异步上传插件|[https://github.com/blueimp/jQuery-File-Upload/wiki/Basic-plugin](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467c8c0e8e936246c8b435ca1a17ec418ded9af66a59783c10f4eb213a36b44bc8dfffbae69c41e426b22aef034a2fba48) 
Node js|工具|[https://nodejs.org/zh-cn/](http://u.720life.cn/g/6dd25ec2eceebbb6348ad519a7343cbc642d5ffb2f84e31a8b886edfdee1950e) 
Gulp |构建工具|[https://www.gulpjs.com.cn/](http://u.720life.cn/g/0483cc0684b2553a268792c39ee1527ce945aacccc71eccbb206738d2db284f9) 

## 本地运行 ##
1. 本工程为maven项目，导入eclipse
2. 建立数据库seezoon-framework，运行/src/main/resources/db/seezoon-framework.sql
3. 配置/src/main/resources/env/application.properties
4. 运行到tomcat 或者mvn jetty:run(代码改动时命令行任意键重新加载)
5. 运行前端需要先配置/src/main/webapp/static/gulpfile.js
中dev=后端接口地址上下文，gulp 是node插件，所以先安装node环境，
安装完成后命令行执行npm install 安装相关插件，然后再命令行到gulpfile.js 所在目录运行gulp 如图：
![gulp运行图](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/gulp-run.png?raw=true)
static/src 为前端源文件，static/dist 为编译后的静态资源，这边简单用了gulp的include 功能，后续会使用压缩合并等功能。

打开浏览器输入http://127.0.0.1:8888/admin/pages/index.html 自动拦截回到登录页。
![登录页](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/login-page.png?raw=true)


## 后续逐步开源如下功能（star 是开源的动力） ##

* spring cloud 版本脚手架；

## 部分项目截图 ##
#### 代码生成 ####
![代码生成](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/codegen.png?raw=true)
#### 首页 ####
![首页](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/index-page.png?raw=true)
#### 用户管理 ####
![用户管理](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/user-manager.png?raw=true)
#### 字典管理 ####
![地点管理](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/dict.png?raw=true)
#### 文件管理 ####
![文件管理](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/file.png?raw=true)
#### 角色管理 ####
![角色管理](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/role-manage.png?raw=true)
#### 菜单管理 ####
![菜单管理](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/menu1.png?raw=true)
![菜单管理](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/menu2.png?raw=true)
![图标选择](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/icon.png?raw=true)
#### 多主题 ####
![主题](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/muti-themes.png?raw=true)

> 更多功能参见演示网站。

下面为分布式版本线上案列，小型项目还是一体比较方便。
![产品编辑](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/eg1.png?raw=true)
![运费](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/eg2.png?raw=true)
![规格](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/eg3.png?raw=true)
![规格配置](https://github.com/734839030/seezoon-framework-all/blob/master/screenshots/eg4.png?raw=true)





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)