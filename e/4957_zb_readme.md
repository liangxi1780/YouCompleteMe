# zb

- 支付技术交流QQ群 ：470414533
- 联系QQ : 842324724
- 联系邮箱 ： 842324724@qq.com

详细技术讨论请加QQ群，营造一个温馨、有质量的技术学习空间。

## 前言

　　`zb`项目创建于2017年5月12日，正在慢慢成长中，目的是随着技术积累而慢慢开发一套分布式架构系统。全部采用目前主流技术与框架，为在技术方面有需要的朋友提供一套完整的研究学习实例。

## 项目介绍

　　基于Spring+SpringMVC+Mybatis分布式敏捷开发系统架构，提供整套公共微服务服务模块：内容管理、支付中心、用户管理（包括第三方）、微信服务系统、文件存储系统、配置中心、日志分析、任务和消息通知等。
 　　以上模块目前只是开发了用户管理系统，由于时间与精力有限，加上技术上本人也并非大牛，项目框架与代码都需要重新设计和整理，后期会慢慢的整理。上面模块是我的目标。

### 组织结构

``` lua
zb
├── zb-common -- 公共配置与工具类模块
|    ├── zb-config -- 配置管理中心
|    ├── zb-util -- 工具类、全局辅助类等
├── zb-ucenter -- 用户系统(包括第三方登录)
|    ├── zb-ucenter-dao -- 数据访问层
|    ├── zb-ucenter-rpc-api -- rpc接口包
|    ├── zb-ucenter-rpc-service -- rpc服务提供者
|    └── zb-ucenter-server -- dubbo服务注册模块
|    └── zb-ucenter-web -- 网站前台
├── zb-wechat -- 微信系统
|    ├── zb-wechat-rpc-api -- rpc接口包
|    ├── zb-wechat-rpc-service -- rpc服务提供者
|    └── zb-wechat-server -- dubbo服务注册模块
├── zb-oa -- OA办公系统
|    ├── zb-oa-rpc-api -- rpc接口包
|    ├── zb-oa-rpc-service -- rpc服务提供者
|    └── zb-oa-server -- dubbo服务注册模块
|    └── zb-oa-web -- 网站前台
├── zb-mq -- MQ消息队列服务系统
|    ├── zb-mq-rpc-api -- rpc接口包
|    ├── zb-mq-rpc-service -- rpc服务提供者
|    └── zb-mq-server -- dubbo服务注册模块
├── zb-oauth -- SSO单点登录模块(CAS源码)
├── zb-entity -- 用户实体模块
└── zb-socket -- socket服务推送模块
```

### 技术选型

#### 后端技术:
技术 | 名称 | 官网
------|-------|-------
Log4J | 日志组件 | [http://logging.apache.org/log4j/1.2/](http://u.720life.cn/g/d24248ea9b8085edf05b454a12c4113a4a243943067bd43da78e8d962bb8001b5bcdd716e023965ecc87eca2217c0aa6) 
Maven | 项目构建管理 | [http://maven.apache.org/](http://u.720life.cn/g/bc840264f6cc23df0a8935b6f2922fec747e8988e9d6774b642901b9662b323f) 
Spring Framework | 容器 | [http://projects.spring.io/spring-framework/](http://u.720life.cn/g/e0845233bf5cae93142c4c8e1c8864d4e670a90f87afc2ad04fb4c1d1899c07fdd2c7fa40574a04f80c374ab3968c758) 
SpringMVC | MVC框架 | [http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/#mvc](http://u.720life.cn/g/a6ba8c6b0e93c9f31bd435772627160d78653d6a55dc6315bda807ef09f29a08138b35c7e95760a878e8a0494b6946c305ffdacf75171f9fb043ea8675f3d72d7a4c2af751af247d69b57160e21c66cf4b1624d4570ec58555958c387c809a0d) 
Apache Shiro | 权限管理框架  | [http://shiro.apache.org/](http://u.720life.cn/g/c3294dc73186562102bd8975db9e807be68145a3e524f14e47e43b209703de8b) 
MyBatis | ORM框架  | [http://www.mybatis.org/mybatis-3/zh/index.html](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a215e4d93221eb26b660bea25686b89be63142caf406b6e1c14d3ab51db921e10ca) 
Mapper | Mybatis封装框架  | [http://git.oschina.net/free/Mapper/](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd4032c848a4f5ea74354a7f9e7145f560c44) 
PageHelper | MyBatis分页插件  | [http://git.oschina.net/free/Mybatis_PageHelper/](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d0c5e449aa2c2e2afac3f4646cf34dfd6346061eac08c9ec3408866b5b4464e3a) 
ZooKeeper | 分布式协调服务  | [http://zookeeper.apache.org/](http://u.720life.cn/g/9036bb30203a9192b0bca1ff23f6480f71d7ad868c7c8d1a9b3c2b9a91b88dd3) 
Dubbo | 分布式服务框架  | [http://dubbo.io/](http://u.720life.cn/g/ad27fc5875c834b4568aeb04084d2bc0) 
Redis | 分布式缓存数据库  | [https://redis.io/](http://u.720life.cn/g/70336383bbe1092dca9fcec94f2fd10823c1cea91ac1108405bfbd56f5b819fc) 
Quartz | 作业调度框架  | [http://www.quartz-scheduler.org/](http://u.720life.cn/g/beb95a72271892e3173f0dad802e5ddf75666c78a77f9b92d69407e846140c43) 
ActiveMQ | 消息队列  | [http://activemq.apache.org/](http://u.720life.cn/g/1ef10f1d63639e4eea43ad318c7c3e29e5e0b9b20040db508812cdd15d1a010d) 
Disconf | 分布式配置管理平台  | [http://disconf.readthedocs.io/zh_CN/latest/](http://u.720life.cn/g/e6a63ee4c6cf2077365a51a7df5c334d8073086f95b41c50feb5385543a45571f0fba51e4350935a9fc80345e45a9fe3) 
SockJS | websocket封装框架  | [https://github.com/sockjs/sockjs-client/](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cc1c7acbe170c416f671845216f94e0dda3a79811d72a1406ea8f769c19a6e89) 
CAS | 单点登录认证系统  | [https://www.apereo.org/projects/cas/](http://u.720life.cn/g/4f9b6750213fda1e93a8c65eb07a1d47876f2c75c3ea3b8b2c101b99df33ab7afb801e5e10f5153c2601fdd3cc9ea2c9) 
Netty | 网络应用程序通信框架  | [http://netty.io/](http://u.720life.cn/g/4ee4780bf52b98267db4e8a22bf13ffa) 
Activiti | 工作流框架  | [https://www.activiti.org/](http://u.720life.cn/g/f45d6e1ca06e5ac29f16886eab23fcc58e34b53200ed0fbef85838a7d85dafa4) 
MessagePack | 对象序列化类库  | [http://msgpack.org/](http://u.720life.cn/g/0383ed379379708b0cd69df5b9046da8eb65b29a68fed764af13f7d526aa1979) 
Mycat | 数据库分库分表中间件  | [http://www.mycat.io/](http://u.720life.cn/g/a74f79b5e482ad27d782d87a16de6bec4652d7ba13d94e83a567cd4b956fff20) 


#### 前端技术:
技术 | 名称 | 官网
----|------|----
jQuery | 函式库  | [http://jquery.com/](http://u.720life.cn/g/bf5ee7c5d8e747312b9dff6cfd25472308f0e1fd43291f641e8858d899a5b79d) 
Bootstrap | 前端框架  | [http://getbootstrap.com/](http://u.720life.cn/g/e23be2821e5181a1a46a005bc6e93d9dc1c8dad0ef41593aa593e12a30fc455b) 
zTree | 树插件  | [http://www.treejs.cn/](http://u.720life.cn/g/498bbd2d294e9101825c13f60c5e8cb37ad483479c706d78427ea72fbedef7eb) 
jQuery DataTable | 表格插件  | [http://datatables.club/](http://u.720life.cn/g/ba956d5e67bc43ac88bf11fadc147a8d3e4646ef53db08166dbaab42a1dfb290) 
jQuery Validation | 表单验证插件  | [https://jqueryvalidation.org/](http://u.720life.cn/g/9d3497d3eb9e11a2152cc317535bb180ff04ece68d98ae7618f97bf0484012c6) 
msgbox | 漂亮提示信息插件  | [http://www.jq22.com/jquery-info1966](http://u.720life.cn/g/d8e2a8345f45bbbaed62bb42062ead4042b8b5902816808b8259f90aa10e67c9d510aea77f154de1f601cc4aca1bb98b) 
My97DatePicker | 日期控件  | [http://www.my97.net/dp/demo/index.htm](http://u.720life.cn/g/84cf1fac38589bbdbe530b0412ea845558c1484ed99616610ff6d7877ca2a3d20e009990cb4996e5bb1083828edb6784) 
UEditor | 百度富文本编辑器  | [http://fex.baidu.com/ueditor/](http://u.720life.cn/g/2ec7fed527cfc306d0ab68523b3da8a69027d3003dd3c350ab9216c8c140cdd2) 
ECharts | Javascript图表库  | [http://echarts.baidu.com/feature.html](http://u.720life.cn/g/3ae663c7907c8270970591085eabb608e339b14e97ea8c218f93240d9654c76f9220391476883d36a4750dcae8f68cad) 
Highcharts | Javascript图表库  | [https://www.hcharts.cn/demo/highcharts](http://u.720life.cn/g/45ae0b69d7168dcaf785178629c2b71e36de8e9a293bf02c645c667b2ffe2352c0adebb8df8e069ae35c76224116e658) 
H-ui | H-ui 前端框架  | [http://www.h-ui.net/](http://u.720life.cn/g/fa330ac51f45f671467276b286c4bcba0030b22b1cfbf6f7b011897eea8035ec) 
H-ui.admin | 网站后台模版  | [http://www.h-ui.net/H-ui.admin.shtml](http://u.720life.cn/g/fa330ac51f45f671467276b286c4bcba04ea977bad0fc097aec8e43ae5c14e2923a239bce5a4a87d953fbe9cbec91f95) 
Layer | web弹层组件  | [http://layer.layui.com/](http://u.720life.cn/g/d6276f71012dea0742ec9af0acbaffd3bd2dc9703f25e563fbb8b365fdb374da) 
SockJS | client与server通信框架(类似websocket)  | [http://sockjs.org](http://u.720life.cn/g/b6dd6285d2dfb9c33b7d45a5783a099674ca461b8dd4a05827d6ddf4936c39f7) 


#### 模块介绍

> zb-common

- 公共资源文件、工具类、配置等信息

> zb-entity

- 实体bean模块

> zb-oauth

- CAS单点登录模块，CAS源代码

> zb-socket

- 服务器消息推送模块。后端使用了spring-websocket服务器端通信框架。前端使用了sockjs作为连接服务器端通信的javascript api。
- SockJS是一个浏览器JavaScript库，它提供了一个类似WebSocket的对象。SockJS为您提供了一个连贯，跨浏览器的JavaScript API，可在浏览器和Web服务器之间创建低延迟，全双工，跨域通信通道。
- 在引擎罩下，SockJS首先尝试使用本机WebSockets。如果失败，它可以使用各种特定于浏览器的传输协议，并通过类似WebSocket的抽象来呈现它们。
- SockJS旨在适用于所有现代浏览器和不支持WebSocket协议的环境。

> zb-mq

- MQ消息服务模块，目前采用了activemq作为消息服务的框架。
- 简单实现了订单同步消息的发送处理、微信模板消息的发送处理。
- 优点是消息的异步通知与处理。高并发情况下缓解系统压力，提高系统业务处理能力。

> zb-oa

- OA办公系统，目前暂未开发，后期会开发。集成cas单点登录功能，实现多个项目的统一登录认证。

> zb-ucenter

- 用户管理中心系统，提供用户角色与权限管理
- 目前所有功能开发都在此模块中(功能有限，如果分布到其他模块，有点小题大做，不易于学习，后期功能多了之后再慢慢分工)，后期会将不同功能分布到其他模块管理。

> zb-wechat

- 微信功能模块。对微信多数接口进行了接口封装，方便使用。

## 环境搭建

(后期补充)

#### 开发工具:
- MySql: 数据库(目前数据库连接的是我的服务器mysql)
- Tomcat: 应用服务器
- Git: 版本管理(目前项目源码托管于开源中国，暂不支持其他人员一起开发)
- Nginx: 反向代理服务器(本地开发环境无须安装，线上环境需要安装，实现动静分离)
- eclipse: 开发IDE
- PowerDesigner: 建模工具
- Navicat for MySQL: 数据库客户端（或者使用SQLyog）
- Mycat: 数据库分库分表中间件。(本地开发无须安装，只是在服务器环境上配置数据库主从、mycat服务)
#### 开发环境：
- Jdk7+
- Mysql5.5+
- Redis (可连接我的服务器中的redis服务)
- Zookeeper (可连接我的服务器中的redis服务)
- ActiveMQ (可连接我的服务器中的redis服务)
- Dubbo-admin (可访问我的服务器中的dubbo-admin：http://www.2b2b92b.com:4050/dubbo-admin)

### 工具安装

(后期补充)

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

- 1、请确保自己本机已经安装Jdk7、maven(建议使用阿里云的maven仓库)
- 2、如果想自己搭建服务，那么请确保自己本机安装好以下服务：Mysql、Redis、Zookeeper、ActiveMQ并**启动相关服务**，使用默认配置默认端口即可，其中，MQ可不安装，不影响项目启动，如果想使用zb-mq模块功能，需要启动activemq服务。
- 3、克隆当前项目的源代码到本地并打开，**我使用的是Eclipse Java EE IDE for Web Developers.**，通过maven方式导入到eclipse中。
- 4、项目中存在activiti工作流框架，对于.bpmn工作流文件的设计与管理，需要安装eclipse的一个插件，才可对文件进行可视化设计。除非你对文件配置非常熟悉，可手动编码。

### 修改本地Host

- 由于项目使用了cas单点登录，如果不想连接我的服务器的CAS服务，就需要你打包好zb-oauth这个模块，配置好自己的域名。
- 域名的话，可以通过修改本机host文件指定。CAS不支持ip访问的，所以需要配置域名

### 编译流程

maven的编译打包，我就不多说了。如果在项目编译或者打包部署期间出现了什么问题，可以联系我询问。

### 启动顺序（后台）

> 环境配置准备工作（如果想自己搭建环境，请确保安装以下服务）：

- mysql数据库，导入zb-ucenter-web模块下的[sql脚本]文件夹下的sql文件。

- 安装redis、zookeeper、activemq、disconf(觉得麻烦的可不修改，使用我的服务器服务即可)、cas单点登录服务(也可不修改，使用我的服务器的cas)

- 修改zb-conf模块下的各种连接等配置信息

- 启动Zookeeper、Redis、ActiveMQ、Disconf(使用本机服务的话需要启动服务)、CAS(使用本机服务的话需要启动服务)

> **zb-ucenter**

- 首先启动 zb-ucenter-server (dubbo服务注册)，再启动zb-ucenter-web (dubbo服务订阅)

- 访问 zb-ucenter-web，默认帐号/密码：admin/123456

- 登录成功后，方可操作(目前还未实现多系统的单点登录集成认证)。

> **zb-mq**

- 目前MQ功能还未集成到项目中，后期会加入进来



### 部署方式

- war包项目：使用tomcat等web容器启动

### 框架编码规范约定

约定优于配置(convention over configuration)，此框架约定了很多编程规范，比如：

```

- service类，需要在叫名`service`的包下，并以`Service`结尾，如`UserServiceImpl`

- controller类，需要在以`controller`结尾的包下，类名以Controller结尾，如`UserController.java`

- spring task类，需要在叫名`task`的包下，并以`Task`结尾，如`TestTask.java`

- mapper.xml，需要放到zb-*-dao模块对应的包下，并以`Mapper.xml`结尾，如`UserMapper.xml`

- mapper接口，需要放到zb-*-dao模块对应的包下，并以`Mapper`结尾，如`UserMapper.java`

- entity实体类，需要放到zb-entity模块下，命名规则为数据表转驼峰规则，如`SysUser.java`

- spring配置文件，命名规则为`spring-*.xml`

- 类名：首字母大写驼峰规则；方法名：首字母小写驼峰规则；常量：全大写；变量：首字母小写驼峰规则，尽量非缩写

- 全局的配置文件放到zb-conf模块下的`src/main/resources`目录下，单独的项目模块的配置文件，放到对应的模块下的`src/main/resources`

- 前端静态资源文件放到`src/main/webapp/resources`目录下

- jsp文件，需要在`/WEB-INF/view`目录下

- 模块命名为`项目`-`子项目`-`业务`，如`zb-ucenter-web`

- 更多规范，参考[阿里巴巴Java开发手册] http://git.oschina.net/zhoubang85/zb/attach_files

```

## 演示地址(目前只发布了[用户管理中心系统：zb-ucenter-web])

演示地址： [http://www.2b2b92b.com](http://u.720life.cn/g/be31f5f8d05fdded2b830214f5a96c46a7b70f1348da062ebedc14849bfe785f  "用户管理中心系统访问地址")

### 预览图
![login](zb-doc/preview/login.jpg)
![userlist](zb-doc/preview/userlist.jpg)
![tomcatlogmonitor](zb-doc/preview/tomcatlogmonitor.jpg)
![nettychat](zb-doc/preview/nettychat.jpg)
![socketpushall](zb-doc/preview/socketpushall.jpg)
![wxmsgtemplate](zb-doc/preview/wxmsgtemplate.jpg)
![activitibpmnlist](zb-doc/preview/activitibpmnlist.jpg)
![addrole](zb-doc/preview/addrole.jpg)
![msgalert](zb-doc/preview/msgalert.jpg)
![myactprocessrecord](zb-doc/preview/myactprocessrecord.jpg)
![permissionadd](zb-doc/preview/permissionadd.jpg)
![socketpushmy](zb-doc/preview/socketpushmy.jpg)
![myactiviti](zb-doc/preview/myactiviti.jpg)
![themegreencloor](zb-doc/preview/themegreencloor.jpg)
![redcolor](zb-doc/preview/redcolor.jpg)
![deptactpproval](zb-doc/preview/deptactpproval.jpg)


### 数据模型

(后期补充)

## 附件

(后期补充)

### 优秀文章和博客

(后期补充)

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

- [Bootstrap在线手册](http://u.720life.cn/g/5dc63d04a35b84846e193be705862c773cff2a22a6b2940498e28eb01e58b4bd  "Bootstrap在线手册")

- [Git官网中文文档](http://u.720life.cn/g/0699e533b96232c5e210af6ab5668134f26d4ce8eb73c737efb58c5e94ea6f74  "Git官网中文文档")



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)