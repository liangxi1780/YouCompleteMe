# goman

A web app like postman

# 已发布平台(go1.9.x编译)

web版，可以使用chrome等浏览器，拥有更好的体验

 * [goman.v0.3.1.web-win.zip 5.6MB (码云源)]http://u.720life.cn/g/635c1cf934c36e281ac63ed53d0962e99a1c90c91bb35531977a24a7987e06c17045ead2a8f0f862a948f127cc9fe0bfa1ac0a40c27ca9383dfe40502c97e1996702c254ff91d0278d412266500ad3e695b459cf357a3db0a7d5d4ae0155c3bc69d9bc7eaf707f3977724fe76ba6ee643419fce55ffbfee2ef511a74913bb6fc285900796048440a2a9db3483799eb60af7bafbc73191e7e820e3746b90ef35498629e47a59864556c6a6630e99745eea5a7fd4c09e8494e7ce2fb2197e56856d779c2bddb780986577e32d828b3d97fb95799be844d172b51802fbee9e9c23aa13a14647ad6914e2a9f656def8056e606014f4cb726cbca57e109c715e582afa1b7b0087e4b693ab4dd978e172317ff) 

 * [goman.v0.3.1.web-mac.tar.gz 6.3MB (码云源)]http://u.720life.cn/g/635c1cf934c36e281ac63ed53d0962e99a1c90c91bb35531977a24a7987e06c17045ead2a8f0f862a948f127cc9fe0bf923e29055f70cdc295eefbc6c722f68e6835f3bcb8e067568451b230f53671584db31888e0a81d9aa4831216f30e5913251b65afb8fdccdd7da3a982616dd3a766c5030edcd86246a0401ed4a158e13f3e8353c3d1a36f81a8a42db60ba1495f362ff68f47eb5dbdd35d465375715d5cb63f1456616dbee1588875b00c71ae9c9ac2520595d650fc8ef2c360999cb4f141f7c741bec834f1d8505f1e4fdd4b4069e5e2d06658eb3e9d36edff1365f42e0d46ed18f278025bb0666a4d07a58b29b1cd18d0e630ff5d983c4ac72d2367ca6654da2257a4907365f5244a008d7ef3) 

app版，独立运行，更简洁，但有些限制

* [goman.v0.3.1.app-win.zip 5.6MB (码云源)]http://u.720life.cn/g/635c1cf934c36e281ac63ed53d0962e99a1c90c91bb35531977a24a7987e06c17045ead2a8f0f862a948f127cc9fe0bf91fd62a27678e7ba34b3152ad7e657e8dde47cabf73da50a346346f6f8492287c50436ca3719f97dfd42cd90edb392efc799f5dd327b254193f1e7e8b2dd450035ed443b2001586c3bed60e2124bf8f95dd48f5b45b4e8177a06b0cabf54d06304fb2550cabc1168a2bb0c3b58de3ffcfefecfe170964d0b18c6d18b25d435c36c93aa75a3b0d65f99e97a83317c6280d7292e64c54e7bbe3c97f370cf95fd6ca472a17608793a46d6c4bed1dcc979062a5f89cadbf5d953fcd846f9f81befeb0badb9fec6a254c8d94713649f9471d8a5946fdbad6d7d348531fd1e274b1933)  (只兼容IE10/IE11内核，请注意升级系统IE浏览器)

* [goman.v0.3.1.app-mac.tar.gz 6.3MB (码云源)]http://u.720life.cn/g/635c1cf934c36e281ac63ed53d0962e99a1c90c91bb35531977a24a7987e06c17045ead2a8f0f862a948f127cc9fe0bf9bdcf6bb6552fb9628e571b254aef6147324cf43fbe02232ee22dfd25efdd35012fc3949503e9b5f41aae7540b8c755066064171345ba2ac68309c9db7bfb802220c5899e6f096344f7967243fa301168979e0fc40d7f7e8ace03a1685096eadc7878c431aa461f96dd2e6e8da0b5092403d11638cd6d13d03cc7232505a7556416392179bd892d7dc6b811cade568f9bcb4de8e192cceb36ad2c9e7afc205510326c9bd348bcfa8dfce81e5925042627f471acc9b594c3a0e83b85ff94ad26ca79c044b1c1cf081c26f128d52c1c41567a5f6bd1233305309b9782a11d496e9)  (已知问题：无法使用复制/粘贴快捷键，但可使用鼠标右键操作)

docker版，更简单的尝鲜使用

* `docker pull zaaksam/goman` 或者指定版本 `docker pull zaaksam/goman:0.3.1`

* `docker run -p 8080:8080 zaaksam/goman`

* 在浏览中打开：`http:127.0.0.1:8080`

注意：docker模式下，goman处在容器内，无法使用 localhost(127.0.0.1) 来请求宿主机的网络资源

# 界面预览

0.3.1版界面相对0.3.0基本没有变化

windows web版

![](https://static.oschina.net/uploads/img/201802/08120715_zvnn.jpg)

macos web版

![](https://static.oschina.net/uploads/img/201802/08120750_hnI4.jpg)

macos app版 (windows版基本雷同)

![](https://static.oschina.net/uploads/img/201802/08120826_tMsb.jpg)

![](https://static.oschina.net/uploads/img/201802/08120851_rVD1.jpg)

# 技术资源

Backend Go + [Beego]http://u.720life.cn/g/4fef179f29be438184ded056121a041d253e5d2bb9741725b3c3a39993dac2389ee4ac97a5d9d0c42167e91afd2570db) 

Frontend Typescript + [Vue]http://u.720life.cn/g/072ec0ff91bc6664c61fa3fb55c1a5237546b1e707277c353b8d0d1d430e58c4)  + [iView]http://u.720life.cn/g/478da2f10b403bf42953fb2ee82c0018b0170844cd8163f832706777b32148e7) 

web版引导界面使用了 [Knockout]http://u.720life.cn/g/34ac88a14f234ff05794f7527d9bab5f6571c7b6447bf158bbbf3989b80d8f95)  + [layui样式]http://u.720life.cn/g/9485a0b8acdeb59e0e8da4fc9f4c161054267375f804d9fe5425706e3674bc94) 

GUI使用了 https://github.com/zserge/webview

请求耗时统计部份参考了 https://github.com/rakyll/hey 代码

# 更新日志

2018-02-09 v0.3.1

* 解决了IE10/IE11的不兼容问题，win app版来了
* 临时解决了mac app版滚动时卡顿问题
* web端心跳包增加了随机数，避免IE缓存
* web端引导页现在不默认打开浏览器了
* web端引导页现在会显示运行的URL地址

2018-02-08 v0.3.0

* 更便捷的web模式运行方式
* web模式下增加了浏览器与应用的互相监测
* docker模式下请求localhost(127.0.01)时会收到警告提示
* app模式建议为实验性质使用
* 简化及增强了各个编译脚本内容

2018-02-03 v0.2.2

* 增加docker镜像编译脚本
* 修改代码支持跨平台条件编译
* 现在访问首页会默认跳往webui地址

2018-02-02 v0.2.1

* 优化构建脚本，更好支持不同平台交叉编译
* 增加不同版本构建main入口

2018-02-01 v0.2.0

* 增加多语方支持，目前支持：简体中文（默认）、英文（不完全）
* 恢复app模式（webview），并默认编译
* 请求支持高级选项模式，可批量请求，并提供统计报告

2017-09-12 v0.1.3

* 拆分webpack为dev、prod环境
* 升级相关依赖项

---

2017-09-10 v0.1.2

* 项目初始化


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)