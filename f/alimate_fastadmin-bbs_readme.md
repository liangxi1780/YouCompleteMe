
### FastAdmin-Bbs 基础FastAdmin开发的超简单的简易留言板、博客、论坛，适用于快速入门FastAdmin。


 **更新首页 前台统一增加了基于FastAdmin的头部模板调用 -后台增加了独立模块调用创建示例** 

 **截至12课的视频课-博客演示** 

![截至12课的视频课-博客演示](https://images.gitee.com/uploads/images/2018/1105/113327_160da720_1022917.png "截至12课的视频课-博客演示")


 **截至13课的视频课-留言板演示** 

![截至13课的视频课-留言板演示](https://images.gitee.com/uploads/images/2018/1105/113425_833e178d_1022917.png "截至13课的视频课-留言板演示")


### 技术选型-参考表

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
Netty-socketio | 实时推送  | [https://github.com/mrniko/netty-socketio](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046329403df04bc1395136dfa28cc1cbe82c275790c76a049fbbf12df45f90ebd9d) 

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
socket.io.js | SocketIO插件  | [https://socket.io/](http://u.720life.cn/g/d1d2c4e50f3a95a3fbf9a01af462df22da6dbfe07be14fbffefa967004de5701) 



FastAdmin是一款基于ThinkPHP5+Bootstrap的极速后台开发框架。
===============


## **主要特性**

* 基于Auth的权限管理系统
    * 支持无限级父子级权限继承，父级的管理员可任意增删改子级管理员及权限设置
    * 支持单管理员多角色
    * 支持管理子级数据或个人数据
* 强大的一键生成功能
    * 一键生成CRUD,包括控制器、模型、视图、JS、语言包、菜单等
    * 一键压缩打包JS和CSS文件，一键CDN静态资源部署
    * 一键生成控制器菜单和规则
    * 一键生成API接口文档
* 完善的前端功能组件
    * 基于AdminLTE二次开发
    * 基于Bootstrap开发，自适应手机、平板、PC
    * 基于RequireJS进行JS模块管理，按需加载
    * 基于Bower进行前端组件包管理
* 强大的插件扩展功能，在线安装卸载升级插件
* 通用的会员模块和API模块
* 共用同一账号体系的Web端会员中心权限验证和API接口会员权限验证
* 二级域名部署支持，同时域名支持绑定到插件
* 多语言支持，服务端及客户端支持
* 强大的第三方模块支持(CMS、博客、文档生成)
* 整合第三方短信接口(阿里云、创蓝短信)
* 无缝整合第三方云存储(七牛、阿里云OSS、又拍云)功能
* 第三方富文本编辑器支持(Summernote、Tinymce、百度编辑器)
* 第三方登录(QQ、微信、微博)整合
* Ucenter整合第三方应用

## **安装使用**

https://doc.fastadmin.net

## **在线演示**

https://demo.fastadmin.net

用户名：admin

密　码：123456

提　示：演示站数据无法进行修改，请下载源码安装体验全部功能

## **界面截图**
![控制台](https://gitee.com/uploads/images/2017/0411/113717_e99ff3e7_10933.png "控制台")

## **问题反馈**

在使用中有任何问题，请使用以下联系方式联系我们

交流社区: https://forum.fastadmin.net

QQ群: [636393962]https://jq.qq.com/?_wv=1027&k=487PNBb交流群① [708784003]https://jq.qq.com/?_wv=1027&k=5ObjtwM交流群② [696992864]https://jq.qq.com/?_wv=1027&k=5R2AB00高级群,付费加入

Email: (karsonzhang#163.com, 把#换成@)

Github: https://github.com/karsonzhang/fastadmin

Gitee: https://gitee.com/karson/fastadmin

## **特别鸣谢**

感谢以下的项目,排名不分先后

ThinkPHP：http://www.thinkphp.cn

AdminLTE：https://adminlte.io

Bootstrap：http://getbootstrap.com

jQuery：http://jquery.com

Bootstrap-table：https://github.com/wenzhixin/bootstrap-table

Nice-validator: https://validator.niceue.com

SelectPage: https://github.com/TerryZ/SelectPage


## 版权信息

FastAdmin遵循Apache2开源协议发布，并提供免费使用。

本项目包含的第三方源码和二进制文件之版权信息另行标注。

版权所有Copyright © 2017-2018 by FastAdmin (http://u.720life.cn/g/7ad79292b33ff5c78f6f81f99017d21ce4547250cadb331c6c2b150d2a46b920) 

All rights reserved。


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)