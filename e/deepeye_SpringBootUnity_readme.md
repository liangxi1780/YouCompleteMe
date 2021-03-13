[![Build Status](https://travis-ci.org/xiaomoinfo/XiaomoApi.svg?branch=master)](https://travis-ci.org/xiaomoinfo/XiaomoApi)
[![GitHub issues](https://img.shields.io/github/issues/xiaomoinfo/SpringBootUnity.svg)](https://github.com/xiaomoinfo/SpringBootUnity/issues)
[![GitHub forks](https://img.shields.io/github/forks/xiaomoinfo/SpringBootUnity.svg)](https://github.com/xiaomoinfo/SpringBootUnity/network)
[![GitHub stars](https://img.shields.io/github/stars/xiaomoinfo/SpringBootUnity.svg)](https://github.com/xiaomoinfo/SpringBootUnity/stargazers)
[![GitHub license](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://raw.githubusercontent.com/xiaomoinfo/SpringBootUnity/master/LICENSE)
[![Maven Central](https://img.shields.io/maven-central/v/org.apache.maven/apache-maven.svg)]()
[![GitHub followers](https://img.shields.io/github/followers/xiaomoinfo.svg?style=social&label=Follow)]()
[![GitHub watchers](https://img.shields.io/github/watchers/xiaomoinfo/SpringBootUnity.svg?style=social&label=Watch)]()

### 环境
- `maven` latest   
- `jdk1.8`   
- `spring boot 1.5.6 release`(目前最新版)
-  个人推荐`idea`来代替eclipse（希望不要被说成异教徒必须死）
- mysql5.5+
- git: 版本管理
- nginx: 反向代理服务器

###  项目简介
![mark](https://static.xiaomo.info/image/project/mark.png)


### 启动方式
- `spring boot`内置了tomcat做为web容器，默认打成jar包直接放在服务器上执行就可以了
> `java -Xms64m -Xmx2048m -jar project.jar 5 >> ./project.log &`

![jar](https://static.xiaomo.info/image/project/javajar.gif)

- 如果需要定制化打成war包，那么也很简单。在`maven`中做下设置就ok了,然后把war包扔到tomcat下面就可以运行了

```
     4.0.0 
     api 
     war 
```


![war](https://static.xiaomo.info/image/project/war.png)


###  项目说明
需求是多变的，本项目是以spring boot为基础，在使用spring boot的过程中对应不同的需求选用不同的技术和spring boot进行搭配，因此本项目是个偏于使用示例的定位。同时如果您在使用spring boot的过程中有什么好用的技术期待您对本项目的PR。

### 关于我
 @[小莫]https://xiaomo.info)：本人是一个热爱开源精神、追求新潮的开发者，技术过得去，还算勤勉！习惯以github的issue驱动方式来组织我的项目，也希望感兴趣的朋友和我联系，一起进步，共同开发感兴趣的开源项目。目前任rpg服务端主程，熟悉游戏开发和web开发。同时也是个喜欢二次元的死宅，爱动漫，略懂日语。

### 在线小工具

- [在线Cron表达式生成器](http://u.720life.cn/g/41a88c49241c9a1f605f913332fbeca495e13ea8491440f895022f4f9df8c3e3  "在线Cron表达式生成器")

- [在线工具 - 程序员的工具箱](http://u.720life.cn/g/41843dbe0fafe94d482221c4b6428051  "在线工具 - 程序员的工具箱")


###  问题反馈
1. 欢迎提[issue]https://github.com/xiaomoinfo/SpringBootUnity/issues)一起完善这个项目。
2. QQ: 83387856
4. 个人主站: https://xiaomo.info

### 在线文档

- [JDK7英文文档](http://u.720life.cn/g/0b74b15bb9de87b5a2fb1d39225b742f9755696133ba7493060bcd72b849d00cc424e0901ba49e1f7b1c0c7ad11a37d3e40ba7e7c999548bff8af0052835554f  "JDK7英文文档")

- [Spring4.x文档](http://u.720life.cn/g/3d3c1eebe7d1a3ce4b19ffb3e57807e89fa619207522cc50e254f65d86af1be0b306863a011de5ef8e4a8b3c5c17ee5d  "Spring4.x文档")

- [Mybatis3官网](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a215e4d93221eb26b660bea25686b89be63142caf406b6e1c14d3ab51db921e10ca  "Mybatis3官网")

- [Dubbo官网](http://u.720life.cn/g/ad27fc5875c834b4568aeb04084d2bc0  "Dubbo官网")

- [Nginx中文文档](http://u.720life.cn/g/0b74b15bb9de87b5a2fb1d39225b742f9755696133ba7493060bcd72b849d00c70ea5132d4eda0624001e88d63d0a989754ed6dd7d93878effc7028703b52239  "Nginx中文文档")

- [Freemarker在线手册](http://u.720life.cn/g/91631dc92407872deef9e7c2f21c90370ec42bca0660599fef01f69ddec2c69d  "Freemarker在线中文手册")

- [Velocity在线手册](http://u.720life.cn/g/7b1a2cc30709fab1f7d3403a12a69622014754ee2d62e2b7aa50d029c7b0b7e601990af5feaafb66030c1887a5b8f3fb78ff2e9ed95d64280286dca81679e83b  "Velocity在线手册")

- [Bootstrap在线手册](http://u.720life.cn/g/5dc63d04a35b84846e193be705862c773cff2a22a6b2940498e28eb01e58b4bd  "Bootstrap在线手册")

- [Git官网中文文档](http://u.720life.cn/g/0699e533b96232c5e210af6ab5668134f26d4ce8eb73c737efb58c5e94ea6f74  "Git官网中文文档")

- [Thymeleaf](http://u.720life.cn/g/93cb058e2406031f6144e42823783979064a4202b3689251145126e998ce8f5defa6da90df7b82a90b1cc7a1307b069c6b1ac6b538cb2504cf0ab092b85f079d  "Thymeleaf")



## [License](LICENSE "apache")

    Copyright 2017 xiaomo

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)