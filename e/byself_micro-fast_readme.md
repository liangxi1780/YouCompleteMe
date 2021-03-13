# 欢迎查看ms项目说明

## 项目简介
  `micro-fast`使用mybatis,spring系列框架作为基础，致力于打造一套中小企业系统解决方案.项目中对常用技术进行封装便于复用以及提高
开发效率，还提供了一个借助springcloud实现的一个分布式项目．这不仅仅是一个springCloud项目，项目中提供了诸多可复用的基础模块，也
许有你想要，可以方便的引入到自己的项目中快速集成。项目的思想是不写一次性代码，所有基础模块都可以在其他项目中通过简单配置快速集成。
如果你觉得本项目对你有帮助，欢迎star;如果你想更深入的了解本项目欢迎加入`qq`交流群`640791460`，如果你乐于分享，欢迎加入本项目的开
发中来，每一个点点滴滴提交都是对项目发展的巨大贡献。
## 参与进来
### `qq`交流群`640791460` 
### 本地部署文档详见[ms开发文档](./all/ms/deploy.md)
## 项目概览
- `mybatis-generator-extend-maven-plugin`模块是便于快速根据条件生成mybatis-generator-plugin配置文件的maven扩展插件，基本增
删改查、按条件分页查询`dao` `servcie` `controller`层利用了词向量、卷积神经网络、使用人工智能技术进行代码语意分析(好吧，我吹不
下去了)自动生成，自动生成70%代码，降低开发中重复性耗时工作,此插件可在其他项目中单独使用。
- 合理的拆分，拥有众多的可复用模块，开箱即用
- 高可用注册中心
- 高可用配置配置管理中心，通过`rabbitmq`支持配置刷新
- 服务网关
- 监控
- 基于oauth2，jwt的认证中心。ouath2服务提供商
- 用户中心
- 权限管理中心
- 拥有配套的后台管理界面[ms-admin-ui](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e79fd7ccedb79b4db69822835f7636f35a359d712078963f752025963a3456a5f) 
- 支持docker容器部署
- 使用flume收集系统日志，便于日志分析
- 热点数据使用redis缓存
- 多数据源支持
- 完善的项目使用文档
- 用心的开发者
## 整体技术选型
技术名称 | 版本 | 技术使用 | 地址
------- | ------- |------- |-------
jdk | 1.8.0_144 | java开发环境 | [官网](http://u.720life.cn/g/0832d3c13dcf440b8c2ddd37014597194dfce0f4546bd12c9ba469d981d9d729007ebfc8068b2baf5cdf0064d40d499934723df973302be9e8c27d1f120dec7b61925cc8b32fdf9fad630e04fa8fd7113a88a9e0124d4693294d63423a2f8c73) 
mysql | 5.7 | 关系型数据库 | [官网](http://u.720life.cn/g/1bf70074d92aadd1ef623e94b2eb0ed00c365aa66125b83131d4712ec0355b40) 
redis | 3.0.6 | 缓存数据库 | [官网]https://redis.io/download,[中文站]http://www.redis.cn/
maven | 3.3.9 | 项目管理工具 | [官网](http://u.720life.cn/g/bc840264f6cc23df0a8935b6f2922fec747e8988e9d6774b642901b9662b323f) 
docker | 1.12.6 | 容器技术 | [官网](http://u.720life.cn/g/d13d2b0ef4a5c92b4f4a6e9ed4270e65b90c4c1e1b506e1a501feef81ad769e9) 
flume|1.8.0| 系统日志收集|[官网](http://u.720life.cn/g/4c1357133cd13004eecbc026c61a59f5afb7e23e1fda1abbf9b7d6ccee3161f3) 
rabbitmq|3.7.2| 消息总线|[官网](http://u.720life.cn/g/f11a52769f38ad92f85e2ee51efef5a9dff40da7cdfe02ae803fb47f6d36c7b5) 
elasticsearch|6.1.2|日志分析引擎|[官网](http://u.720life.cn/g/de3742c0ac7bbef6b8feb3a0318f0771d8069a877016758cbc2f60ad4f590110867a0e483bf957b2b5d88abbbc157ac4) 
fastdfs| 5.11 |分布式文件存储|[官网](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d00820f799868fd9afbf99f9fa8c150e2b3f8d8c0a394513ed08b836db28783d) 
springBoot | 1.5.9.RELEASE | 微服务入门框架 | [官网](http://u.720life.cn/g/a69280274c25b74186181776a3e0de85eb1603863f68213faebf4f8c02d3a35914615e6c2e48843223cc4089b9dc5392) 
springCloud | Edgware.RELEASE | 微服务框架 | [官网]http://projects.spring.io/spring-cloud/,[中文文档]https://springcloud.cc/
mybatis | 3.4.4 | 数据持久化框架 | [官网](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a215e4d93221eb26b660bea25686b89be63142caf406b6e1c14d3ab51db921e10ca) 
mybatis-generator | 1.3.5 | mybatis代码生成 | [github地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304602d75ec6f7ef29bab0759c73f5fdf49997b16c203063ed2ad9d38fb1be612af0) 
mybatis-pagehelper | 4.1.0 | mybatis分页插件 | [github地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e46d295ad2841af2558737b9b48e7f525f5d9e37bc321a699ae434b02ff50941) 
nodejs |v8.4.0 | web项目开发,静态资源http服务器 | [官网](http://u.720life.cn/g/6dd25ec2eceebbb6348ad519a7343cbc870e0686893d09c2c96407c7d32e10b3) 
npm | 3.10.7 | nodejs模块管理工具 | [官网](http://u.720life.cn/g/920c024f0b8c5aa5e32c4f88af4e6c963ac4e53f8a43f7c3d25154209847e9d0) 
vuejs | 2.5.2 | 前端视图框架| [官网](http://u.720life.cn/g/1eea7f654038e3466b5f7afd82540e026fb743de569442ae210ad68342f4d930dce673a23775917ccef48a4cec35d806) 
vue-router | 3.0.1 | 前端路由 | [官网](http://u.720life.cn/g/7bedfe02707a57b283aa65bf169b40686452cfedd97435d81c67927328a3271f) 
vuex| 3.0.1 | 单向数据流 |  [官网](http://u.720life.cn/g/acea3f53396a46112876052cae0a3648d9ec2e30c8a052662732ee7eaa3312bf) 
axios| 0.17.1 | ajax请求框架 | [github地址](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304638015ac6a54b1cadf0934b8a0d5637d0) 
elemnet-ui | 2.0.8 | 前端视图库 | [官网](http://u.720life.cn/g/99b90101e0edb43e4fb6c26272a617e68663cc65b086687fa23d692ae5a71460f46c41bd5e556a5c80e1411639f231fc61da3a12304b84df873a8ab63ca1c524) 
swagger | 2.6.1 | 文档生成 | [官网](http://u.720life.cn/g/144fc7dac4f8956d4599e1fe5c1bbcf883c55dd9d71a04eb7bc64e107270e142) 
lombok | 1.16.6.1|代码工具|[官网](http://u.720life.cn/g/9cec729ef2d3c72b70f7caf7a64fe54cd6e706641e9b2936105b4a7807fccbb3d1764fb20116c23a69ff357203ad9890) 
ratelimit|1.4.0|网关限流|[github](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e58bed8c9044c252a16c30c3737f7859764721417ccdc344eca4861553c211fea7349f7476957df2400e99b7e066a91) 
## 开发界面
![](./all/ms/idea.png)
## 模块介绍
``` lua
micro-fast
├── boot-starter -- 借助spring boot自建快速启动项目
|    ├── boot-starter-common -- ms系统的通用模块
|    ├── boot-starter-elasticsearch -- elasticsearch快速启用
|    ├── boot-starter-fastdfs-client -- fastdfs客户端
|    ├── boot-starter-maven-plugin -- maven的一系列插件
|    |    └── mybatis-generator-extend-maven-plugin -- 用于简化mybatis-generator生成代码的流程
|    ├── boot-starter-security-oauth -- 权限认证　
|    ├── boot-starter-ssm  -- ssm公共配置
|    └── boot-starter-util -- 常用工具
├── ms -- 分布式系统
|    ├── config-server -- 配置管理中心
|    ├── gateway  -- 服务网关
|    ├── monitor-turbine-- 请求监控
|    ├── monitor-zipkin-- 服务调用监控
|    ├── oauth -- 认证中心
|    ├── register-center1 -- 高可用注册中心
|    ├── register-center2 -- 高可用注册中心
|    ├── ucenter  -- 用户中心
|    └── upms  -- 权限管理系统
├── ms-web -- 业务系统界面搭建示例
└── all-in-one -- ms系统的集中式实现
```

## ms分布式系统架构图
![](./all/ms/架构图.png)
## 登录
![](./all/ms/login.png)
## 首页
![](./all/ms/index.png)
## 系统管理
![](./all/ms/system.png)
## 组织管理
![](./all/ms/organization.png)
## 用户管理
![](./all/ms/Upmsuser.png)
## 权限管理
![](./all/ms/permission.png)
## 角色管理
![](./all/ms/role.png)
## 服务简单信息查看
![](./all/ms/serviceInfo.png)
## 服务详细信息查看,服务状态管理
![](./all/ms/serviceManage.png)
## swagger系统文档聚合
![](./all/ms/swagger.png)
## 监控中心
![](./all/ms/monitor.png)
## 服务调用追踪
![](./all/ms/zipkin.png)
## 热门服务实时排行
![](./all/ms/serviceRank.png)
## 各模块的详细介绍
- `boot-starter`项目介绍[README.md](boot-starter/README.md)
- `ms`项目介绍[README.md](ms/README.md)
- `ms-web`项目介绍[README.md](ms-web/README.md)
- `all-in-one`项目介绍[README.md](all-in-one/README.md)
 




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)