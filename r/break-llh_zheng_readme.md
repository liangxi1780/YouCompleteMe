# zheng
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](http://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/shuzheng/zheng/pulls)
[![GitHub forks](https://img.shields.io/github/forks/shuzheng/zheng.svg?style=social&label=Fork)](https://github.com/shuzheng/zheng)

**春节期间停止更新，祝大家新年快乐！**

交流QQ群：133107819 (群内含各种工具和文档下载)

文档：[https://shuzheng.gitbooks.io/zheng/content/](http://u.720life.cn/g/80e34e941437ca4106776ccc77b996c853e859fe818ac75fb7944d05cda2c23a538c929c8cdf9c4cf6291ff6307382c3  "文档")

## 前言

　　`zheng`项目于2016年10月4日创建于Github，之初目的是为自己建立一个“小工具”，后因github网速慢的原因同步到oschina上，迅速得到国内广大同仁关注、支持和肯定，所以我也愿意分享给大家使用。最近经常收到一些提问，由于缺乏文档，虽然耐心解答，但杯水车薪，特开始篡写文档并建立交流群等。

## 项目介绍

基于Spring+SpringMVC+Mybatis分布式敏捷开发系统架构：内容管理系统（门户、博客、论坛、问答等）、统一支付中心（微信、支付宝、在线网银等）、用户权限管理系统（RBAC细粒度用户权限、统一后台、单点登录、会话管理）、微信管理系统、第三方登录系统、会员系统、存储系统等

### 组织结构

``` lua
zheng
├── zheng-common -- SSM框架公共模块
├── zheng-admin -- 后台管理系统模板（基于bootstrap实现的响应式Material Design风格的通用后台管理系统模板）
├── zheng-upms -- 用户权限管理系统（网关）
|    ├── zheng-upms-dao -- MyBatisGenerator代码生成模块，无需开发
|    ├── zheng-upms-sso-client -- SSO客户端依赖包
|    ├── zheng-upms-rpc-api -- rpc接口包
|    ├── zheng-upms-rpc-service -- rpc服务提供者[端口:1112]
|    ├── zheng-upms-app1 -- SSO测试客户端1[端口:1113]
|    ├── zheng-upms-app2 -- SSO测试客户端2[端口:1114]
|    └── zheng-upms-server -- 系统及SSO服务端[端口:1111]
├── zheng-cms -- 内容管理系统
|    ├── zheng-cms-dao -- MyBatisGenerator代码生成模块，无需开发
|    ├── zheng-cms-rpc-api -- rpc接口包
|    ├── zheng-cms-rpc-service -- rpc服务提供者[端口:2225]
|    ├── zheng-cms-search -- 搜索服务[端口:2221]
|    ├── zheng-cms-admin -- 后台管理[端口:2222]
|    ├── zheng-cms-job -- 消息队列、任务调度等[端口:2223]
|    └── zheng-cms-web -- 网站前台[端口:2224]
├── zheng-pay -- 支付系统
|    ├── zheng-pay-dao -- MyBatisGenerator代码生成模块，无需开发
|    ├── zheng-pay-service -- 业务逻辑
|    ├── zheng-pay-sdk -- 开发工具包
|    ├── zheng-pay-admin -- 后台管理[端口:3331]
|    └── zheng-pay-web -- 演示示例[端口:3332]
├── zheng-ucenter -- 用户系统(包括第三方登录)
|    ├── zheng-ucenter-dao -- MyBatisGenerator代码生成模块，无需开发
|    ├── zheng-ucenter-service -- 业务逻辑
|    └── zheng-ucenter-home -- 网站前台[端口:4441]
|── zheng-wechat-mp -- 微信公众号管理系统
|    ├── zheng-wechat-mp-dao -- MyBatisGenerator代码生成模块，无需开发
|    ├── zheng-wechat-mp-service -- 业务逻辑
|    └── zheng-wechat-mp-admin -- 后台管理[端口:5551]
├── zheng-api -- 接口系统
|    ├── zheng-api-sdk -- 开发工具包
|    ├── zheng-api-doc -- 接口文档项目
|    └── zheng-api-example -- 演示示例[端口:6661]
└── zheng-oss -- 对象存储系统
     ├── zheng-oss-sdk -- 开发工具包
     └── zheng-oss-web -- 管理界面[端口:7771]
```

### 技术选型

#### 后端技术:
* Spring Framework
* SpringMVC: MVC框架
* Spring secutity|Shiro: 安全框架
* Spring session: 分布式Session管理
* MyBatis: ORM框架
* MyBatis Generator: 代码生成
* Druid: 数据库连接池
* Jsp|Velocity|Thymeleaf: 模板引擎
* ZooKeeper: 协调服务
* Dubbo: 分布式服务框架
* TBSchedule|elastic-job: 分布式调度框架
* Redis: 分布式缓存数据库
* Quartz: 作业调度框架
* Ehcache: 缓存框架
* ActiveMQ: 消息队列
* Solr|Elasticsearch: 分布式全文搜索引擎
* FastDFS: 分布式文件系统
* Log4J: 日志管理
* Swagger2: 接口文档
* sequence: 分布式高效ID生产 [http://git.oschina.net/yu120/sequence](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d668807e284370ed5548c26ba6d643d5688aac63b66842b90bb9aae2d46e507fc  "sequence")
* AliOSS|Qiniu: 云存储
* Protobuf|json: 数据传输 
* Jenkins: 持续集成工具
* Maven|Gradle: 项目构建管理

#### 前端技术:
* jQuery
* Bootstrap
* jQuery EasyUI
* AngularJs
* zhengAdmin [基于bootstrap实现的响应式Material Design风格的通用后台管理系统](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467faba9083dbd846c77818d3de6c1e6688e2b9955a1ca3175702ae33817317262  "zhengAdmin")
* autoMail [邮箱地址自动补全插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046872152e207ef734a7d4d87bb26aa10c72b44fd6f9db5a42c2efc46bc366a5dca  "autoMail")
* zheng.jprogress.js [一款模仿youtube加载进度条插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467faba9083dbd846c77818d3de6c1e6680f7c41cc1c94ff0531a3f71333be6766  "zheng.jprogress.js")
* zheng.jtotop.js [返回顶部插件(可以任意速度滑动到指定任意位置)](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467faba9083dbd846c77818d3de6c1e668e12dbe692c839e0f4b3440d94ac044bb  "zheng.jtotop.js")

#### 模块依赖
![模块依赖](project-bootstrap/project.png)

#### 模块介绍

> zheng-common

Spring+SpringMVC+Mybatis框架集成公共模块，包括公共配置、MybatisGenerator扩展插件、通用BaseService、工具类等。

> zheng-admin

基于bootstrap实现的响应式Material Design风格的通用后台管理系统，`zheng`项目所有系统都是使用该模块界面作为前端展示。

> zheng-upms

本系统是基于RBAC授权和基于用户授权的细粒度权限控制通用平台，并提供单点登录、会话管理和日志管理。接入的系统可自由定义组织、角色、权限、资源等。

**系统功能概述：**

- 系统组织管理：系统和组织增加、删除、修改、查询功能。
- 用户角色管理：用户和角色增加、删除、修改、查询功能。
- 资源权限管理：资源和权限增加、删除、修改、查询功能。
- 权限分配管理：提供给角色和用户的权限增加、删除、修改、查询功能。
- 单点登录(SSO)：提供统一用户单点登录认证、用户鉴权功能。
- 用户会话管理：提供分布式用户会话管理
- 操作日志管理：提供记录用户登录、操作等日志。

> zheng-oss

文件存储系统，提供三种方案：

- **阿里云** 对象存储OSS
- **腾讯云** 对象存储COS
- **七牛云** 对象存储

> zheng-api

接口系统，包括开发加密接口、接口文档等对外开放服务。

> zheng-cms

内容管理系统：支持多标签、多类目、强大评论的内容管理，有基本单页展示，菜单管理，系统设置等功能。

> zheng-pay

一站式支付解决方案，统一下单接口，支持支付宝、微信、网银等多种支付方式。不涉及业务的纯粹的支付平台。

**功能介绍：**

- 统一下单（统一下单接口、统一扫码）、订单管理、数据分析、财务报表、商户管理、渠道管理、对账系统、系统监控

> zheng-ucenter

通用用户管理系统， 实现最常用的用户注册、登录、资料管理、个人中心、第三方登录等基本需求，支持扩展二次开发。

> zheng-wechat-mp

微信公众号管理平台，除实现官网后台自动回复、菜单管理、素材管理、用户管理、消息群发等基础功能外，还有二维码推广、营销活动、微网站、会员卡、优惠券等

## 环境搭建

#### 开发工具:
* MySql: 数据库
* jetty: 开发服务器
* Tomcat: 应用服务器
* SVN|Git: 版本管理
* Nginx: 反向代理服务器
* Varnish: HTTP加速器
* IntelliJ IDEA: 开发IDE
* PowerDesigner: 建模工具
* Navicat for MySQL: 数据库客户端

#### 开发环境：

- Jdk7
- Mysql5.5
- Redis
- Zookeeper
- ActiveMQ
- Dubbo-admin

### 工具安装

[环境搭建和系统部署文档(作者：小兵)](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d47239a8476d8e96a4930b936ff5feb23ef2461b58c40cbbcade47e760d8b19778b6f26b1fe2774bf294cf954edfd8455  "环境搭建和系统部署文档(作者：小兵)")

### 资源下载

* JDK7 [http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html#jdk-7u80-oth-JPR](http://u.720life.cn/g/0832d3c13dcf440b8c2ddd37014597194dfce0f4546bd12c9ba469d981d9d729007ebfc8068b2baf5cdf0064d40d499934723df973302be9e8c27d1f120dec7b85d43baa411ec8b965a250d5c3c1a472012739f428572134111b101dee0bb73461d28a961fe30fd0ed05f3227b8411137331ae2a48279f1327915e8d5ba5b90c  "JDK7")
* Maven [http://maven.apache.org/download.cgi](http://u.720life.cn/g/bc840264f6cc23df0a8935b6f2922fec94ff6a8561d0b6bc316737cabaa3024658023840c15f3e7f28cf9ac3c1a389dd  "Maven")
* Redis [https://redis.io/download](http://u.720life.cn/g/70336383bbe1092dca9fcec94f2fd1080fb6792497a244eb2803ca3875f6a403  "Redis")
* ActiveMQ [http://activemq.apache.org/download-archives.html](http://u.720life.cn/g/1ef10f1d63639e4eea43ad318c7c3e29aed5a3f8732d353f4cb00d1527d2d9d744b76c3ce781775d2298fb3c59b42d1cc18ce86ea8098829c93376960182c1ef  "ActiveMQ")
* ZooKeeper [http://www.apache.org/dyn/closer.cgi/zookeeper/](http://u.720life.cn/g/c0fe1da5278ca9f6360e901f74721f8472014a29255ca2020681edf6817010be3d654a9189b565f20a6e183ac7296787  "ZooKeeper")
* Dubbo [http://dubbo.io/Download-zh.htm](http://u.720life.cn/g/ad27fc5875c834b4568aeb04084d2bc018cae7cae1a1e67fee62968346f5790e  "Dubbo")
* Elastic Stack [https://www.elastic.co/downloads](http://u.720life.cn/g/de3742c0ac7bbef6b8feb3a0318f07719aab0e585c5d880a6a8d7f20f20bbd9f  "Elastic Stack")
* Jenkins [http://updates.jenkins-ci.org/download/war/](http://u.720life.cn/g/c896990f5bd3c33c5a533ade338e7f53e07c1eb407401bbf07f8ddf4817f9c59b99ed3f6ace5ea93e698e651fff1f96c  "Jenkins")
* dubbo-admin-2.5.3 [http://download.csdn.net/detail/shuzheng5201314/9733652](http://u.720life.cn/g/9b4a1380e2aa619eac4d900347bdc8b988b3227d0eaf6623ada963ebde1c3087f877ab51bf6b6cfa59178b20cdecaa0445e424d477c34713559a35402531614c  "dubbo-admin-2.5.3")
* dubbo-admin-2.5.4-SNAPSHOT-jdk8 [http://download.csdn.net/detail/shuzheng5201314/9733657](http://u.720life.cn/g/9b4a1380e2aa619eac4d900347bdc8b988b3227d0eaf6623ada963ebde1c3087f877ab51bf6b6cfa59178b20cdecaa0407d7598ca7adbedc3d03a76d0c5c28a5  "dubbo-admin-2.5.4-SNAPSHOT-jdk8")

## 开发指南:

* 1、本机安装Jdk7、Mysql、Redis、Zookeeper、ActiveMQ并启动相关服务，使用默认配置默认端口，下面有资源下载链接（安装流程略）

* 2、克隆源代码到本地并打开，**推荐使用IntelliJ IDEA**，本地编译并安装到本地maven仓

### 修改本地Host
* 127.0.0.1	upms.zhangshuzheng.cn
* 127.0.0.1	cms.zhangshuzheng.cn
* 127.0.0.1	pay.zhangshuzheng.cn
* 127.0.0.1	ucenter.zhangshuzheng.cn
* 127.0.0.1	wechat.zhangshuzheng.cn
* 127.0.0.1	api.zhangshuzheng.cn
* 127.0.0.1	oss.zhangshuzheng.cn

### 编译流程

zheng-admin、zheng-common => zheng-oss、zheng-api => zheng-upms => 其他

### 启动顺序

- 新建`zheng`数据库，导入`zheng.sql`、`upms_system.sql`、`upms_user.sql`

- 启动 zheng-upms-rpc-service => zheng-upms-server => zheng-`xxx`-rpc-service => zheng-`xxx`-`webapp`

- 访问 [统一后台地址](http://u.720life.cn/g/df3cbdb42fe1f1ef1ec67f4fb72ed3dbceba944aeb34e8dd008653f7ee69cb5e0d8ab8eb4605aca09932ebc17792970a  "统一后台地址")，默认帐号密码：`admin/123456`

- 登录成功后，可在右上角切换已注册系统访问

### 开发演示

- 创建数据表（建议使用PowerDesigner）

- 直接运行对应项目dao模块中的generator.main()，可自动生成单表的CRUD功能和对应的model、example、mapper、service代码

    - 生成的model和example均已实现Serializable接口，支持分布式
    - 生成的mapper.xml的selectByExample方法自动包含分页参数offset和limit
    - 已包含抽象类BaseServiceImpl，只需要继承抽象类并传入泛型参数，即可默认实现mapper接口所有方法，特殊需求直接扩展即可

- 启动流程：优先rcp-service服务提供者，再启动其他webapp

- 扩展流程：可扩展和拆分rpc-api和rpc-service模块，可按微服务拆分或场景拆分

## 演示地址

演示地址： [http://www.zhangshuzheng.cn/zhengAdmin](http://u.720life.cn/g/9de410eefb2e8800a0633adea37e119d2eb2a078574fe438fb8395aed1defdedb01bbe610ff61b9e58351d273caa6d6f  "演示地址")

### 预览图
![login](zheng-admin/src/images/zheng-upms-login.png)
![crud](zheng-admin/src/images/zheng-upms-crud.png)
![swagger](project-bootstrap/api.png)

### 数据模型
![数据库模型](https://github.com/shuzheng/zheng/raw/master/project-datamodel/zheng.png)

### 拓扑图
![拓扑图](https://github.com/shuzheng/zheng/raw/master/project-bootstrap/distributedSystem.png)

## 附件

### 优秀文章和博客

- [创业互联网公司如何搭建自己的技术框架](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271b15a9f3143a820af99b242bac1bddb954  "创业互联网公司如何搭建自己的技术框架")

- [单点登录原理与简单实现](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271bb354c5efa3ac8ba29954917c7df65aa6  "单点登录原理与简单实现")

- [支付系统架构](http://u.720life.cn/g/00b5b5b7681eead9a3c1f8192f370e997e477d7fb388ff4ce05a632965cf913d115b93e50a71d6a6677797a96a1b6be4cf1cd0a3793030cb435ad6f5d1e5a30e  "支付系统架构")

- [ITeye论坛关于权限控制的讨论](http://u.720life.cn/g/79075b0b214ce70be040eb4c2085a0293f326ef3556a41b398ecd08515aa182e2a4ed9c0a2ce57dacf3198757e3da7f5  "ITeye论坛关于权限控制的讨论")

- [RBAC新解：基于资源的权限管理(Resource-Based Access Control)](http://u.720life.cn/g/e3cb95d362ac306ae496c1ccddb5809d72fe18e8899e8e99b83d1c0660b228f8fa57f4672728696fb9dc5138159f51e9  "RBAC新解：基于资源的权限管理(Resource-Based Access Control)")

- [Spring整合JMS](http://u.720life.cn/g/cb08bef269584a7a80de468db7afa45642d3fde81548ececa5b67575169a754e7c8741219ac5aca2a93732bc43c52aa9  "Spring整合JMS")

- [Redis中文网](http://u.720life.cn/g/5bbeb658b3b29111025f8f6d1b1ac7e7e21d6b0d95f9c13dae9935dd5c101b9d  "Redis中文网")

- [读懂Redis并配置主从集群及高可用部署](http://u.720life.cn/g/ecc7d42b8e4205e5d387aa616e7cff787790df498634a7265a9de812e3c83a31e93e0b90cc47fa55b144a3c2218eaa25fe81aec28a7a4904cadff3cd16e00bff553476f3b697d9822735b61e7a6f056882da3ac3740c04856c772336c012f060f16442387226b5c86f81dccab53b134e36914f260ebe78459ba10cdbd1f727eeb63c6ee6b697ec4713f1e1280a502c364dcb55d79d951951c0b047c77df059739236165207208063c8bd6ea225307f355f4ad0c6b6968a9d2d589fc954b632d276f238e5816c8ce301711ee57cdb423f56a7e910b276b3201bf667488b8153b55441bc4fa62ee8536a5309692b777a82f285de6a590e4dd0df09ef4f8f9e8b0b  "读懂Redis并配置主从集群及高可用部署")

- [ELK(ElasticSearch, Logstash, Kibana)搭建实时日志分析平台](http://u.720life.cn/g/fd6eca4b0fbbac408c109c69a910940dcf3c092220662b4ba88b8a70684ddbca27fc729ec92e2a633d407c6142a64e46ddf76105329fe4c637ec337cc4e8c6dd  "ELK(ElasticSearch, Logstash, Kibana)搭建实时日志分析平台")

- [Nginx基本功能极速入门](http://u.720life.cn/g/5ffdf2a24e1b2bbd5675a4ce14af25eb6286f7650c3d9402857cef26d27f0d89a7444804986fbed1f33543bfc9204d0b  "Nginx基本功能极速入门")

- [mybatis-genarator 自定义插件](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb17318cd075ba15e084639bc845a84cace7a83a89472f1b9ac7dfd43ca0f7d18c3ff  "mybatis-genarator 自定义插件")

- [Elasticsearch权威指南（中文版）](http://u.720life.cn/g/38a6caf4b41304d8700b935c585d5fe5c5a18657f3c23822170efbff94ecd6378a5184bd411353cc6ea5cac932491c6bf1f48d8eaa61bc13c6d31b1e3807019f  "Elasticsearch权威指南（中文版）")

- [springMVC对简单对象、Set、List、Map的数据绑定和常见问题.](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4e3a725e5cc303574b6644d569864ebacae3bbbc6d47a55533be3bdb62ede042fe677d9514d5d6e2b9e9afee1c7cda1ed  "springMVC对简单对象、Set、List、Map的数据绑定和常见问题.")

- [做个男人，做个成熟的男人，做个有城府的男人](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271b8916b1d051befffbb0e09d31de280b72  "做个男人，做个成熟的男人，做个有城府的男人")

- [中国所有神仙列表](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271be3d72ab6df721a41d21c08b942c9a30f  "中国所有神仙列表")


### 常用在线小工具

- [在线Cron表达式生成器](http://u.720life.cn/g/41a88c49241c9a1f605f913332fbeca495e13ea8491440f895022f4f9df8c3e3  "在线Cron表达式生成器")

- [在线工具 - 程序员的工具箱](http://u.720life.cn/g/41843dbe0fafe94d482221c4b6428051  "在线工具 - 程序员的工具箱")

## 许可证

[MIT](http://u.720life.cn/g/ba059582536a397f7c573b87c8bea647045b0ef049248233b6f76e909e70200fe7048b25e29c8bab79aeff32ea74556a  "MIT")


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)