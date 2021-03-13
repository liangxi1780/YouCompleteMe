# zheng
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/shuzheng/zheng/pulls)
[![GitHub stars](https://img.shields.io/github/stars/shuzheng/zheng.svg?style=social&label=Stars)](https://github.com/shuzheng/zheng)
[![GitHub forks](https://img.shields.io/github/forks/shuzheng/zheng.svg?style=social&label=Fork)](https://github.com/shuzheng/zheng)

交流QQ群：133107819🈵、284280411🈵、305155242🈵、528049386🈵、157869467🈵、570766789🈵、601147566🈵、309985359🈵、336380857🈵、522723488🈵、556447629🈵、654558397🈵、392564561🈵、494594000🈵、494070275(群内含各种工具、文档、视频教程下载)

## 前言

　　`zheng`项目创建于2016年10月4日，正在慢慢成长中，目的不仅仅是一个开发架构，而是努力打造一套从 **前端模板** - **基础框架** - **分布式架构** - **开源项目** - **持续集成** - **自动化部署** - **系统监测** - **无缝升级** 的全方位J2EE企业级开发解决方案。

## 项目介绍

　　基于Spring+SpringMVC+Mybatis分布式敏捷开发系统架构，提供整套公共微服务服务模块：内容管理、支付中心、用户管理（包括第三方）、微信平台、存储系统、配置中心、日志分析、任务和通知等，支持服务治理、监控和追踪，努力为中小型企业打造全方位J2EE企业级开发解决方案。

### 组织结构

``` lua
zheng
├── zheng-common -- SSM框架公共模块
├── zheng-admin -- 后台管理模板
├── zheng-ui -- 前台thymeleaf模板[端口:1000]
├── zheng-config -- 配置中心[端口:1001]
├── zheng-upms -- 用户权限管理系统
|    ├── zheng-upms-common -- upms系统公共模块
|    ├── zheng-upms-dao -- 代码生成模块，无需开发
|    ├── zheng-upms-client -- 集成upms依赖包，提供单点认证、授权、统一会话管理
|    ├── zheng-upms-rpc-api -- rpc接口包
|    ├── zheng-upms-rpc-service -- rpc服务提供者
|    └── zheng-upms-server -- 用户权限系统及SSO服务端[端口:1111]
├── zheng-cms -- 内容管理系统
|    ├── zheng-cms-common -- cms系统公共模块
|    ├── zheng-cms-dao -- 代码生成模块，无需开发
|    ├── zheng-cms-rpc-api -- rpc接口包
|    ├── zheng-cms-rpc-service -- rpc服务提供者
|    ├── zheng-cms-search -- 搜索服务[端口:2221]
|    ├── zheng-cms-admin -- 后台管理[端口:2222]
|    ├── zheng-cms-job -- 消息队列、任务调度等[端口:2223]
|    └── zheng-cms-web -- 网站前台[端口:2224]
├── zheng-pay -- 支付系统
|    ├── zheng-pay-common -- pay系统公共模块
|    ├── zheng-pay-dao -- 代码生成模块，无需开发
|    ├── zheng-pay-rpc-api -- rpc接口包
|    ├── zheng-pay-rpc-service -- rpc服务提供者
|    ├── zheng-pay-sdk -- 开发工具包
|    ├── zheng-pay-admin -- 后台管理[端口:3331]
|    └── zheng-pay-web -- 演示示例[端口:3332]
├── zheng-ucenter -- 用户系统(包括第三方登录)
|    ├── zheng-ucenter-common -- ucenter系统公共模块
|    ├── zheng-ucenter-dao -- 代码生成模块，无需开发
|    ├── zheng-ucenter-rpc-api -- rpc接口包
|    ├── zheng-ucenter-rpc-service -- rpc服务提供者
|    └── zheng-ucenter-web -- 网站前台[端口:4441]
├── zheng-wechat -- 微信系统
|    ├── zheng-wechat-mp -- 微信公众号管理系统
|    |    ├── zheng-wechat-mp-dao -- 代码生成模块，无需开发
|    |    ├── zheng-wechat-mp-service -- 业务逻辑
|    |    └── zheng-wechat-mp-admin -- 后台管理[端口:5551]
|    └── zheng-ucenter-app -- 微信小程序后台
├── zheng-api -- API接口总线系统
|    ├── zheng-api-common -- api系统公共模块
|    ├── zheng-api-rpc-api -- rpc接口包
|    ├── zheng-api-rpc-service -- rpc服务提供者
|    └── zheng-api-server -- api系统服务端[端口:6666]
├── zheng-oss -- 对象存储系统
|    ├── zheng-oss-sdk -- 开发工具包
|    ├── zheng-oss-web -- 前台接口[端口:7771]
|    └── zheng-oss-admin -- 后台管理[端口:7772]
├── zheng-shop -- 电子商务系统
├── zheng-im -- 即时通讯系统
├── zheng-oa -- 办公自动化系统
├── zheng-eoms -- 运维系统
└── zheng-demo -- 示例模块(包含一些示例代码等)
     ├── zheng-demo-rpc-api -- rpc接口包
     ├── zheng-demo-rpc-service -- rpc服务提供者
     └── zheng-demo-web -- 演示示例[端口:8888]
```

### 技术选型

#### 后端技术:
技术 | 名称 | 官网
----|------|----
Spring Framework | 容器  | [http://projects.spring.io/spring-framework/](http://u.720life.cn/g/e0845233bf5cae93142c4c8e1c8864d4e670a90f87afc2ad04fb4c1d1899c07fdd2c7fa40574a04f80c374ab3968c758) 
SpringMVC | MVC框架  | [http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/#mvc](http://u.720life.cn/g/a6ba8c6b0e93c9f31bd435772627160d78653d6a55dc6315bda807ef09f29a08138b35c7e95760a878e8a0494b6946c305ffdacf75171f9fb043ea8675f3d72d7a4c2af751af247d69b57160e21c66cf4b1624d4570ec58555958c387c809a0d) 
Apache Shiro | 安全框架  | [http://shiro.apache.org/](http://u.720life.cn/g/c3294dc73186562102bd8975db9e807be68145a3e524f14e47e43b209703de8b) 
Spring session | 分布式Session管理  | [http://projects.spring.io/spring-session/](http://u.720life.cn/g/e0845233bf5cae93142c4c8e1c8864d4e670a90f87afc2ad04fb4c1d1899c07f5edcaa1e51c3d9bd7ea9b89a185892b3) 
MyBatis | ORM框架  | [http://www.mybatis.org/mybatis-3/zh/index.html](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a215e4d93221eb26b660bea25686b89be63142caf406b6e1c14d3ab51db921e10ca) 
MyBatis Generator | 代码生成  | [http://www.mybatis.org/generator/index.html](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a21a07057a36d6ca5ea426a94333449b8ee4a9090aa94e48705a0a12124d68034da) 
PageHelper | MyBatis物理分页插件  | [http://git.oschina.net/free/Mybatis_PageHelper](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d0c5e449aa2c2e2afac3f4646cf34dfd65ceb51a277771277d2a7f535bcbaead3) 
Druid | 数据库连接池  | [https://github.com/alibaba/druid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a) 
FluentValidator | 校验框架  | [https://github.com/neoremind/fluent-validator](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cb136fe0f6caf33b3edd2634b789bfd6b74e648fe57412134be6246087ce68f7) 
Thymeleaf | 模板引擎  | [http://www.thymeleaf.org/](http://u.720life.cn/g/93cb058e2406031f6144e4282378397987e151bf87215720b501542d1dbfbf04) 
Velocity | 模板引擎  | [http://velocity.apache.org/](http://u.720life.cn/g/7b1a2cc30709fab1f7d3403a12a6962269bc30564c30ad560dde6517ffaca179) 
ZooKeeper | 分布式协调服务  | [http://zookeeper.apache.org/](http://u.720life.cn/g/9036bb30203a9192b0bca1ff23f6480f71d7ad868c7c8d1a9b3c2b9a91b88dd3) 
Dubbo | 分布式服务框架  | [http://dubbo.io/](http://u.720life.cn/g/ad27fc5875c834b4568aeb04084d2bc0) 
TBSchedule & elastic-job | 分布式调度框架  | [https://github.com/dangdangdotcom/elastic-job](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ea516248917ac7a35ff5944f421f82fd6ce6cd6a83852420546a6b15a664441f) 
Redis | 分布式缓存数据库  | [https://redis.io/](http://u.720life.cn/g/70336383bbe1092dca9fcec94f2fd10823c1cea91ac1108405bfbd56f5b819fc) 
Solr & Elasticsearch | 分布式全文搜索引擎  | [http://lucene.apache.org/solr/](http://u.720life.cn/g/bbdca0dda33b41f95a6560dc4b6c99278b738875900a441d8ab09c03fe3561eb)  [https://www.elastic.co/](http://u.720life.cn/g/de3742c0ac7bbef6b8feb3a0318f077134e44859dfd208ba6912eae0acd6f2f0) 
Quartz | 作业调度框架  | [http://www.quartz-scheduler.org/](http://u.720life.cn/g/beb95a72271892e3173f0dad802e5ddf75666c78a77f9b92d69407e846140c43) 
Ehcache | 进程内缓存框架  | [http://www.ehcache.org/](http://u.720life.cn/g/dee26afa1b97181b9679d266f0740e531dbc93d0549dbfc9728e2239aa4f49e7) 
ActiveMQ | 消息队列  | [http://activemq.apache.org/](http://u.720life.cn/g/1ef10f1d63639e4eea43ad318c7c3e29e5e0b9b20040db508812cdd15d1a010d) 
JStorm | 实时流式计算框架  | [http://jstorm.io/](http://u.720life.cn/g/a5518ce08fd8f78d45194a441c0641802fc303ad190b7c4c74e707e55c268788) 
FastDFS | 分布式文件系统  | [https://github.com/happyfish100/fastdfs](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d00820f799868fd9afbf99f9fa8c150e2b3f8d8c0a394513ed08b836db28783d) 
Log4J | 日志组件  | [http://logging.apache.org/log4j/1.2/](http://u.720life.cn/g/d24248ea9b8085edf05b454a12c4113a4a243943067bd43da78e8d962bb8001b5bcdd716e023965ecc87eca2217c0aa6) 
Swagger2 | 接口测试框架  | [http://swagger.io/](http://u.720life.cn/g/11c40bf970887098486746d0b29456d7097ab4deff64fa816437c6fd1578a071) 
sequence | 分布式高效ID生产  | [http://git.oschina.net/yu120/sequence](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d668807e284370ed5548c26ba6d643d5688aac63b66842b90bb9aae2d46e507fc) 
AliOSS & Qiniu & QcloudCOS | 云存储  | [https://www.aliyun.com/product/oss/](http://u.720life.cn/g/cc176fdce68265104b8a4a80987ffe393f0578af68b131e06d5e5b3778fa057e74405b8eb94497831d7299f41abbf1e5)  [http://www.qiniu.com/](http://u.720life.cn/g/388937451a621da2ed3388374d67c63d3c4b54fd82591d905e36b23a3040cabb)  [https://www.qcloud.com/product/cos](http://u.720life.cn/g/297a506394a7e684b1feeac9fd4f722cdffc248e93f7c752003f542e9278ff90b737c2a36b68e93f7421e3a544645da5) 
Protobuf & json | 数据序列化  | [https://github.com/google/protobuf](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a5172d16931bc9434a400dbb07fdbe46b6508bd55daa2a7b3fac734310498357) 
Jenkins | 持续集成工具  | [https://jenkins.io/index.html](http://u.720life.cn/g/c49fa834be03879707125af0699343e3e3290abf56afe7e529f80f52d59a24f9) 
Maven | 项目构建管理  | [http://maven.apache.org/](http://u.720life.cn/g/bc840264f6cc23df0a8935b6f2922fec747e8988e9d6774b642901b9662b323f) 

#### 前端技术:
技术 | 名称 | 官网
----|------|----
jQuery | 函式库  | [http://jquery.com/](http://u.720life.cn/g/bf5ee7c5d8e747312b9dff6cfd25472308f0e1fd43291f641e8858d899a5b79d) 
Bootstrap | 前端框架  | [http://getbootstrap.com/](http://u.720life.cn/g/e23be2821e5181a1a46a005bc6e93d9dc1c8dad0ef41593aa593e12a30fc455b) 
Bootstrap-table | Bootstrap数据表格  | [http://bootstrap-table.wenzhixin.net.cn/](http://u.720life.cn/g/d01548d39ecdbf3c595515bbd4e58d9dcec6c2397fb9ccbd4d5b65ebfc2a4feac6937f8e53f076a847aa3d14ce294d91) 
Font-awesome | 字体图标  | [http://fontawesome.io/](http://u.720life.cn/g/214bbe9ff6ad53005f2a6de3696f36fffcfbfc1374f8d2fb41b782949ee44927) 
material-design-iconic-font | 字体图标  | [https://github.com/zavoloklom/material-design-iconic-font](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ca04b45eb1c2fd2a0fd1e5a025d853504a1eaefd205be4cc45ba40fe711f743e5509bffea494c444a73c774e3f25815f) 
Waves | 点击效果插件  | [https://github.com/fians/Waves](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ad61d3cc51ad97e12fd0399f7e351ed2) 
zTree | 树插件  | [http://www.treejs.cn/v3/](http://u.720life.cn/g/498bbd2d294e9101825c13f60c5e8cb3f681e96d109cd0ce72a74684c0f7e9ca) 
Select2 | 选择框插件  | [https://github.com/select2/select2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462d1700869653b8d6e14aa86de14db12546ad040a5927aa3c61ca7378024a2b42) 
jquery-confirm | 弹出窗口插件  | [https://github.com/craftpip/jquery-confirm](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c9d2e45490ecc11db468fa2c5165adec48125e8b0e403f1cfdbfdb8b93e64da3) 
jQuery EasyUI | 基于jQuery的UI插件集合体  | [http://www.jeasyui.com](http://u.720life.cn/g/0c519d05a3267c20024930c6036ce9eee06e5357a41deee72b3d46cd5f18e4ad) 
React | 界面构建框架  | [https://github.com/facebook/react](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046405e3357754798ba3fdb28fb956ae71f3f95f97337fa9f7933c903f0b8a28f5b) 
Editor.md | Markdown编辑器  | [https://github.com/pandao/editor.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c2531d0d62bc04ab421ebd243aa86e7ae67e52b2770e61c62b007b56ee3731ca) 
zhengAdmin | 后台管理系统模板  | [https://github.com/shuzheng/zhengAdmin](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467faba9083dbd846c77818d3de6c1e6688e2b9955a1ca3175702ae33817317262) 
autoMail | 邮箱地址自动补全插件  | [https://github.com/shuzheng/autoMail](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046872152e207ef734a7d4d87bb26aa10c72b44fd6f9db5a42c2efc46bc366a5dca) 
zheng.jprogress.js | 加载进度条插件  | [https://github.com/shuzheng/zheng.jprogress.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467faba9083dbd846c77818d3de6c1e6680f7c41cc1c94ff0531a3f71333be6766) 
zheng.jtotop.js | 返回顶部插件  | [https://github.com/shuzheng/zheng.jtotop.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467faba9083dbd846c77818d3de6c1e668e12dbe692c839e0f4b3440d94ac044bb) 

#### 架构图

![架构图](project-bootstrap/architect.png)

#### 模块依赖

![模块依赖](project-bootstrap/project.png)

#### 模块介绍

> zheng-common

Spring+SpringMVC+Mybatis框架集成公共模块，包括公共配置、MybatisGenerator扩展插件、通用BaseService、工具类等。

> zheng-admin

基于bootstrap实现的响应式Material Design风格的通用后台管理系统，`zheng`项目所有后台系统都是使用该模块界面作为前端展示。

> zheng-ui

各个子系统前台thymeleaf模板，前端资源模块，使用nginx代理，实现动静分离。

> zheng-upms

本系统是基于RBAC授权和基于用户授权的细粒度权限控制通用平台，并提供单点登录、会话管理和日志管理。接入的系统可自由定义组织、角色、权限、资源等。用户权限=所拥有角色权限合集+用户加权限-用户减权限，优先级：用户减权限>用户加权限>角色权限

> zheng-oss

文件存储系统，提供四种方案：

- **阿里云** OSS
- **腾讯云** COS
- **七牛云**
- 本地分布式存储

![阿里云OSS](project-bootstrap/aliyun-oss-post-callback.png)

> zheng-api

服务网关，对外暴露统一规范的接口和包装响应结果，包括各个子系统的交互接口、对外开放接口、开发加密接口、接口文档等服务，可在该模块支持验签、鉴权、路由、限流、监控、容错、日志等功能。示例图：

![API网关](project-bootstrap/gateway_config.png)


> zheng-cms

内容管理系统：支持多标签、多类目、强大评论的内容管理，有基本单页展示，菜单管理，系统设置等功能。

> zheng-pay

- 一站式支付解决方案，统一下单接口，支持支付宝、微信、网银等多种支付方式。不涉及业务的纯粹的支付平台。

- 统一下单（统一下单接口、统一扫码）、订单管理、数据分析、财务报表、商户管理、渠道管理、对账系统、系统监控。

![统一扫码支付](project-bootstrap/zheng-pay.png)

> zheng-ucenter

通用用户管理系统， 实现最常用的用户注册、登录、资料管理、个人中心、第三方登录等基本需求，支持扩展二次开发。

> zheng-wechat-mp

微信公众号管理平台，除实现官网后台自动回复、菜单管理、素材管理、用户管理、消息群发等基础功能外，还有二维码推广、营销活动、微网站、会员卡、优惠券等。

> zheng-wechat-app 

微信小程序后台

## 环境搭建（QQ群内有“zheng环境搭建和系统部署文档.doc”）

#### 开发工具:
- MySql: 数据库
- jetty: 开发服务器
- Tomcat: 应用服务器
- SVN|Git: 版本管理
- Nginx: 反向代理服务器
- Varnish: HTTP加速器
- IntelliJ IDEA: 开发IDE
- PowerDesigner: 建模工具
- Navicat for MySQL: 数据库客户端

#### 开发环境：
- Jdk7+
- Mysql5.5+
- Redis
- Zookeeper
- ActiveMQ
- Dubbo-admin
- Dubbo-monitor

### 工具安装

环境搭建和系统部署文档(作者：小兵，QQ群共享提供下载)

### 资源下载

- JDK7 [http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html](http://u.720life.cn/g/0832d3c13dcf440b8c2ddd37014597194dfce0f4546bd12c9ba469d981d9d729007ebfc8068b2baf5cdf0064d40d499934723df973302be9e8c27d1f120dec7b85d43baa411ec8b965a250d5c3c1a472012739f428572134111b101dee0bb73431be497c15fb2f67990903bce5234822  "JDK7")
- Maven [http://maven.apache.org/download.cgi](http://u.720life.cn/g/bc840264f6cc23df0a8935b6f2922fec94ff6a8561d0b6bc316737cabaa3024658023840c15f3e7f28cf9ac3c1a389dd  "Maven")
- Redis [https://redis.io/download](http://u.720life.cn/g/70336383bbe1092dca9fcec94f2fd1080fb6792497a244eb2803ca3875f6a403  "Redis")
- ActiveMQ [http://activemq.apache.org/download-archives.html](http://u.720life.cn/g/1ef10f1d63639e4eea43ad318c7c3e29aed5a3f8732d353f4cb00d1527d2d9d744b76c3ce781775d2298fb3c59b42d1cc18ce86ea8098829c93376960182c1ef  "ActiveMQ")
- ZooKeeper [http://www.apache.org/dyn/closer.cgi/zookeeper/](http://u.720life.cn/g/c0fe1da5278ca9f6360e901f74721f8472014a29255ca2020681edf6817010be3d654a9189b565f20a6e183ac7296787  "ZooKeeper")
- Dubbo [http://dubbo.io/Download-zh.htm](http://u.720life.cn/g/ad27fc5875c834b4568aeb04084d2bc018cae7cae1a1e67fee62968346f5790e  "Dubbo")
- Elastic Stack [https://www.elastic.co/downloads](http://u.720life.cn/g/de3742c0ac7bbef6b8feb3a0318f07719aab0e585c5d880a6a8d7f20f20bbd9f  "Elastic Stack")
- Nginx [http://nginx.org/en/download.html](http://u.720life.cn/g/8e5d45d2feb3582a8a09a3bac21cb32b916bb5a86180a7329f0f39fd9ce0a11f7693c98ac1ed44979fa2773022033a34  "Nginx")
- Jenkins [http://updates.jenkins-ci.org/download/war/](http://u.720life.cn/g/c896990f5bd3c33c5a533ade338e7f53e07c1eb407401bbf07f8ddf4817f9c59b99ed3f6ace5ea93e698e651fff1f96c  "Jenkins")
- dubbo-admin-2.5.3 [http://download.csdn.net/detail/shuzheng5201314/9733652](http://u.720life.cn/g/9b4a1380e2aa619eac4d900347bdc8b988b3227d0eaf6623ada963ebde1c3087f877ab51bf6b6cfa59178b20cdecaa0445e424d477c34713559a35402531614c  "dubbo-admin-2.5.3")
- dubbo-admin-2.5.4-SNAPSHOT-jdk8 [http://download.csdn.net/detail/shuzheng5201314/9733657](http://u.720life.cn/g/9b4a1380e2aa619eac4d900347bdc8b988b3227d0eaf6623ada963ebde1c3087f877ab51bf6b6cfa59178b20cdecaa0407d7598ca7adbedc3d03a76d0c5c28a5  "dubbo-admin-2.5.4-SNAPSHOT-jdk8")
- 更多资源请加QQ群

## 开发指南:

- 1、本机安装Jdk7、Mysql、Redis、Zookeeper、ActiveMQ并**启动相关服务**，使用默认配置默认端口即可
- 2、克隆源代码到本地并打开，**推荐使用IntelliJ IDEA**，本地编译并安装到本地maven仓库

### 修改本地Host

- 127.0.0.1	ui.zhangshuzheng.cn
- 127.0.0.1	upms.zhangshuzheng.cn
- 127.0.0.1	cms.zhangshuzheng.cn
- 127.0.0.1	pay.zhangshuzheng.cn
- 127.0.0.1	ucenter.zhangshuzheng.cn
- 127.0.0.1	wechat.zhangshuzheng.cn
- 127.0.0.1	api.zhangshuzheng.cn
- 127.0.0.1	oss.zhangshuzheng.cn
- 127.0.0.1 config.zhangshuzheng.cn

- 127.0.0.1	zkserver
- 127.0.0.1	rdserver
- 127.0.0.1	dbserver
- 127.0.0.1	mqserver

### 编译流程

maven编译安装zheng/pom.xml文件即可

### 启动顺序（后台）

> 准备工作

- 新建zheng数据库，导入project-datamodel文件夹下的zheng.sql

- 修改各dao模块和rpc-service模块的redis.properties、jdbc.properties、generator.properties数据库连接等配置信息，其中master.redis.password、master.jdbc.password、slave.jdbc.password、generator.jdbc.password密码值使用了AES加密，请使用com.zheng.common.util.AESUtil工具类修改这些值

- 启动Zookeeper、Redis、ActiveMQ、Nginx（配置文件参考project-tools/nginx下的*.conf文件）

> **zheng-upms**

- 首先启动 zheng-upms-rpc-service(直接运行src目录下的ZhengUpmsRpcServiceApplication#main方法启动) => zheng-upms-server(jetty)，然后按需启动对应子系统xxx的zheng-xxx-rpc-service(main方法) => zheng-xxx-webapp(jetty)

![启动演示](project-bootstrap/start.png)

- 访问 [http://upms.zhangshuzheng.cn:1111/](http://u.720life.cn/g/df3cbdb42fe1f1ef1ec67f4fb72ed3dbceba944aeb34e8dd008653f7ee69cb5e0d8ab8eb4605aca09932ebc17792970a  "统一后台地址")，子系统菜单已经配置到zheng-upms权限中，不用直接访问子系统，默认帐号密码：admin/123456

- 登录成功后，可在右上角切换已注册系统访问

> **zheng-cms**

- zheng-cms-admin：启动ActiveMQ-启动 => 启动zheng-rpc-service => 启动zheng-cms-admin

- zheng-cms-web：启动nginx代理zheng-ui静态资源，配置文件可参考 [nginx.conf](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d47239a8476d8e96a4930b936ff5feb23ef2461b58c40cbbcade47e760d8b19778b6f26b1fe2774bf294cf954edfd8455) 

> **zheng-oss**

- 首先启动zheng-oss-web服务

- 开发阶段，如果zheng-oss-web没有公网域名，推荐使用`ngrok`内网穿透工具，为开发环境提供公网域名，实现上传回调

- 启动nginx代理zheng-ui静态资源


### 开发演示（QQ群内有“zheng十分钟视频：从检出到启动.wmv”）

- 创建数据表（建议使用PowerDesigner）

- 直接运行对应项目dao模块中的generator.main()，可自动生成单表的CRUD功能和对应的model、example、mapper、service代码

    - 生成的model和example均已实现Serializable接口，支持分布式

    - 已包含抽象类BaseServiceImpl，只需要继承抽象类并传入泛型参数，即可默认实现mapper接口所有方法，特殊需求直接扩展即可
    
    - BaseServiceImpl默认已实现四种根据条件分页接口
     
        - selectByExampleWithBLOBsForStartPage()
        
        - selectByExampleForStartPage()
        
        - selectByExampleWithBLOBsForOffsetPage()
        
        - selectByExampleForOffsetPage()

    - BaseServiceImpl方法根据读写操作自动切换主从数据源，继承的扩展接口，可手动通过`DynamicDataSource.setDataSource(DataSourceEnum.XXX.getName())`指定数据源

- 启动流程：优先rcp-service服务提供者，再启动其他webapp

- 扩展流程：可扩展和拆分rpc-api和rpc-service模块，可按微服务拆分或场景拆分

### 部署方式（QQ群内有“zheng十分钟视频：从打包到linux服务器部署.wmv”）

- war包项目：使用tomcat等web容器启动

- rpc-service服务提供者jar包：将打包后的zheng-xxx-rpc-service-assembly.tar.gz文件解压，使用bin目录的管理脚本运行即可，支持优雅停机。

### 框架规范约定

约定优于配置(convention over configuration)，此框架约定了很多编程规范，下面一一列举：

```

- service类，需要在叫名`service`的包下，并以`Service`结尾，如`CmsArticleServiceImpl`

- controller类，需要在以`controller`结尾的包下，类名以Controller结尾，如`CmsArticleController.java`，并继承`BaseController`

- spring task类，需要在叫名`task`的包下，并以`Task`结尾，如`TestTask.java`

- mapper.xml，需要在名叫`mapper`的包下，并以`Mapper.xml`结尾，如`CmsArticleMapper.xml`

- mapper接口，需要在名叫`mapper`的包下，并以`Mapper`结尾，如`CmsArticleMapper.java`

- model实体类，需要在名叫`model`的包下，命名规则为数据表转驼峰规则，如`CmsArticle.java`

- spring配置文件，命名规则为`applicationContext-*.xml`

- 类名：首字母大写驼峰规则；方法名：首字母小写驼峰规则；常量：全大写；变量：首字母小写驼峰规则，尽量非缩写

- springmvc配置加到对应模块的`springMVC-servlet.xml`文件里

- 配置文件放到`src/main/resources`目录下

- 静态资源文件放到`src/main/webapp/resources`目录下

- jsp文件，需要在`/WEB-INF/jsp`目录下

- `RequestMapping`和返回物理试图路径的url尽量写全路径，如：`@RequestMapping("/manage")`、`return "/manage/index"`

- `RequestMapping`指定method

- 模块命名为`项目`-`子项目`-`业务`，如`zheng-cms-admin`

- 数据表命名为：`子系统`_`表`，如`cms_article`

- 更多规范，参考[[阿里巴巴Java开发手册] http://git.oschina.net/shuzheng/zheng/attach_files

```

## 演示地址

演示地址： [http://upms.zhangshuzheng.cn/](http://u.720life.cn/g/1f3224c66310fc0ecd4e0f19ef0d14d2b994fbaf91bcf5b35db722aeb30f696214547970c3eb92c53fcefa22a1678b25684ab489d561dd429f48d7575613f33472e8d4460f56c20a0ea6ac59feb8e6e6cce7241e8fdf31d65e79f8e3caff32d0219c2d0d5500dbe5c41d7b57c54c4f0c3c3704f4bbdfa2d0b602dd9b0bd61a5e  "演示地址")

### 预览图
![idea](project-bootstrap/idea.png)
![login](project-bootstrap/zheng-login.png)
![upms](project-bootstrap/zheng-upms.png)
![cms](project-bootstrap/zheng-cms.png)
![swagger](project-bootstrap/api.png)

### 数据模型
![数据库模型](project-datamodel/zheng.png)

### 拓扑图
![拓扑图](project-bootstrap/distributedSystem.png)

### 开发进度
![开发进度](project-bootstrap/progress.png)

### 参与开发

首先谢谢大家支持，如果你希望参与开发，欢迎通过[Github](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467faba9083dbd846c77818d3de6c1e6683cc447ebf04884c5d897ac0463120031  "Github")上fork本项目，并Pull Request您的commit。

### 常见问题

- Eclipse下，dubbo找不到dubbo.xsd报错，不影响使用，如果要解决，可参考 [http://blog.csdn.net/gjldwz/article/details/50555922](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a48402d7a947450bffee6af030133d57084d63d7f7bac15764c9f09d1fe98259d41137e64eb2e177d86c920fc812864d20) 

- 报zheng-xxx.jar包找不到,请按照文档编译顺序，将源代码编译并安装到本地maven仓库

- zheng-cms-admin启动卡住：因为没有启动activemq

- zheng-upms-server访问报session不存在：因为没有启动redis服务

- 界面没有样式：因为zheng-admin没有编译安装到本地仓库

## 附件

### 优秀文章和博客

- [创业互联网公司如何搭建自己的技术框架](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271b15a9f3143a820af99b242bac1bddb954  "创业互联网公司如何搭建自己的技术框架")

- [微服务实战](http://u.720life.cn/g/6900aa436d7855810ebad430307e6f91c8b258b81c5d2f9bc5f21dfc6a8e3e476f5099637ad4e484cf12e03573d42117  "微服务实战")

- [单点登录原理与简单实现](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271bb354c5efa3ac8ba29954917c7df65aa6  "单点登录原理与简单实现")

- [ITeye论坛关于权限控制的讨论](http://u.720life.cn/g/79075b0b214ce70be040eb4c2085a0293f326ef3556a41b398ecd08515aa182e2a4ed9c0a2ce57dacf3198757e3da7f5  "ITeye论坛关于权限控制的讨论")

- [RBAC新解：基于资源的权限管理(Resource-Based Access Control)](http://u.720life.cn/g/e3cb95d362ac306ae496c1ccddb5809d72fe18e8899e8e99b83d1c0660b228f8fa57f4672728696fb9dc5138159f51e9  "RBAC新解：基于资源的权限管理(Resource-Based Access Control)")

- [网站架构经验随笔](http://u.720life.cn/g/25906bdc0fc16400f02556971e599f2709f07a74efd3d4d325692c8721bf9a8ad40fafa7ee93a8de30a83945075bf27f  "网站架构经验随笔")

- [支付系统架构](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271b8bffd136c44a789da4621e820bd3ae15  "支付系统架构")

- [Spring整合JMS](http://u.720life.cn/g/cb08bef269584a7a80de468db7afa45642d3fde81548ececa5b67575169a754e7c8741219ac5aca2a93732bc43c52aa9  "Spring整合JMS")

- [跟我学Shiro目录贴](http://u.720life.cn/g/25906bdc0fc16400f02556971e599f2709f07a74efd3d4d325692c8721bf9a8ab8c87cac52b8a05c0c291999de469593  "跟我学Shiro目录贴")

- [跟我学SpringMVC目录汇总贴](http://u.720life.cn/g/25906bdc0fc16400f02556971e599f2709f07a74efd3d4d325692c8721bf9a8ab1cea63b6a6ce820aecf330dc6f9bf37  "跟我学SpringMVC目录汇总贴")

- [跟我学spring3 目录贴](http://u.720life.cn/g/25906bdc0fc16400f02556971e599f2709f07a74efd3d4d325692c8721bf9a8a127be06a0613b1d1dd7c62037a8cee3d  "跟我学spring3 目录贴")

- [跟我学OpenResty(Nginx+Lua)开发目录贴](http://u.720life.cn/g/25906bdc0fc16400f02556971e599f2709f07a74efd3d4d325692c8721bf9a8a037e0d08dd8c44e1710e0e2e637474a8  "跟我学OpenResty(Nginx+Lua)开发目录贴")

- [Redis中文网](http://u.720life.cn/g/5bbeb658b3b29111025f8f6d1b1ac7e7e21d6b0d95f9c13dae9935dd5c101b9d  "Redis中文网")

- [读懂Redis并配置主从集群及高可用部署](http://u.720life.cn/g/ecc7d42b8e4205e5d387aa616e7cff787790df498634a7265a9de812e3c83a31e93e0b90cc47fa55b144a3c2218eaa25fe81aec28a7a4904cadff3cd16e00bff553476f3b697d9822735b61e7a6f056882da3ac3740c04856c772336c012f060f16442387226b5c86f81dccab53b134e36914f260ebe78459ba10cdbd1f727eeb63c6ee6b697ec4713f1e1280a502c364dcb55d79d951951c0b047c77df059739236165207208063c8bd6ea225307f355f4ad0c6b6968a9d2d589fc954b632d276f238e5816c8ce301711ee57cdb423f56a7e910b276b3201bf667488b8153b55441bc4fa62ee8536a5309692b777a82f285de6a590e4dd0df09ef4f8f9e8b0b  "读懂Redis并配置主从集群及高可用部署")

- [Redis哨兵-实现Redis高可用](http://u.720life.cn/g/502b1a7fb5953291c483003b357df3951a7cd3dc9aa86b3c1000a6d40c935ddbe2d2143c3f2e9fbfd45b3b7694daf4b2  "Redis哨兵-实现Redis高可用")

- [ELK(ElasticSearch, Logstash, Kibana)搭建实时日志分析平台](http://u.720life.cn/g/fd6eca4b0fbbac408c109c69a910940dcf3c092220662b4ba88b8a70684ddbca27fc729ec92e2a633d407c6142a64e46ddf76105329fe4c637ec337cc4e8c6dd  "ELK(ElasticSearch, Logstash, Kibana)搭建实时日志分析平台")

- [Nginx基本功能极速入门](http://u.720life.cn/g/5ffdf2a24e1b2bbd5675a4ce14af25eb6286f7650c3d9402857cef26d27f0d89a7444804986fbed1f33543bfc9204d0b  "Nginx基本功能极速入门")

- [mybatis-genarator 自定义插件](http://u.720life.cn/g/a88615b97db01a1ba3d626afe31cb17318cd075ba15e084639bc845a84cace7a83a89472f1b9ac7dfd43ca0f7d18c3ff  "mybatis-genarator 自定义插件")

- [Elasticsearch权威指南（中文版）](http://u.720life.cn/g/38a6caf4b41304d8700b935c585d5fe5c5a18657f3c23822170efbff94ecd6378a5184bd411353cc6ea5cac932491c6bf1f48d8eaa61bc13c6d31b1e3807019f  "Elasticsearch权威指南（中文版）")

- [springMVC对简单对象、Set、List、Map的数据绑定和常见问题.](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4e3a725e5cc303574b6644d569864ebacae3bbbc6d47a55533be3bdb62ede042fe677d9514d5d6e2b9e9afee1c7cda1ed  "springMVC对简单对象、Set、List、Map的数据绑定和常见问题.")

- [如何细粒度地控制你的MyBatis二级缓存](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4f99ee5337203e4bde43039a4e9bfbced50ad1850edac672ce0d27b828ba42fc0b089ed6cb909920823e978d132bc6766  "如何细粒度地控制你的MyBatis二级缓存")

- [做个男人，做个成熟的男人，做个有城府的男人](http://u.720life.cn/g/45f036fc5b3781fe5f54f972e8095fb50e0c5a5ca37de71d2917cfab719c271b8916b1d051befffbb0e09d31de280b72  "做个男人，做个成熟的男人，做个有城府的男人")


### 在线小工具

- [在线Cron表达式生成器](http://u.720life.cn/g/41a88c49241c9a1f605f913332fbeca495e13ea8491440f895022f4f9df8c3e3  "在线Cron表达式生成器")

- [在线工具 - 程序员的工具箱](http://u.720life.cn/g/41843dbe0fafe94d482221c4b6428051  "在线工具 - 程序员的工具箱")

### 在线文档

- [JDK7英文文档](http://u.720life.cn/g/0b74b15bb9de87b5a2fb1d39225b742f9755696133ba7493060bcd72b849d00cc424e0901ba49e1f7b1c0c7ad11a37d3e40ba7e7c999548bff8af0052835554f  "JDK7英文文档")

- [Spring4.x文档](http://u.720life.cn/g/3d3c1eebe7d1a3ce4b19ffb3e57807e89fa619207522cc50e254f65d86af1be0b306863a011de5ef8e4a8b3c5c17ee5d  "Spring4.x文档")

- [Mybatis3官网](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a215e4d93221eb26b660bea25686b89be63142caf406b6e1c14d3ab51db921e10ca  "Mybatis3官网")

- [Dubbo官网](http://u.720life.cn/g/ad27fc5875c834b4568aeb04084d2bc0  "Dubbo官网")

- [Nginx中文文档](http://u.720life.cn/g/0b74b15bb9de87b5a2fb1d39225b742f9755696133ba7493060bcd72b849d00c70ea5132d4eda0624001e88d63d0a989754ed6dd7d93878effc7028703b52239  "Nginx中文文档")

- [Freemarker在线手册](http://u.720life.cn/g/91631dc92407872deef9e7c2f21c90370ec42bca0660599fef01f69ddec2c69d  "Freemarker在线中文手册")

- [Velocity在线手册](http://u.720life.cn/g/7b1a2cc30709fab1f7d3403a12a69622014754ee2d62e2b7aa50d029c7b0b7e601990af5feaafb66030c1887a5b8f3fb78ff2e9ed95d64280286dca81679e83b  "Velocity在线手册")

- [Bootstrap在线手册](http://u.720life.cn/g/5dc63d04a35b84846e193be705862c773cff2a22a6b2940498e28eb01e58b4bd  "Bootstrap在线手册")

- [Git官网中文文档](http://u.720life.cn/g/0699e533b96232c5e210af6ab5668134f26d4ce8eb73c737efb58c5e94ea6f74  "Git官网中文文档")

- [Thymeleaf](http://u.720life.cn/g/93cb058e2406031f6144e42823783979064a4202b3689251145126e998ce8f5defa6da90df7b82a90b1cc7a1307b069c6b1ac6b538cb2504cf0ab092b85f079d  "Thymeleaf")

## 许可证

[MIT](LICENSE "MIT")



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)