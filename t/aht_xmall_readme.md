# XMall
[![AUR](https://img.shields.io/aur/license/yaourt.svg)](https://github.com/Exrick/xmall/blob/master/License)
[![](https://img.shields.io/badge/Author-Exrick-orange.svg)](http://blog.exrick.cn)
[![](https://img.shields.io/badge/version-1.0-brightgreen.svg)](https://github.com/Exrick/xmall)
[![GitHub stars](https://img.shields.io/github/stars/Exrick/xmall.svg?style=social&label=Stars)](https://github.com/Exrick/xmall)
[![GitHub forks](https://img.shields.io/github/forks/Exrick/xmall.svg?style=social&label=Fork)](https://github.com/Exrick/xmall)
### [宣传视频](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a975755db42cd94e8c8e680895eca0c9b51) 
- 作者亲自制作 可接单做视频... 视频已上传至[B站](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a975755db42cd94e8c8e680895eca0c9b51) 
### 项目已部署，在线Demo
- 前台商城：http://xmall.exrick.cn/
- 后台管理系统：http://xmadmin.exrick.cn/
- 此项目将作为作者2018本科毕业设计，单体系统版本(一台tomcat可运行)以及详细文档后续放出
### 前台页面为基于Vue的独立项目 请跳转至 [xmall-front](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ffc8901a7640f779c6263e902647077c39e912e347a500f2bc472e73e458577f)  项目仓库查看
### 开发中，敬请期待！
- Spring Cloud版
    - [X-Cloud](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046120bf27eb9d851fee2126e630f5040f45e86a8507c9a4d0ee8d21f76954d4015)  框架开发中
- 微信小程序APP 
    - 捐赠≥19.9可加群私聊群主提前下载前台源码 [预览视频](http://u.720life.cn/g/cbad280c284c0afc32b549dc6e61524e7b5a28c21a3c86b889c69476b9042f8ff0c3b9576ba3ffd284b8e1936a8f8f1b) 

    ![](http://oweupqzdv.bkt.clouddn.com/%E5%B0%8F%E7%A8%8B%E5%BA%8F%E9%A2%84%E8%A7%881.png)

- XMall开放平台(仿微信开放平台)

    ![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171231172014.png)
### 基于SOA架构的分布式购物电商商城
- [x] 后台管理系统：管理商品、订单、类目、商品规格属性、用户、权限、系统统计、系统日志以及前台内容等功能
- [x] 前台系统：用户可以在前台系统中进行注册、登录、浏览商品、首页、下单等操作
- [x] 会员系统：用户可以在该系统中查询已下的订单、管理订单、我的优惠券等信息
- [x] 订单系统：提供下单、查询订单、修改订单状态、定时处理订单
- [x] 搜索系统：提供商品的搜索功能
- [x] 单点登录系统：为多个系统之间提供用户登录凭证以及查询登录用户的信息

### v1.1更新日志(需更新前后台代码及SQL)
- [x] 接入[XPay支付系统](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046336d47cc5a778493ecb22d7d19989437) 
- [x] 更新Dubbo(2.6.1)、ES(6.2.3)等依赖版本
- [x] 取消ES需在页面中配置及跨域问题，ES默认配置集群名改为原elasticsearch
- [x] 修复后台统计热卖商品SQL错误，xmall-front-web模块支持SpringMVC文件上传配置
- [x] 修改金额字段类型优化SQL与备注
- [x] 优化后台页面
- [x] 修复用户修改BUG
- [x] 优化批量删除
- [x] 优化商品分类添加
- [x] 重构首页，后台可配置，包括3D轮播图
- [x] 新增缓存管理功能菜单
- [ ] 完成订单打印发货等功能
- [ ] 完成SKU设计
- [ ] 增添报表

...

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171119130819.jpg "登录界面")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022174034.jpg "后台首页")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022224322.jpg "商品管理")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022225418.jpg "管理员编辑")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022183906.jpg "前台首页")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171109215656.jpg "ES分词搜索")

### 前端所用技术
- 后台页面【新 待开发】
    - [ANT DESIGN PRO]https://pro.ant.design/index-cn)：蚂蚁金服开箱即用中台前端
    - React + dva + G2 + ANTD + ES2015+
- 后台页面【旧】
    - 感谢 [H-ui]http://www.h-ui.net/、[FlatLab]https://github.com/Exrick/xmall/blob/master/study/FlatLab.md 提供静态页面支持
    - [Ztree]http://www.treejs.cn/v3/main.php#_zTreeInfo)：jQuery树插件
    - [DataTables]http://www.datatables.club/)：jQuery表格插件
    - [Layer]http://layer.layui.com/)：web弹层组件
    - [Distpicker]https://github.com/fengyuanchen/distpicker)：中国省市区地址三级联动插件
    - [KindEditor]https://github.com/kindsoft/kindeditor)：富文本编辑器 简洁方便 没UEditor那么多坑
    - [WebUploader]http://fex.baidu.com/webuploader/getting-started.html)：百度文件上传插件
    - [HighCharts]http://www.hcharts.cn/)：图表库
    - [不蒜子](http://u.720life.cn/g/579e1d658192662da38f39ca1c82cd9d7584a1d3a88d55093ae0b232f0281753fd60f99c4bd38a0b305d23ff4b1f87941fa7b39f369541140844955c3113aadc 
- 前台页面
    - 详情请跳转至 [xmall-front](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ffc8901a7640f779c6263e902647077c39e912e347a500f2bc472e73e458577f)  项目仓库
    - 感谢 [yucccc](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cd7017a4f1aa1f7d34b7a3c3cee04ce4)  的开源 [vue-mall](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046972527ba0da1295bf647a094e05ea6bd1e24e4d1f8ba19c2f56965bef13b40ec)  项目提供前端页面及框架支持
    - Vue2 + Vuex + Vue Router + Element UI + ES6 + webpack + axios + Node.js
    
### 后端所用技术
##### 各框架依赖版本皆使用目前最新版本 可进入xmall-parent中 [pom.xml](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767e0247cc1d6f1e2a45ac070b78a317e82f7937a9050e4738d56ed4a0cb2ec0212)  查看
- Spring
- [SpringMVC](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767b84b880ad658a76463126efd4ccd71f2c4ed4c5a5eea8ca101295c46370386fd) 
- MyBatis
- [Dubbo](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767b84b880ad658a76463126efd4ccd71f2e916ebb2bfd182960ceac4406ff54aac) 
- [ZooKeeper](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767b84b880ad658a76463126efd4ccd71f2787d7e873305f32bcadaf0ba5b526f7a) 
- MySQL
- Mycat：数据库分库分表中间件
- [Redis]https://github.com/Exrick/xmall/blob/master/study/Redis.md)：缓存
- [Elasticsearch]https://github.com/Exrick/xmall/blob/master/study/Elasticsearch.md)：基于Lucene分布式搜索引擎
- [ActiveMQ]https://github.com/Exrick/xmall/blob/master/study/ActiveMQ.md)：消息队列
- [Druid]http://druid.io/)：阿里高性能数据库连接池
- Shiro：安全框架
- [Swagger2]https://github.com/Exrick/xmall/blob/master/study/Swagger2.md)：Api文档生成
- Docker
- [Nginx](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767b84b880ad658a76463126efd4ccd71f217fccfa33970fe39769d484342462181) 
- Tomcat
- [Maven](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767b84b880ad658a76463126efd4ccd71f294ce774a01a7afebfc6d8e8c13a28e51) 
- 第三方SDK
    - [七牛云文件存储服务](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b148468fe5a337933ee3e4dc0c976e35a408defe5fa513b350774ea0a7747ec0d3d10) 
    - [极验Test-button人机验证码](http://u.720life.cn/g/af1e222ff94b66580ad482e7c89c63f91645bbf5d51ed1f9acc1543666ad2a900dcb96a46c593fa1254958318280eaec) 
- 第三方插件
    - [hotjar]https://github.com/Exrick/xmall/blob/master/study/hotjar.md)：一体化分析和反馈
    - [搜狐畅言评论插件](http://u.720life.cn/g/fb2586c4ecb6075c88b852d82c275a2f765488c6bebaee1c88d0054ab37d3070) 
- 第三方接口
    - [Mob全国天气预报接口](http://u.720life.cn/g/30a395c9d5c18eaca077813853a1c8b54407882ed34a6e3d97c3bfb2b8a977c7a12e7f82b8e245c4f295489e28b86fe3) 
- 其它开发工具
    - Jenkins：持续集成
    - [JRebel]https://github.com/Exrick/xmall/blob/master/study/JRebel.md)：开发热部署
    - [阿里JAVA开发规约插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046eee1f37ed667d08f5c30df231e894fa2) 

### 文件说明
- `xmall` 文件夹提供部分依赖与sql文件
    - xmall.sql：数据库文件
    - dubbo.xsd：需手动配置避免报错
    - redis-3.0.0.gem：Redis集群搭建所需Ruby库
- `generatorSqlmapCustom` 文件夹为 [Mybatis Generator](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a21a07057a36d6ca5ea426a94333449b8eea33deea4240609df5d516aef06832784)  逆向生成工具，且已配置好maven插件
### 本地开发运行部署
- 下载zip直接解压或安装git后执行克隆命令 `git clone https://github.com/Exrick/xmall.git`
- 安装各中间件并启动：[ZooKeeper]https://github.com/Exrick/xmall/blob/master/study/Zookeeper.md、[Redis]https://github.com/Exrick/xmall/blob/master/study/Redis.md、[ActiveMQ]https://github.com/Exrick/xmall/blob/master/study/ActiveMQ.md、[Elasticsearch]https://github.com/Exrick/xmall/blob/master/study/Elasticsearch.md
- 修改各配置文件相应依赖IP配置(默认本地127.0.0.1)，以及七牛云、极验配置在 `xmall-common - utils` 中找到修改，XPay邮箱配置在 `manager-service与sso-service` 中
- [Maven安装和在IDEA中配置](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767b84b880ad658a76463126efd4ccd71f294ce774a01a7afebfc6d8e8c13a28e51) 
- 使用IDEA([破解/免费注册](http://u.720life.cn/g/a951c120f3b4383a914a3c153183e0ac36630217d723a80f0d4836df3a2d9dc6)  `File-Open` 直接打开xmall项目，点击右下角 `Import Changes` 等待安装完依赖即可
- MySQL数据库新建 `xmall` 数据库，运行sql文件，注意在有 `db.properties` 的模块中修改你的数据库连接配置
- 按照依赖顺序分别在每个模块文件夹根目录执行 `mvn install` 命令
- 项目需运行除 `xmall-parent` `xmall-common` 以外其它所有6个服务，且都已配置好Tomcat插件, 执行命令 `mvn tomcat7:run` 或在IDEA中使用插件(`View - Tool Buttons - 右侧菜单Maven Projects - tomcat7 - tomcat7:run`)运行即可，当然可自行配置
- 后端管理系统默认端口8888 http://localhost:8888 管理员账密admin|123456
- 前端项目接口默认端口7777 前台页面请启动基于Vue的 [xmall-front](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ffc8901a7640f779c6263e902647077c39e912e347a500f2bc472e73e458577f)  项目，并修改其接口配置
### 技术疑问交流
- 给作者项目Star或捐赠后可加入交流群 `475743731`，还可免费获取最新源码和 [UI框架](https://github.com/Exrick/xmall/blob/master/study/FlatLab.md) [![](http://pub.idqqimg.com/wpa/images/group.png)](http://shang.qq.com/wpa/qunwpa?idkey=7b60cec12ba93ebed7568b0a63f22e6e034c0d1df33125ac43ed753342ec6ce7)
- 作者博客：[http://blog.exrick.cn](http://u.720life.cn/g/d9facb80ece1075627c5e84d9677b2c19a52006991cae3006c3cacccaf404d77) 
### 捐赠
![](http://oweupqzdv.bkt.clouddn.com/FgwHSk1Rnd-8FKqNJhFSSdcq2QVB.png)




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)