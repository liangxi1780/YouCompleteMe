# zscat_sw
springboot dubbo redis solr mq kafka 商城 blog cms
 qq群 483681368
 
zscat


- ├── sw-common -- SSM框架公共模块
- ├── dubbo-cache-starter -- dubbo缓存插件
- ├── app-monitor --dubbo服务监控和统计
- ├── sw_manager -- 后台管理模板
- ├── sw-portl -- 官网门户展示
- ├── sw-search-- search管理系统（实现了luence，solr两种搜索）
- |    ├── search-api -- search相关的service
- |    ├── search-service -- search相关的service实现  dubbo服务
- |    ├── search-web -- search消费者 前端展示
- ├── sw-blog-- blog管理系统
- |    ├── blog-api -- blog相关的service
- |    ├── blog-service -- blog相关的service实现  dubbo服务
- |    ├── blog-web -- blog消费者 前端展示
- ├── sw-cms-- cms管理系统
- |    ├── cms-api -- cms相关的service
- |    ├── cms-service -- cms相关的service实现  dubbo服务
- |    ├── cms-web -- cms消费者 前端展示
- ├── sw-shop-- shop管理系统
- |    ├── shop-api -- shop相关的service
- |    ├── shop-service -- shop相关的service实现  dubbo服务
- |    ├── shop-web -- shop消费者 前端展示
- |    ├── shop-h5-- h5消费者 前端展示

1.项目部署，根据doc目录下的 zsboot.sql，weixin.sql，分别创建数据库，相关数据库配置 参考application.properties
先安装 spring-boot-starter-dubbo模块到本地
### 2.blog模块为例  



- a.启动blog-services下面的BlogServiceApplication主类，启动blog的dubbo服务
- b.启动blog-web下面的BlogWebApplication主类，访问 http://localhost:2001/front/blog/indexs
### 3.cms模块为例 
 


- a.启动cms-services下面的cmsServiceApplication主类，启动blog的dubbo服务
- b.启动cms-web下面的cmsWebApplication主类，访问 http://localhost:2001/web/cms/index http://localhost:2001/wap/cms/index
### 4.shop模块为例  



- a.启动shop-services下面的ShopServiceApplication主类，启动blog的dubbo服务
- b.启动shop-web下面的ShopWebApplication主类，访问  http://localhost:2007/front http://localhost:2007/youhong
- c.启动shop-h5下面的ShopWebApplication主类，访问 http://localhost:2006/wap1 
### 5.search模块为例
  


- a.启动search-services下面的SearchServiceApplication主类，启动blog的dubbo服务
- b.启动search-web下面的SearchWebApplication主类，访问 http://localhost:2008
### 6.启动sw_manager下面的 GunsApplication主类，访问 http://localhost  admin  111111
### 7.启动sw_portl下面的 PortlWebApplication主类，访问 http://localhost:2009/index



- [搜索模块具体介绍](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844da5e65fc0e5b04545f569a1a81f014b7da75d2c52acbe42c681aba5e3bf19b7c69001516c987b72c4e844f5703105827f26cd0abcc3a73f77c3754e3a999416cb) 
- [后台管理具体介绍](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844da5e65fc0e5b04545f569a1a81f014b7d5b67c2a1eaa898815e5463a2c530d9fd1b622ae07dd183d4fed40244024ebb939f22fdc946654bfd38f791947a7d82fc) 
- [blog管理具体介绍](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844da5e65fc0e5b04545f569a1a81f014b7d5b67c2a1eaa898815e5463a2c530d9fd0ea095e67fab727c916e452097be868426ac3a510d88b2db16512badb03d1916) 
- [cms管理具体介绍](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844da5e65fc0e5b04545f569a1a81f014b7d5b67c2a1eaa898815e5463a2c530d9fd4dca0e0bd24d4e34002dd7d08b417da73105430d7767354c32cb69f270907e4c) 
- [商城管理具体介绍](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844da5e65fc0e5b04545f569a1a81f014b7d5b67c2a1eaa898815e5463a2c530d9fdef7bb51ac52f0f34164edce98f820c2880a7de1f9790e9861bb4a2591e085b28) 

请作者喝杯咖啡

![输入图片说明](https://git.oschina.net/uploads/images/2017/0829/203712_6694b4c1_134431.jpeg "weixin.jpg")
![输入图片说明](https://git.oschina.net/uploads/images/2017/0829/203723_5567bd56_134431.jpeg "alipay.jpg")


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)