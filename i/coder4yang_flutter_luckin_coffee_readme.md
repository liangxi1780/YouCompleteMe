![app_head](./readme/images/githead1.png)

# flutter_luckin_coffee

> flutter luckin coffee application（仿瑞幸咖啡）

## 目录

- [前言](#前言)
- [flutter版本信息](#flutter版本信息)
- [扫码下载体验](#扫码下载体验)
- [安装](#安装)
- [相关插件](#相关插件)
- [待完善](#待完善)
- [近期计划](#近期计划)
- [维护者](#维护者)
- [欢迎PR](#欢迎PR)
- [预览](#预览)

## 前言

Q：为什么会有这个项目？

> 了解到了flutter这个框架，并且和rn和uniapp的实现跨平台的思路完全不一样。做了一些demo之后，感觉挺有意思的，所以想做一个完整的项目，体验学习一下。

Q：为什么用luckin coffee？

> luckin coffee在网上能搜索到开源的原型+设计图,简直方便的不行。[luckin coffee原型+设计图](http://u.720life.cn/g/71446ccd22fdeaf0c6064fec8055bb32196593ee2460c419c53eb848cd5d844473f29819806fc0dba540ac835cb9a9d38783301a2a1f60dffeee9b1a7f2a8a5c184c992bb0896bd4f0f3db24e353a8d1) 

Q：数据从哪里来？

> [api工厂]https://www.it120.cc/?referrer=18046)配置商城数据，网站提供接口。

## flutter版本信息

``` sh
flutter --verison
```

``` sh
Flutter 1.9.1+hotfix.6 • channel stable • https://github.com/flutter/flutter.git
Framework • revision 68587a0916 (7 weeks ago) • 2019-09-13 19:46:58 -0700
Engine • revision b863200c37
Tools • Dart 2.5.0
```

## 扫码下载体验

密码：meetqy

![](./qrcode.png)

> 没有安卓机，只在虚拟机上面测试过，有bug欢迎提issues。

## 安装

这个项目使用 [flutter](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a3d53dc14c00de9f3fbb6f9540207347c8a6e1c6d7d72ab2e88ede2e31c7e858  请确保你本地安装了它们。

1. 检查版本号是否正确
```sh
flutter --version
```

2. 运行一下命令查看是否需要安装其他依赖
``` sh
flutter doctor
```

3. 运行启动
```
flutter pub get
flutter run
```

## 相关插件

插件 | 说明
---- | ----
[flutter_swiper](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469c726917dae2d5b57035fa1efe682ea9ed670e12fb941a27d4773263e0da5abe)  | 轮播图
[provider](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304657812d22408971f4e401a8be5cbc921ec2985cf9ff3b062eaf69535991bf684e)  | 状态管理
[pull_to_refresh](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e2096c8696610e61a4037c8bf970010696324fef23328b1cbb838252cd6c808)  | 上拉加载，下拉刷新
[dio](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e8c8d669b02a5a6af4e98a728ab494d45189cee03f6f8d843a032b59f800ad43)  | 网络请求
[json_annotation](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461d7fb0ce9040fb59a7272f13c0a972406c67b703660c4017d73b519242dfbec5feea554be7910079a14a14856d3ca18d53e6debd12ac6ad2ada9e3bdb2495214f81c93221b512352222b24c0227add9c88abb4c28e6abec4dafaed5dc4e0ef5555b804814a48544e71a48b61280091efd113ff7453284046bb53d4b72446c324)  | json序列化
[fluttertoast](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ee3873dafab90e4d57447da1d5e5512bf46efd9faec2e8d9da4e8f8b105a252f)  | toast
[shared_preferences](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464f476ff75e2536ca34b0e410629ed3362cdd918977a70d959ebf889d5672318d23f074340e49dfe1132ffc6ebb539c6617bbd6e5e97e6d7f44a4cef358ff692f)  | 本地缓存
[iconfont_dart](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469639e7d841209b0e25293d630c4884ffb23713af6f054b8ba32ea859b8dde732)  | 快速将iconfont生成项目中可以直接调用的icon
[color_dart](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a66254cf2bb9b16aac3e17efc29829944d634c74845920f8a4e3296be224dcbf)  | 配合vscode插件在代码中显示颜色

## 待完善

- [ ] 菜单页面锚点功能未实现
- [ ] 代码不符合开发规范（进行中...）
- [ ] 订单模块联调
- [x] 新增用户管理模块

## 近期计划

- [x] 重构request模块
- [x] 新增邮箱注册页面
- [x] 新增邮箱登录页面
- [x] 新增邮箱登录联调
- [x] 新增邮箱注册联调
- [ ] 订单页面联调
- [ ] 重构自定义appbar
- [ ] 重构components（进行中...）

## 版本日志

- [v1.x.x](./readme/backlog/v1.x.x.md)
- [v2.x.x](./readme/backlog/v2.x.x.md)

## 维护者

[@meetqy](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e18b608d7a9919389793db9da6a770a 

## 欢迎PR

非常欢迎一起学习flutter! [提一个Issue](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c8436850d06b3ede677ae3433b3176df9367cd8911a9f7f4129450a08626b586729916d4cf0bba58aa16f92105fceaa)  或者提交一个 Pull Request.

## 预览

  |   
---- | ----



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)