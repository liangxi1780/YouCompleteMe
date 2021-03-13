# mall

## 说明

> 基于SpringBoot+MyBatis-plus的电商系统，包括前台商城系统及后台管理系统。

> 如果该项目对您有帮助，您可以点右上角 "Star" 支持一下 谢谢！

> 或者您可以 "follow" 一下，该项目将持续更新，不断完善功能。

> 项目交流人QQ群：) 133070260 725021772 202220970]

> 如有问题或者好的建议可以在 Issues 中提。


## 前言

`mallplus`项目致力于打造一个完整的电商系统，采用现阶段流行技术实现。

## 项目介绍

`mallplus`项目是一套电商系统，包括前台商城系统及后台管理系统，小程序，h5，基于SpringBoot+MyBatis实现。
前台商城系统包含首页门户、商品推荐、商品搜索、商品展示、购物车、订单流程、会员中心、客户服务、帮助中心等模块。
后台管理系统包含商品管理、订单管理、会员管理、促销管理、运营管理、内容管理、统计报表、财务管理、权限管理、代码生成设置等模块。

### 项目演示

![输入图片说明](https://images.gitee.com/uploads/images/2020/0109/102351_cfd0b0c7_134431.png "屏幕截图.png")
### 关注公众号获取最新数据库脚本和后台管理的vue前端，以及uniapp生成的h5 小程序和app和演示地址



 _下载项目根路径下的 mall-web-admin(后台管理vue项目，需要启动mllplus-admin项目)
修改mallplus-admin中application-dev.properties 的数据库和redis配置_ 

[部署文档](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e53f75cd84529f81a00b22a2ffa9c22a399b83f2a9e5cac4b5803d6736a2dbb086d248d098f927492a42a7fde9a24acc59d675dd77a976e32ae151d72bd3e19e3e0d5d00a2ef8935520e4bdec9d95488f) 
> 后台管理系统

- 1. 商城总后台 http://51wangshi.com:8087/index
- 2.商户后台和用户端h5 小程序 和app（群文件下载） 
- 商户端演示 http://51wangshi.com:8090/
- uniapp h5演示 http://51wangshi.com:8082/
- app下载 https://share.weiyun.com/5KsC2YL
pc演示  [http://51wangshi.com:8088/#/](http://u.720life.cn/g/1505c170aad868a4d94879a1a5a0ab01532d9b8cf9bf5b220e377d61c6261d77)   


- uniapp下载 地址 https://gitee.com/mallcloud/uni4mall
- 小程序下载 地址 https://gitee.com/catshen/mall-applet


[TOC]


### 组织结构

``` lua
mall
├── mallplus-mbg -- MyBatisGenerator生成的数据库操作代码
├── mallplus-admin -- 后台商城管理系统接口
├── mall-search -- 基于Elasticsearch的商品搜索系统
├── mallplus-portal -- 前台商城系统接口
└── mall-demo -- 框架搭建时的测试代码
├── 前端项目`mallplus-admin-web` 
├── 小前端项目  uniapp 
```

**开源版本功能列表 ** 

 _下载项目根路径下的mall-web-admin(vue项目)
修改mallplus-admin中application-dev.properties 的数据库和redis配置_ 


### 关注公众号 获取最新的数据库脚本

 



 **_uniapp_** 

uni-app 是一个使用 Vue.js 开发跨平台应用的前端框架，开发者编写一套代码，可编译到iOS、Android、H5、小程序等多个平台。

 



## 目前h5项目已实现功能
1. 首页数据的展示
2. 分类页数据的展示
3. 购物车
4. 我的
5. 注册
6. 登录
7. 商品详情页
8. 商品搜索
##h5项目效果图


![](https://images.gitee.com/uploads/images/2019/0217/112713_5f032a4c_134431.png)

![](https://images.gitee.com/uploads/images/2019/0217/112713_f4cb24ab_134431.png)

![](https://images.gitee.com/uploads/images/2019/0217/112713_a17c828d_134431.png)

![](https://images.gitee.com/uploads/images/2019/0217/112713_a7afcc52_134431.png)

![](https://images.gitee.com/uploads/images/2019/0217/112713_2d82d3c8_134431.png)

![](https://images.gitee.com/uploads/images/2019/0217/112714_62baf63a_134431.png)

![](https://images.gitee.com/uploads/images/2019/0217/112715_c571472d_134431.png)


## 目前小程序项目已实现功能
1. 首页数据的展示
2. 分类页数据的展示
3. 购物车
4. 我的
5. 注册
6. 登录
7. 商品详情页
8. 商品搜索
9.下单
10.用户详情


## 目前pc项目已实现功能
1. 首页数据的展示
2. 分类页数据的展示
3. 购物车
4. 我的
5. 注册
6. 登录
7. 商品详情页
8. 商品搜索
9.下单
10.用户详情
### 技术选型

#### 后端技术

技术 | 说明 | 官网
----|----|----

Spring Boot | 容器+MVC框架 | [https://spring.io/projects/spring-boot](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d74791681f9785d83f6cd6c957366ad1debb29bb8c32cd47aff960e71f7893090) 
Spring Security | 认证和授权框架 | [https://spring.io/projects/spring-security](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d74791681f9785d83f6cd6c957366ad1d51f22cbfad230da539bef50203caf238) 
MyBatis | ORM框架  | [http://www.mybatis.org/mybatis-3/zh/index.html](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a215e4d93221eb26b660bea25686b89be63142caf406b6e1c14d3ab51db921e10ca) 
MyBatisGenerator | 数据层代码生成 | [http://www.mybatis.org/generator/index.html](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a21a07057a36d6ca5ea426a94333449b8ee4a9090aa94e48705a0a12124d68034da) 
PageHelper | MyBatis物理分页插件 | [http://git.oschina.net/free/Mybatis_PageHelper](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d0c5e449aa2c2e2afac3f4646cf34dfd65ceb51a277771277d2a7f535bcbaead3) 
Swagger-UI | 文档生产工具 | [https://github.com/swagger-api/swagger-ui](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ee873d8b7265bda98dbeb1b913855dc8cc8fe4f2d8a7cf6393aeda706a915000) 
Hibernator-Validator | 验证框架 | [http://hibernate.org/validator/](http://u.720life.cn/g/09d74cfb02196ca3ed0ec52b685384e1fd96db6373856c92099520b41f86fef5) 
Elasticsearch | 搜索引擎 | [https://github.com/elastic/elasticsearch](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e836c5dd85610d86e6f01486f462e2c0d9e4b426066af1ff2b4626bce8b1132) 
RabbitMq | 消息队列 | [https://www.rabbitmq.com/](http://u.720life.cn/g/0fa33e240a4f68a032ffc0865d7dcd1fb673b17d4773e9f52139fbece79cad2e) 
Redis | 分布式缓存 | [https://redis.io/](http://u.720life.cn/g/70336383bbe1092dca9fcec94f2fd10823c1cea91ac1108405bfbd56f5b819fc) 
MongoDb | NoSql数据库 | [https://www.mongodb.com/](http://u.720life.cn/g/5b6081b126093fbb42e8289314c4c63edef09cba29820afcfda6f238d141f89a) 
Docker | 应用容器引擎 | [https://www.docker.com/](http://u.720life.cn/g/d13d2b0ef4a5c92b4f4a6e9ed4270e65b90c4c1e1b506e1a501feef81ad769e9) 
Druid | 数据库连接池 | [https://github.com/alibaba/druid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a) 
OSS | 对象存储 | [https://github.com/aliyun/aliyun-oss-java-sdk](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463acc10ac40ebe392ae83d014e0e2b286fe9c84bf686fc8dede39c92bd0288ee5) 
JWT | JWT登录支持 | [https://github.com/jwtk/jjwt](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304637710c50c45b7e4b55624adcef685c65) 
LogStash | 日志收集 | [https://github.com/logstash/logstash-logback-encoder](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304669aa5c06d8130c325d1bfa13fdfd08726e2d71470b343aedcffc515849eb90f4b7fea92e7eced4cc00b62438ea6c9e83) 
Lombok | 简化对象封装工具 | [https://github.com/rzwitserloot/lombok](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304667e1b2f7ca2a7abf102cdf9e5fa5070a803dc1dd5f1c376fd8d7fb727fc2defd) 

#### 前端技术

技术 | 说明 | 官网
----|----|----
Vue | 前端框架 | [https://vuejs.org/](http://u.720life.cn/g/1c3db3fec6433a3fb191bb48af91f3bb055304712f0641658c814ca15fec0089) 
Vue-router | 路由框架 | [https://router.vuejs.org/](http://u.720life.cn/g/7bedfe02707a57b283aa65bf169b40685a2bcc51af184101de4b71f45db846fa) 
Vuex | 全局状态管理框架 | [https://vuex.vuejs.org/](http://u.720life.cn/g/acea3f53396a46112876052cae0a3648a88a7ed218d2be0ffa10fc982c11ad04) 
Element | 前端UI框架 | [https://element.eleme.io/](http://u.720life.cn/g/5fa51553afae358345e9f20b5a6e741569ec367dcef795a9cc086ceba9a9242d) 
Axios | 前端HTTP框架 | [https://github.com/axios/axios](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304638015ac6a54b1cadf0934b8a0d5637d0) 
v-charts | 基于Echarts的图表框架 | [https://v-charts.js.org/](http://u.720life.cn/g/04bb650c6b9547d2ac7f61bed3e715031e418e4efd3cee1a70120fe3eff14e14) 
Js-cookie | cookie管理工具 | [https://github.com/js-cookie/js-cookie](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304601a18a0a98543c227ccab0f66e611f0076dc75769652863fa8e48c713794768c) 
nprogress | 进度条控件 | [https://github.com/rstacruz/nprogress](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621051bfe8a14df709920d1b59773b4a1b34b830a15281032ae36824abb143cae) 

#### 架构图

##### 系统架构图

![系统架构图](document/resource/mall_system_arch.png)

##### 业务架构图

![系统架构图](document/resource/mall_business_arch.png)

#### 模块介绍

##### 后台管理系统 `mallplus-admin`

- 商品管理：[功能结构图-商品.jpg](document/resource/mind_product.jpg)
- 订单管理：[功能结构图-订单.jpg](document/resource/mind_order.jpg)
- 促销管理：[功能结构图-促销.jpg](document/resource/mind_sale.jpg)
- 内容管理：[功能结构图-内容.jpg](document/resource/mind_content.jpg)
- 用户管理：[功能结构图-用户.jpg](document/resource/mind_member.jpg)

##### 前台商城系统 `mallplus-portal`

[功能结构图-前台.jpg](document/resource/mind_portal.jpg)

#### 开发进度

![项目开发进度图](document/resource/mall_dev_flow.png)

## 环境搭建

### 开发工具

工具 | 说明 | 官网
----|----|----
IDEA | 开发IDE | https://www.jetbrains.com/idea/download
RedisDesktop | redis客户端连接工具 | https://redisdesktop.com/download
Robomongo | mongo客户端连接工具 | https://robomongo.org/download
SwitchHosts| 本地host管理 | https://oldj.github.io/SwitchHosts/
X-shell | Linux远程连接工具 | http://www.netsarang.com/download/software.html
Navicat | 数据库连接工具 | http://www.formysql.com/xiazai.html
PowerDesigner | 数据库设计工具 | http://powerdesigner.de/
Axure | 原型设计工具 | https://www.axure.com/
MindMaster | 思维导图设计工具 | http://www.edrawsoft.cn/mindmaster
ScreenToGif | gif录制工具 | https://www.screentogif.com/
ProcessOn | 流程图绘制工具 | https://www.processon.com/
PicPick | 屏幕取色工具 | https://picpick.app/zh/

### 开发环境

工具 | 版本号 | 下载
----|----|----
JDK | 1.8 | https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
Mysql | 5.7 | https://www.mysql.com/
Redis | 3.2 | https://redis.io/download
Elasticsearch | 2.4.6 | https://www.elastic.co/downloads
MongoDb | 3.2 | https://www.mongodb.com/download-center
RabbitMq | 5.25 | http://www.rabbitmq.com/download.html
nginx | 1.10 | http://nginx.org/en/download.html

### 搭建步骤

> 本地环境搭建

- 本地安装开发环境中的所有工具并启动，具体参考
- 关注公众号获取最新脚本安装最新的数据库mallplus.sql，解压 前端vue mallplsu-admin-web.zip
- 克隆源代码到本地，使用IDEA或Eclipse打开，并完成编译;
- 在mysql中新建mall数据库，导入document/sql下的mall.sql文件；
- 启动mallplus-admin项目：直接运行com.zscat.mallplus.MallAdminApplication的main方法即可，
  接口文档地址：http://localhost:8080/swagger-ui.html;
- 启动mall-search项目：直接运行com.zscat.mallplus.search.MallSearchApplication的main方法即可，
  接口文档地址：http://localhost:8081/swagger-ui.html;
- 启动mallplus-portal项目：直接运行com.zscat.mallplus.portal.MallPortalApplication的main方法即可，
  接口文档地址：http://localhost:8085/swagger-ui.html;



## 项目相关文档



## 参考资料

- [Spring实战（第4版）](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb94874c7d8266a5b6185efd63ee1a1b949e6) 
- [Spring Boot实战](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb9486c180ea8c71c04d580e1d69d81d2096c) 
- [Spring Cloud微服务实战](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb948464364d321cb1a480a334643657b2050) 
- [Spring Cloud与Docker微服务架构实战](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb948227c489e37cbab294b1b2b57fd19dcbe) 
- [Spring Data实战](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb9482882e36b00652a8cfe2abc0643c001e1) 
- [MyBatis从入门到精通](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb9481097fddbe4540bc1da07e49abedd3367) 
- [深入浅出MySQL](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb94820190c2bf74554faf15c565e39d313d9) 
- [循序渐进Linux（第2版）](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb94856daf4c2ba37ce612c3939305132d8e8) 
- [Elasticsearch 技术解析与实战](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb94809d10fa03d673745e9e7a9e54d7c3d6f) 
- [MongoDB实战(第二版)](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb948ad6954bcaee79a1503314ae7b738637b) 
- [Kubernetes权威指南](http://u.720life.cn/g/6dda20f34a6f0cac55219074bdc5cc40f06f6970df711edfb5c1d348414fb9481c9613b9a03b5eab64c1404e19eee7cc) 
- [mall商城](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e6d835ecf4b774474fd4ca3d48d644703b9b24f45c2acd63f582d17e459ce284) 
- [mybatis-plus](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e0890e1f3b6561591f7d31ac78339fdfa633def67832e2c7be44b99bc59270253) 


## 许可证

[MIT](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f2869282156bfb3e1a9d90aa1a71edd77288a149e2427dfceecf20f85bd1fa55ad056d1d1e6d5af418e070763c0a413b) 

Copyright (c) 2018-2019 zscatzheng


 **- 版权声明** 
- 本项目由北京zscat科技有限公司开发，禁止未经授权用于商业用途。个人学习可免费使用。如需商业授权，请加微信，获取域名授权。
- 本项目由北京zscat科技有限公司开发，禁止未经授权用于商业用途。个人学习可免费使用。如需商业授权，请加微信，获取域名授权。

### 我的微信号

![输入图片说明](https://images.gitee.com/uploads/images/2020/0109/175349_ce8614db_134431.jpeg "流逝.jpeg")

 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)