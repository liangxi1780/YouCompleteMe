## mica（云母）
[![Build Status](https://www.travis-ci.org/lets-mica/mica.svg?branch=master)](https://www.travis-ci.org/lets-mica/mica)
![JAVA 8](https://img.shields.io/badge/JDK-1.8+-brightgreen.svg)
[![Mica Maven release](https://img.shields.io/nexus/r/https/oss.sonatype.org/net.dreamlu/mica-bom.svg?style=flat-square)](https://mvnrepository.com/artifact/net.dreamlu/mica-bom)
[![Mica maven snapshots](https://img.shields.io/nexus/s/https/oss.sonatype.org/net.dreamlu/mica-bom.svg?style=flat-square)](https://oss.sonatype.org/content/repositories/snapshots/net/dreamlu/)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/eadcb54f2ec14f31b8abf3ab13ad2d4d)](https://app.codacy.com/app/ChunMengLu/mica?utm_source=github.com&utm_medium=referral&utm_content=lets-mica/mica&utm_campaign=Badge_Grade_Settings)
[![GitHub](https://img.shields.io/github/license/lets-mica/mica.svg?style=flat-square)](https://github.com/lets-mica/mica/blob/master/LICENSE)

`Mica`，Spring Cloud 微服务开发核心包，支持 `web` 和 `webflux`。

`注意`：`snapshots` 版本会及时响应，修复最新的 `bug` 或者必要的需求。

| 依赖         | 版本              |
| ------------ | ----------------- |
| Spring | 5.x |
| Spring Boot  | 2.1.x             |
| Spring Cloud | Greenwich 版 |

![犬夜叉-云母](docs/img/mica-001.jpeg)

想要了解更多可加入【如梦技术】QQ 群：`479710041`。

## 模块划分
### mica-auto
1. 编译期生成 `spring.factories`。
2. 编译期生成 `spring-devtools.properties`。
3. 编译期生成 `FeignClient` 信息到 `spring.factories` 中，供 `mica-cloud` 中完成 `Feign` 自动化配置。

`文档地址`：[https://gitee.com/596392912/mica-auto](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6edd9cc4708a4f3db68bdd558caedb032fdfc5f3aa488ebe5957bdc31cfd95328f) 

### mica-core
- 常用工具包，基于 `Spring-core` 扩展增强，无其他依赖。
- 增强 cglib Bean copy，高性能（接近直接 get set），支持链式 bean，支持自动类型转换 。
- `$` 工具类快捷方法，不用再记忆到底有哪些工具类。
- 统一消息返回体，封装得更加好用。
- Jaskson Read Write HttpMessageConverter，分读写的消息转换器。
- Spring 枚举转换器，规则同 Jackson。

`文档地址`：[mica-core](http://u.720life.cn/g/1223673b752970deb6582301422733a62a0ee21f48da9074a4ebecbbdf788855f75b23139fd894f160fdb3649e277a8f) 

### mica-http
- `mica-http` 是 `okhttp` 的封装，Fluent 语法的 http 工具包，语法参考 HttpClient Fluent API。

`文档地址`：[mica-http](mica-http/README.md)

### mica-laytpl 
- laytpl 模板（将其引入到 java 中）

`文档地址`：[mica-laytpl](mica-laytpl/README.md)

### mica-launcher
- 项目启动器
- 启动信息打印
- 系统环境处理
- spi 扩展

`文档地址`：[mica-launcher](http://u.720life.cn/g/1223673b752970deb6582301422733a6a6f65414ce47aababc15f15c089ef1fc503b3adb83bfcbfa16bda272556b9b2c676df1466c4ace3b93eb1b798d80b695) 

### mica-boot
- 支持 `Spring boot web` 和 `Spring boot webflux`。
- 异步配置。
- 异常处理，未知异常发送 Event 事件，方便监听收集。
- swagger 自动化配置，加入 jar 包即可。
- jackson 配置。
- 文件上传配置。
- 文件下载，支持断点续传，浏览器兼容好。
- 请求日志打印，方便开发。
- url 版本号和 header 版本处理。

`文档地址`：[mica-boot](http://u.720life.cn/g/1223673b752970deb6582301422733a67952dc1582b58ef3fb9644d1e2e003c30b0dfd4a2df92b62aa3cbd0438f18204) 

### mica-boot-test
- 方便 mica-boot 测试，注入 mica-launcher 中注入的参数。

`文档地址`：[mica-boot-test](http://u.720life.cn/g/1223673b752970deb6582301422733a67952dc1582b58ef3fb9644d1e2e003c387c30f08e44bdfa17d21aed38891f341) 

### mica-log4j2
- mica log4j 配置。
- 基于 disruptor 异步日志，高性能。
- 非开发环境将 System.out 和 err 写入 log。

`文档地址`：[mica-log4j2](http://u.720life.cn/g/1223673b752970deb6582301422733a6dca6439f02301b0d4dcf7fca4573c551c131b4b67651fc89b7376478bc10db36) 

### mica-captcha
- 验证码，支持 `webflux` 和 `serlvet`。

`文档地址`：[mica-captcha](http://u.720life.cn/g/1223673b752970deb6582301422733a6623f3899e243776611850b8c10591cd67b332505e40953b61316d8205527744a) 

### mica-social
- 第三方登录组件

`文档地址`：[mica-social](mica-social/README.md)

### mica-cloud
- Feign 自动降级、header 透传、版本处理，结合 `mica-auto` 自动化配置。
- RestTemplate 自动配置，基于 okhttp 增强，添加请求日志和 Header 传递。
- hystrix 熔断器增强，支持 header 透传、当前用户获取和透传。
- Apollo Properties 配置刷新。

### mica-plus-error-catch
- 未知异常收集到 spring-cloud-stream 中，方便统一处理。

### mica-plus-redis
- redis cache name # 自动配置超时时间。
- 通用 MicaRedisCache Spring Bean。
- 分布式限流。

`文档地址`：[mica-plus-redis](mica-plus-redis/README.md)

### mica-plus-mongo
- mongo 复杂 tree 和 jsonNode 转换处理。

### mica-plus-swagger
- swagger 和 swagger-bootstrap-ui 依赖。

### mica-plus-ribbon
- 【优先级最高】ip 相同的服务（方便本地多服务联调）。
- 可设置选择的 ip 或者 ip 段，例如：`172.21.0.*`、`172.21.0.8*`。
- 可设定 `tag`，用于灰度，匹配：`nacos.discovery.metadata.tag`。

`文档地址`：[mica-plus-ribbon](mica-plus-ribbon/README.md)

### mica-plus-social
- `mica-social` 自动化配置。

`文档地址`：[mica-plus-social](mica-plus-social/README.md)

## 已知问题
lombok 生成的 method 问题：https://github.com/rzwitserloot/lombok/issues/1861

对于 xX 类属性名，第一个小写，第二个大写的 bean 属性名，Map -> Bean 或 Bean -> Map 存在问题。

不打算做兼容，待 lombok 新版修复。

## 开源协议
![LGPL v3](docs/img/lgplv3-147x51.png) 

## 协议解释
LGPL（[GNU Lesser General Public License]http://www.gnu.org/licenses/lgpl.html)）

LGPL是GPL的一个为主要为类库使用设计的开源协议。和GPL要求任何使用/修改/衍生之GPL类库的的软件必须采用GPL协议不同。LGPL允许商业软件通过类库引用(link)方式使用LGPL类库而不需要开源商业软件的代码。这使得采用LGPL协议的开源代码可以被商业软件作为类库引用并发布和销售。

但是如果修改LGPL协议的代码或者衍生，则所有修改的代码，涉及修改部分的额外代码和衍生的代码都必须采用LGPL协议。因此LGPL协议的开源代码很适合作为第三方类库被商业软件引用，但不适合希望以LGPL协议代码为基础，通过修改和衍生的方式做二次开发的商业软件采用。

## 用户权益
允许以引入不改源码的形式免费用于学习、毕设、公司项目、私活等。

特殊情况修改代码，但仍然想闭源需经过作者同意。

对未经过授权和不遵循 lgpl 协议二次开源或者商业化我们将追究到底。

参考请注明：参考自 mica：https://github.com/lets-mica/mica ，另请遵循 lgpl 协议。

`注意`：若禁止条款被发现有权追讨 **19999** 的授权费。

## 授权用户（最佳实践）
* `pigx` 宇宙最强微服务（架构师必备）：https://pig4cloud.com
* `bladex` 完整的线上解决方案（企业生产必备）：https://bladex.vip

## 相关链接
* `示例项目`：[https://github.com/lets-mica/mica-example](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046be453ee6cca485b63092180979f2b028974b1c7b19eb6f058ae573028e9e2944) 
* mica 源码 Github：[https://github.com/lets-mica](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469700d62ac59d3e6d24ce9b3ac7258fe6) 
* mica 源码 Gitee（码云）：[https://gitee.com/596392912/mica](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6edd9cc4708a4f3db68bdd558caedb032f) 
* mica 性能压测：[https://github.com/lets-mica/mica-jmh](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046be453ee6cca485b63092180979f2b028b1b82deec9fc5bf78b99dc5a980b3767) 
* 文档地址（官网）：[https://www.dreamlu.net/docs/](http://u.720life.cn/g/1223673b752970deb6582301422733a66f2dc65917008f2b9d35247450152910) 
* 文档地址（语雀-可关注订阅）：[https://www.yuque.com/dreamlu/mica](http://u.720life.cn/g/794be49a28e6f6b6aa755de579be43d947827ed69abb2b660d8206820cbcdb1e1c2694d30e66bda74e676284ee286ec4) 

## 开源推荐
- `Avue` 一款基于 vue 可配置化的神奇框架：[https://gitee.com/smallweigit/avue](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e9a45ea68dd78dd93ab4ce0a12f91adcf597755959c1ecde8ac8b2591700d6b1d) 
- `pig` 宇宙最强微服务（架构师必备）：[https://gitee.com/log4j/pig](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e003a98ff8124711bc8bb2a735eddd1c3) 
- `SpringBlade` 完整的线上解决方案（企业开发必备）：[https://gitee.com/smallc/SpringBlade](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e3546460c0cd5dba4cbac39602ce9c18cfb9683eaf44923e5c878f4ad4056bdf6) 
- `IJPay` 支付 SDK 让支付触手可及：[https://gitee.com/javen205/IJPay](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ef068ea679d97703e45f205b8f530ec5f) 

## 鸣谢
`mica-social` 参考了 `JustAuth` 并已经加入 [JustAuth](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046066dd74459bee98bfd188515b03f16770c296c2a74d25b559d1d9874813de6f8)  开发者群，想了解更多请求访问：[https://github.com/zhangyd-c/JustAuth](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046066dd74459bee98bfd188515b03f16770c296c2a74d25b559d1d9874813de6f8) 

感谢 JetBrains 提供的免费开源 License：

[![JetBrains](docs/img/jetbrains.png)](https://www.jetbrains.com/?from=mica)

感谢 `如梦技术VIP群` 小伙伴们的大力支持。

## 微信公众号

![如梦技术](docs/img/dreamlu-weixin.jpg)

精彩内容每日推荐！！！



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)