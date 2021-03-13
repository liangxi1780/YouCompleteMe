#概述
1.	本工程是[archer-framework]http://git.oschina.net/ArcherGroup/archer-framework)，以[archer-application-core]http://git.oschina.net/ArcherGroup/archer-application-core)提供的API为数据来源的一套后台管理系统。
2.	本工程只负责界面展现。

#界面截图
![菜单管理](/snapshot/menu.png "菜单管理")

![角色列表](/snapshot/role.png "角色列表")

![角色详情](/snapshot/roleDetail.png "角色详情")

# 相关项目
| 名称           | 说明            |
| ------------- |-------------|
| [archer-framework](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d142b63ca205aeeeda84860ae4bd752dfd8f7eca758981e8332b3f34ce340ae937b71759310c19d6d0e40324734dd46de)         | `archer-framework`是一个旨在构建RESful风格WEB服务的轻量级框架        |
| [archer-application-core](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d142b63ca205aeeeda84860ae4bd752df8ffaa2050357da14565dcfa4254001fe75bf43a40bf8936bb151469c22c33926)         | 使用`archer-framework`做的服务工程演示，一个简单的用户角色权限管理系统，对外只提供API        |

#  主要技术
-	css：`bootstrap` `AdminLTE`
-	js: `vue` `jquery`


# 如何启动
1.	本工程依赖于`archer-framework`,所以请先install `archer-framework`
2.	本工程依赖于`archer-application-core`提供的接口，所以请先启动`archer-application-core`工程
3.	运行`test/DevelopmentStarter.java`启动整个工程。
4.	使用admin/123456用户登录
5.	enjoy :)

# 常见FAQ

> IE兼容性如何？
>> 因为这是后端管理系统，采用的是`vue`，而`vue`支持IE9+，所以该工程也支持IE9+。

> 为什么选用`vue`而不是`angular`？
>> `vue`简单易用，且`angular2`尚未正式发布。

>我在使用中发现了bug，我要如何报告这个bug？
>> 你可以在git上提交issue，说明问题的现象，错误日志等，我们会在第一时间予以排查和修复。


#	特别鸣谢
- [AdminLTE](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469938d875cf47e5488f379f965eb2a0745e6b8f3c0029e0f6d8e8db173b9167bf)    极好的bootstrap的后台管理界面皮肤

- [vue.js](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a66c77cd0911e5527fb3fc591bfc25f5)  国人参与的MVVM js库，确实比angular.js简单

- [bootstrap-table](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f2f423513f085635331b1265a6816cdb36af265fd434a72654ac1ef575ab42cc)  国人写的table组件，最近还有vue版本出现，个人觉得比datatables简单易用


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)