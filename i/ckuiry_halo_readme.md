  Halo  

> Halo may be the best Java blog system. | Halo可能是最好的Java博客系统。

[![JDK](https://img.shields.io/badge/JDK-1.8-yellow.svg)](#)
[![GitHub release](https://img.shields.io/github/release/ruibaby/halo.svg)](https://github.com/ruibaby/halo/releases)
[![Travis CI](https://img.shields.io/travis/ruibaby/halo.svg)](https://travis-ci.org/ruibaby/halo)

------------------------------

## 目录

- [Introduction 简介](#introduction-简介)
- [Quickstart 快速开始](#quickstart-快速开始)
- [Demo 演示](#demo-演示)
- [Download 下载部署](#download-下载部署)
- [Docs 文档](#docs-文档)
- [Themes 主题](#themes-主题)
- [License 许可证](#license-许可证)
- [Todo 后续功能](#todo-后续功能)
- [Thanks 感谢](#thanks-感谢)
- [Donate 捐赠](#donate-捐赠)

## Introduction 简介

**Halo** [ˈheɪloʊ]，意为光环。当然，你也可以当成拼音读(哈喽)。

轻快，简洁，功能强大，使用Java开发的博客系统。

> Halo交流群: 162747721

## Quickstart 快速开始

```bash
git clone https://github.com/ruibaby/halo.git
cd halo
mvn clean package -Pprod
java -jar target/dist/halo/halo-latest.jar
```

> 注意：如使用Idea，Eclipse等IDE运行的话，需要安装Lombok插件。

Let's start: http://localhost:8090

## Demo 演示

[测试地址]http://149.28.63.223，[测试后台admin,123456]http://149.28.63.223/admin

[Ryan0up'S Blog](http://u.720life.cn/g/cb2f0bc20b4bb1f7694586275886c06b) 

[SNAIL BLOG](http://u.720life.cn/g/7ce658b080dbea0a8ea55dab4a516852) 

[宋浩志博客](http://u.720life.cn/g/6ccf74cff720341fecda665de4ec0ade0966e132d16bfe875d60d634e15fb5da) 

## Download 下载部署

> 如需部署到服务器，请参考[Halo部署教程]https://ryanc.cc/archives/halo-run-with-git-maven)或者[Wiki]https://github.com/ruibaby/halo/wiki)。

## Docs 文档

[Halo Document](http://u.720life.cn/g/647be2c4b21b2926d8ebf1ea842b5c99a7c4b1786ff0eb6cd51fa0e2b144bb73) 

> 文档正在不断完善中。

## Themes 主题

除了内置的[Anatole](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dc515dba2b4d87b0a57969390a65391901b5619005b6babbb399939e04e0a41abcfad0c85493491baeeae3374da1d98cb68f38513e7763f3e3eef609594898a29e3b408ecbb7201a24927203f44592bb4024ee7b3b58af89e702aeee18d0adc2e246e5ae7d66360584a89d62afa158a8d2d731615ac39cecb55dee3b4b2091cbd96b24ae908a14c35c81256b5af9a341bc0420dd559a413a0d1c1ceee83932122f13e1356fefeb2fe7afec81bfb9deef73068c5ad004c8ed1b639abbade029014391e3bdce0cb86a41f8a9ff5029af607bcc5c71c5ea0404b36f8bbaee7a18fc 

- [Vno](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b8301a5dfb204e96d2dc703b139cabe746f2c7b5287eb916b99e0724eccce7f9)  - 来自Jekyll的一款主题，作者[Wei Wang]https://onevcat.com/)。
- [Hux](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304609881a66ba129474d42125ff7e44575816e1b21530161c6447e30efddb43765d)  - 来自Jekyll的一款主题，作者[Xuan Huang]https://huangxuan.me/)。

## License 许可证

[![license](https://img.shields.io/github/license/ruibaby/halo.svg)](https://github.com/ruibaby/halo/blob/master/LICENSE)

> Halo使用GPL-v3.0协议开源，请尽量遵守开源协议，即便是在中国。

## Todo 后续功能

- [x] 文章阅读统计
- [ ] 文章顶置
- [ ] 集成又拍云，七牛云等云服务

## Thanks 感谢

Halo的诞生离不开下面这些项目：

- [IntelliJ IDEA]https://www.jetbrains.com/idea/)：个人认为最强大的Java IDE，没有之一
- [Spring Boot]https://github.com/spring-projects/spring-boot)：Spring的微服务框架
- [Freemarker]https://freemarker.apache.org/)：模板引擎，使页面静态化
- [H2 Database]https://github.com/h2database/h2database)：嵌入式数据库，无需安装
- [Druid]https://github.com/alibaba/druid)：阿里开发的连接池
- [Spring-data-jpa]https://github.com/spring-projects/spring-data-jpa.git)：不需要写sql语句的持久层框架
- [Ehcache]http://www.ehcache.org/)：缓存框架
- [Lombok]https://www.projectlombok.org/)：让代码更简洁
- [Apache Commons]http://commons.apache.org/)：非常好用的Java工具库
- [oh-my-email]https://github.com/biezhi/oh-my-email)：可能是最小的Java邮件发送库了，支持抄送、附件、模板等
- [Hutool](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464890b78bf8a4fe32681c0079c418127606d3585a014882bada694e141085f8937cd7f294c96c0b1ca242ce9a09f19162 
- [Thumbnailator]https://github.com/coobird/thumbnailator)：缩略图生成库
- [AdminLTE](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469938d875cf47e5488f379f965eb2a074650967228d842f796f127036f217821f36bb8f93e6f8f2be93d89aa05666c91c91cfdab6ca453dd6e9593c6faef6ffdc 
- [Bootstrap]https://github.com/twbs/bootstrap.git)：使用最广泛的前端ui框架
- [Animate]https://github.com/daneden/animate.css.git)：非常好用的css动效库
- [Editor.md]https://github.com/pandao/editor.md.git)：Markdown前端编辑器，遗憾作者弃坑了
- [Editor.md]https://github.com/hawtim/editor.md)：Editor.md，hawtim接过来维护的版本
- [Bootstrap-FileInput]https://github.com/kartik-v/bootstrap-fileinput.git)：个人认为最好用的上传组件，没有之一
- [Font-awesome]https://github.com/FortAwesome/Font-Awesome.git)：使用最广泛的字体图标库
- [Jquery]https://github.com/jquery/jquery.git)：使用最广泛的JavaScript框架
- [Layer]https://github.com/sentsin/layer.git)：个人认为最实用最好看的弹出层组件，没有之一
- [Jquery-Toast]https://github.com/kamranahmedse/jquery-toast-plugin)：消息提示组件
- [Pjax]https://github.com/defunkt/jquery-pjax.git)：pushState + ajax = pjax
- [OwO]https://github.com/DIYgod/OwO)：前端表情库

## Donate 捐赠

> 如果Halo对你有帮助，可以请作者喝瓶娃哈哈哈哈哈哈哈哈哈哈。

| 支付宝  | 微信  |
| :------------: | :------------: |
|    |    |


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)