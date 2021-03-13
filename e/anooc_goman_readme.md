# goman

A web app like postman

# 已发布平台(go1.9.x编译)

web版，可以使用chrome等浏览器，拥有更好的体验

 * [goman.v0.3.1.web-win.zip 5.6MB (码云源)](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e5cb29cf7fdba05c25a9b754b59a6151fa672f8d171d9089cea4c48ca128d1c2897c8f8383edd9b1141a5b2c89a7bd9dd483135ac3556472e840be00e33ef13c3971aa450b476e90c32affd02d6a8f177c5e3c9ef633c8abeebfd57b985600cfeef7624fad9c104adaa76ef2267007558fbd0c841824389d0265bf5c4086125298547b04ecaaa4f8862f3062b0c334a038c3d8dbbd5d708299390d21e04c9904d5d9f56b4edc2a30a36bdccb9addf11ba6c4126dfe328d67924fa46480a941b5dd537652d6f8e33f133b7c9fac8dad2a339152b32891a82e8df65dc5445d515e5584f73ee5258a4ec2e04741f522aa211ae81ef084c77800f74fc5058a582168e) 

 * [goman.v0.3.1.web-mac.tar.gz 6.3MB (码云源)](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e5cb29cf7fdba05c25a9b754b59a6151fa672f8d171d9089cea4c48ca128d1c28bf5cae2024524be777545bbf8b481ae21cb83cfc62b1a933162483b551a0337352dc2c696079aa1505c2b3988d5d6dae067113a143e5595c7049121c65adbdc6f575a3a5f53745320606dee49d055f8408ee40490a8ca0a27689fb0e0ecbc2520956c5f4b77444e74acbe85df109f9eecf249c7d358a639b2eee332e94e55694d3d002b8fcfa776b8e879c877c0a0a461e6d0a0f67827575b45f8603a7e4a5276a8163cb373610d1a3f6bd9459ce44278dc96e8d67d73db983955c31a788aff7f4b037dc2ac92f0ff52096d15f5113aa106e689f0d2c1b246a0c35b95dc6e0dc) 

app版，独立运行，更简洁，但有些限制

* [goman.v0.3.1.app-win.zip 5.6MB (码云源)](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e5cb29cf7fdba05c25a9b754b59a6151fa672f8d171d9089cea4c48ca128d1c2875bb8f7b70f345c6fe1be7c7446df5972a479a09b044ea3d038d6d236542a304d68b2f6ba6d298e0515ae728a2f62270f338c461baa65da2729dfc33956cfb31dd95d1ad0bbc7a88a1a7bfb46a884a363542b07cee3a97e79ea0583bc3eca07fa5b88b728acb1d9aef1ef1c392f76abbc75df9b6941f00e98685905102659a39c0e6ba647fdd3634e6cbbb2614a7c1c089c283edbab78afedd0a8408dc5a18e74517b288b82100724c2ca4f7fb275ebef0f839ce7399ec430cf77ae33e41ec66d02b4c4ec2463f0f679affa6da7430ef4d421480f7dd97ecb283da50be460bf3)  (只兼容IE10/IE11内核，请注意升级系统IE浏览器)

* [goman.v0.3.1.app-mac.tar.gz 6.3MB (码云源)](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e5cb29cf7fdba05c25a9b754b59a6151fa672f8d171d9089cea4c48ca128d1c28926547606ce7919ae49829058762e4dda907a558513589a3a4b55ddfc53bb334449e5f83a32be1b2a37caa17931d5436af53a97e99c948aa9ac19ee5b1068e750add7ebf9925e660726f0d455ca89fdf61ad140e73af1d3e19859cc9baa33f73e38e830bebb649c6357ec427d1cc8a47a6c8954b7b2cadb07d5c646b6f7f6414275ed2b5324c76cbdd9a7546f7d2f1ddfb55825bc1b508da8a92c514286cb11d009d750a55019294c1f4a23af785e8a5f0543dfce725da2153d55073cecaf0697fddaa170a69930a031486f1678bde85cbd68a91f956aaa29208ece9e0cc02cf)  (已知问题：无法使用复制/粘贴快捷键，但可使用鼠标右键操作)

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

Backend Go + [Beego](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467c1826c7838e81d98dcf492284684f84) 

Frontend Typescript + [Vue](http://u.720life.cn/g/1eea7f654038e3466b5f7afd82540e023fd6d2023b41aa69a1d2cc1d8b2bfc97)  + [iView](http://u.720life.cn/g/042b48c1b518af8039860c9df004b13cb855bd704dab6d9eda4b7866cab288c8) 

web版引导界面使用了 [Knockout](http://u.720life.cn/g/a9a20becfb4c3be6f3a78cf229214827acf26e9321dd56cf0adc2998b41e884e)  + [layui样式](http://u.720life.cn/g/330802d232849288787f1cd346adeee3c838d0b1f3345344d023de319b74982b) 

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