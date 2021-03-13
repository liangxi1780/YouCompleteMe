> JavaGuide 的Star数量虽然比较多，但是它的价值和含金量一定是不能和 Dubbo、Nacos这些优秀的国产开源项目比的。希望国内可以出更多优秀的开源项目！
>
> 另外，希望大家对面试不要抱有侥幸的心理，打铁还需自身硬！  我希望这个文档是为你学习  Java 指明方向，而不是用来应付面试用的。加油！奥利给！

**开始阅读之前必看** ：

1. [完结撒花！JavaGuide面试突击版来啦！](./docs/javaguide面试突击版.md)
2. [JavaGuide重大更新记录](./docs/update-history.md)

更多原创内容和干货分享：

1. [公众号—JavaGuide](#公众号) ： 最新原创文章+免费领取本文档配套的《Java面试突击》以及Java工程师必备学习资源）
2. [微信](#联系我) ：如果需要和我交流的话可以加我私人微信(ps: 有问题的话也可以问，我会尽量回答大家，我很随和的，哈哈！另外，账号快加满了)
3. [B站-Guide哥]https://space.bilibili.com/504390397)：（各种干货视频和生活向视频，来个一键三连可好！）
4.  [知识星球—JavaGuide读者圈](http://u.720life.cn/g/e11b05d6b68eaf9173d9bd654777839249bba7fe7ff4055b5a6f868456b444d4ef57bf3e581e354e5ac7da7ed995f7b78fb494abf867dcf933b1d8ab187233311bf29272ccdf97876a1878cd9baa1c6e1039e226f0451c9af5cb5ee603f1d4bc0bf87b6dd1f0623cdee9f42d3a8f54a0bde8c46d586ba7300b557b4dfa53a6b438c5a3a04519c698289b895cbeda5d5aa784d0af73369ee65c05cf26233f3737) 

Github用户如果访问速度缓慢的话，可以转移到[码云](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ea90ac08a1bbc4ef42cec4457848b75d3b102110a85e754c3f00eab6dd8bbf52d  )查看，或者[在线阅读](http://u.720life.cn/g/08b039364736ef6104848cd7be5d9256337ccc938e960bcff773cc5029182045a3c8950c09590dcbea386e89fd934e61  )。

 
 
	 
 
 

 
     
     
     
     
     
 

 Sponsor 
 
 
 
 
 

## 目录

- [Java](#java)
    - [基础](#基础)
    - [容器](#容器)
    - [并发](#并发)
    - [JVM](#jvm)
    - [其他](#其他)
- [网络](#网络)
- [操作系统](#操作系统)
    - [Linux](#linux)
- [数据结构与算法](#数据结构与算法)
    - [数据结构](#数据结构)
    - [算法](#算法)
- [数据库](#数据库)
    - [MySQL](#mysql)
    - [Redis](#redis)
- [系统设计](#系统设计)
    - [常用框架](#常用框架)
        - [Spring](#spring)
        - [SpringBoot](#springboot)
        - [MyBatis](#mybatis)
    - [认证授权(JWT、SSO)](#认证授权)
    - [分布式](#分布式)
        - [Elasticsearch(分布式搜索引擎)](#elasticsearch分布式搜索引擎)
        - [RPC](#rpc)
        - [消息队列](#消息队列)
        - [API 网关](#api-网关)
        - [分布式id](#分布式id)
        - [分布式限流](#分布式限流)
        - [分布式接口幂等性](#分布式接口幂等性)
        - [数据库扩展](#数据库扩展)
        - [ZooKeeper](#zookeeper)
    - [大型网站架构](#大型网站架构)
        - [性能测试](#性能测试)
        - [高并发](#高并发)
        - [高可用](#高可用)
    - [微服务](#微服务)
        - [Spring Cloud](#spring-cloud)
- [面试指南](#面试指南)
- [Java学习常见问题汇总](#java学习常见问题汇总)
- [工具](#工具)
    - [Git](#git)
    - [Docker](#docker)
    - [其他](#其他-1)
- [资源](#资源)
    - [书单](#书单)
    - [实战项目推荐](#实战项目推荐)
    - [Github](#github)
- [待办](#待办)
- [说明](#说明)

## Java

### 基础

**基础知识系统总结：**

1. **[Java 基础知识](docs/java/Java基础知识.md)**
2. **[Java 基础知识疑难点/易错点](docs/java/Java疑难点.md)**
3. [【加餐】一些重要的Java程序设计题](docs/java/Java程序设计题.md)
4. [【选看】J2EE 基础知识](docs/java/J2EE基础知识.md)

**重要知识点详解：**

1. [枚举](docs/java/basic/用好Java中的枚举真的没有那么简单.md) （很重要的一个数据结构，用好枚举真的没有那么简单！）
2. [Java 常见关键字总结：final、static、this、super!](docs/java/basic/final,static,this,super.md)
3. [什么是反射机制?反射机制的应用场景有哪些?](docs/java/basic/reflection.md)

**其他：**

1. [JAD反编译](docs/java/JAD反编译tricks.md)

### 容器

1. **[Java容器常见面试题/知识点总结](docs/java/collection/Java集合框架常见面试题.md)**
2. [ArrayList 源码](docs/java/collection/ArrayList.md)  、[LinkedList 源码](docs/java/collection/LinkedList.md)   、[HashMap(JDK1.8)源码](docs/java/collection/HashMap.md)  

### 并发

**面试题总结：**

1. **[Java 并发基础常见面试题总结](docs/java/Multithread/JavaConcurrencyBasicsCommonInterviewQuestionsSummary.md)**
2. **[Java 并发进阶常见面试题总结](docs/java/Multithread/JavaConcurrencyAdvancedCommonInterviewQuestions.md)**

**必备知识点：**

1. [并发容器总结](docs/java/Multithread/并发容器总结.md)
2. **[Java线程池学习总结](./docs/java/Multithread/java线程池学习总结.md)**
3. [乐观锁与悲观锁](docs/essential-content-for-interview/面试必备之乐观锁与悲观锁.md)
4. [JUC 中的 Atomic 原子类总结](docs/java/Multithread/Atomic.md)
5. [AQS 原理以及 AQS 同步组件总结](docs/java/Multithread/AQS.md)

### JVM

1. **[Java内存区域](docs/java/jvm/Java内存区域.md)**
2. **[JVM垃圾回收](docs/java/jvm/JVM垃圾回收.md)**
3. [JDK 监控和故障处理工具](docs/java/jvm/JDK监控和故障处理工具总结.md)
4. [类文件结构](docs/java/jvm/类文件结构.md)
5. **[类加载过程](docs/java/jvm/类加载过程.md)**
6. [类加载器](docs/java/jvm/类加载器.md)
7. **[【待完成】最重要的 JVM 参数指南（翻译完善了一半）](docs/java/jvm/最重要的JVM参数指南.md)**
8. [JVM 配置常用参数和常用 GC 调优策略](docs/java/jvm/GC调优参数.md)
9. **[【加餐】大白话带你认识JVM](docs/java/jvm/[加餐]大白话带你认识JVM.md)**

### 其他

1. **I/O** ：[BIO,NIO,AIO 总结 ](docs/java/BIO-NIO-AIO.md)
2. **Java 8**  ：[Java 8 新特性总结](docs/java/What's%20New%20in%20JDK8/Java8Tutorial.md)、[Java 8 学习资源推荐](docs/java/What's%20New%20in%20JDK8/Java8教程推荐.md)、[Java8 forEach 指南](docs/java/What's%20New%20in%20JDK8/Java8foreach指南.md)
3.  **[Java 编程规范以及优雅 Java 代码实践总结](docs/java/Java编程规范.md)**
4. 设计模式 :[设计模式系列文章](docs/system-design/设计模式.md)

## 网络

1. [计算机网络常见面试题](docs/network/计算机网络.md)
2. [计算机网络基础知识总结](docs/network/干货：计算机网络知识总结.md)
3. [HTTPS中的TLS](docs/network/HTTPS中的TLS.md)

## 操作系统

操作系统相关概念总结

### Linux

* [后端程序员必备的 Linux 基础知识](docs/operating-system/后端程序员必备的Linux基础知识.md)  
* [Shell 编程入门](docs/operating-system/Shell.md) 

## 数据结构与算法

### 数据结构

- [不了解布隆过滤器？一文给你整的明明白白！](docs/dataStructures-algorithms/data-structure/bloom-filter.md)
- [数据结构知识学习与面试](docs/dataStructures-algorithms/数据结构.md)

### 算法

- [算法学习资源推荐](docs/dataStructures-algorithms/算法学习资源推荐.md)  
- [几道常见的字符串算法题总结 ](docs/dataStructures-algorithms/几道常见的子符串算法题.md)
- [几道常见的链表算法题总结 ](docs/dataStructures-algorithms/几道常见的链表算法题.md)   
- [剑指offer部分编程题](docs/dataStructures-algorithms/剑指offer部分编程题.md)
- [公司真题](docs/dataStructures-algorithms/公司真题.md)
- [回溯算法经典案例之N皇后问题](docs/dataStructures-algorithms/Backtracking-NQueens.md)

## 数据库

### MySQL

1. **[【推荐】MySQL/数据库 知识点总结](docs/database/MySQL.md)**
2. **[阿里巴巴开发手册数据库部分的一些最佳实践](docs/database/阿里巴巴开发手册数据库部分的一些最佳实践.md)**
3. **[一千行MySQL学习笔记](docs/database/一千行MySQL命令.md)**
4. [MySQL高性能优化规范建议](docs/database/MySQL高性能优化规范建议.md)
5. [数据库索引总结1](docs/database/MySQL%20Index.md)、[数据库索引总结2](docs/database/数据库索引.md)
6. [事务隔离级别(图文详解)](docs/database/事务隔离级别(图文详解).md)
7. [一条SQL语句在MySQL中如何执行的](docs/database/一条sql语句在mysql中如何执行的.md)

### Redis

* [Redis 总结](docs/database/Redis/Redis.md)
* [Redlock分布式锁](docs/database/Redis/Redlock分布式锁.md)
* [如何做可靠的分布式锁，Redlock真的可行么](docs/database/Redis/如何做可靠的分布式锁，Redlock真的可行么.md)
* [几种常见的 Redis 集群以及使用场景](docs/database/Redis/redis集群以及应用场景.md) 

## 系统设计

### 常用框架

#### Spring

1. [Spring 学习与面试](docs/system-design/framework/spring/Spring.md)
2. **[Spring 常见问题总结](docs/system-design/framework/spring/SpringInterviewQuestions.md)**
3. [Spring中 Bean 的作用域与生命周期](docs/system-design/framework/spring/SpringBean.md)
4. [SpringMVC 工作原理详解](docs/system-design/framework/spring/SpringMVC-Principle.md)
5. [Spring中都用到了那些设计模式?](docs/system-design/framework/spring/Spring-Design-Patterns.md)

#### SpringBoot

- **[SpringBoot 指南/常见面试题总结](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ce87b8a12f7ae47af1609e728756ba344a82d488ca3dfdcdec5907944e1786cec5a32b04d7761df3ec7ecd79e2c4658a 

#### MyBatis

- [MyBatis常见面试题总结](docs/system-design/framework/mybatis/mybatis-interview.md)

### 认证授权

**[认证授权基础:搞清Authentication,Authorization以及Cookie、Session、Token、OAuth 2、SSO](docs/system-design/authority-certification/basis-of-authority-certification.md)**

#### JWT

- **[JWT 优缺点分析以及常见问题解决方案](docs/system-design/authority-certification/JWT-advantages-and-disadvantages.md)**
- **[适合初学者入门 Spring Security With JWT 的 Demo](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ce87b8a12f7ae47af1609e728756ba3495d4c76ede1d8fc1f43d503db26a143017addeb8ff4a1470a43aa20822bc685a 

#### SSO(单点登录)

SSO(Single Sign On)即单点登录说的是用户登陆多个子系统的其中一个就有权访问与其相关的其他系统。举个例子我们在登陆了京东金融之后，我们同时也成功登陆京东的京东超市、京东家电等子系统。相关阅读：**[SSO 单点登录看这篇就够了！](docs/system-design/authority-certification/sso.md)**

### 分布式

[分布式相关概念入门](docs/system-design/website-architecture/分布式.md)

#### Elasticsearch(分布式搜索引擎)

提高搜索效率。常见于电商购物网站的商品搜索于分类。

代办......

#### RPC

让调用远程服务调用像调用本地方法那样简单。

- [Dubbo 总结：关于 Dubbo 的重要知识点](docs/system-design/data-communication/dubbo.md)
- [服务之间的调用为啥不直接用 HTTP 而用 RPC？](docs/system-design/data-communication/why-use-rpc.md)

#### 消息队列

消息队列在分布式系统中主要是为了接耦和削峰。相关阅读： **[消息队列总结](docs/system-design/data-communication/message-queue.md)** 。

**RabbitMQ:**

1. [RabbitMQ 入门](docs/system-design/data-communication/rabbitmq.md)

**RocketMQ:**

1. [RocketMQ 入门](docs/system-design/data-communication/RocketMQ.md)
2. [RocketMQ的几个简单问题与答案](docs/system-design/data-communication/RocketMQ-Questions.md)

**Kafka:**

1. **[Kafka 入门+SpringBoot整合Kafka系列](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ce87b8a12f7ae47af1609e728756ba3459c6fdf89bb0312866d238e6a55371ce17c20aa92e94c42e43d2ccc94f9bcdba 
2. **[Kafka 常见面试题总结](docs/system-design/data-communication/kafka-inverview.md)**
3. [【加餐】Kafka入门看这一篇就够了](docs/system-design/data-communication/Kafka入门看这一篇就够了.md)

#### API 网关

网关主要用于请求转发、安全认证、协议转换、容灾。

1. [为什么要网关？你知道有哪些常见的网关系统？](docs/system-design/micro-service/api-gateway-intro.md)
2. [如何设计一个亿级网关(API Gateway)？](docs/system-design/micro-service/API网关.md)

#### 分布式id

1. [为什么要分布式 id ？分布式 id 生成方案有哪些？](docs/system-design/micro-service/分布式id生成方案总结.md)

#### 分布式限流

1. [限流算法有哪些？](docs/system-design/micro-service/limit-request.md)

#### 分布式接口幂等性

#### ZooKeeper

> 前两篇文章可能有内容重合部分，推荐都看一遍。

1. [【入门】ZooKeeper 相关概念总结](docs/system-design/framework/ZooKeeper.md)
2. [【进阶】Zookeeper 原理简单入门！](docs/system-design/framework/ZooKeeper-plus.md)
3. [【拓展】ZooKeeper 数据模型和常见命令](docs/system-design/framework/ZooKeeper数据模型和常见命令.md)

#### 其他

- 接口幂等性（代办）：分布式系统必须要考虑接口的幂等性。

#### 数据库扩展

读写分离、分库分表。

代办.....

### 大型网站架构

- [8 张图读懂大型网站技术架构](docs/system-design/website-architecture/8%20张图读懂大型网站技术架构.md)
- [关于大型网站系统架构你不得不懂的10个问题](docs/system-design/website-architecture/关于大型网站系统架构你不得不懂的10个问题.md)

#### 性能测试

- [后端程序员也要懂的性能测试知识](http://u.720life.cn/g/aae964087bc563d7b751283d22b670acb06c8803fca537f9ca7ea6e3b3389baca11c74cd97b8dbb5d888c730f1a451c8)  （知识星球）

#### 高并发

待办......

#### 高可用

高可用描述的是一个系统在大部分时间都是可用的，可以为我们提供服务的。高可用代表系统即使在发生硬件故障或者系统升级的时候，服务仍然是可用的 。相关阅读： **《[如何设计一个高可用系统？要考虑哪些地方？](docs/system-design/website-architecture/如何设计一个高可用系统？要考虑哪些地方？.md)》** 。

### 微服务

#### Spring Cloud

- [ 大白话入门 Spring Cloud](docs/system-design/micro-service/spring-cloud.md)

## 面试指南

> 这部分很多内容比如大厂面经、真实面经分析被移除，详见[完结撒花！JavaGuide面试突击版来啦！](./docs/javaguide面试突击版.md)。

1. **[【备战面试1】程序员的简历就该这样写](docs/essential-content-for-interview/PreparingForInterview/程序员的简历之道.md)**
2. **[【备战面试2】初出茅庐的程序员该如何准备面试？](docs/essential-content-for-interview/PreparingForInterview/interviewPrepare.md)**
3. **[【备战面试3】7个大部分程序员在面试前很关心的问题](docs/essential-content-for-interview/PreparingForInterview/JavaProgrammerNeedKnow.md)**
4. **[【备战面试4】Github上开源的Java面试/学习相关的仓库推荐](docs/essential-content-for-interview/PreparingForInterview/JavaInterviewLibrary.md)**
5. **[【备战面试5】如果面试官问你“你有什么问题问我吗？”时，你该如何回答](docs/essential-content-for-interview/PreparingForInterview/面试官-你有什么问题要问我.md)**
6. [【备战面试6】应届生面试最爱问的几道 Java 基础问题](docs/essential-content-for-interview/PreparingForInterview/应届生面试最爱问的几道Java基础问题.md)
7. **[【备战面试6】美团面试常见问题总结(附详解答案)](docs/essential-content-for-interview/PreparingForInterview/美团面试常见问题总结.md)**
8. **[【备战面试7】一些刁难的面试问题总结](http://u.720life.cn/g/899b97186d3c25e681bcee8d4ee5bef1008fbe4eddae4c482f6be278f847d8207eed1034f100286490f60b2da7b32d44 

## Java学习常见问题汇总

1. [Java学习路线和方法推荐](docs/questions/java-learning-path-and-methods.md)
2. [Java培训四个月能学会吗？](docs/questions/java-training-4-month.md)
3. [新手学习Java，有哪些Java相关的博客，专栏，和技术学习网站推荐？](docs/questions/java-learning-website-blog.md)
4. [Java 还是大数据，你需要了解这些东西！](docs/questions/java-big-data)
5. [Java 后台开发/大数据？你需要了解这些东西！]https://articles.zsxq.com/id_wto1iwd5g72o.html)（知识星球）

## 工具

### Git

* [Git入门](docs/tools/Git.md)

### Docker

1. [Docker 基本概念解读](docs/tools/Docker.md)
2. [一文搞懂 Docker 镜像的常用操作！](docs/tools/Docker-Image.md )

### 其他

- [阿里云服务器使用经验](docs/tools/阿里云服务器使用经验.md)

## 资源

### 书单

- [Java程序员必备书单](docs/data/java-recommended-books.md)

### 实战项目推荐

- [Github 上热门的 Spring Boot 项目实战推荐](docs/data/spring-boot-practical-projects.md)

### Github

- [Github 上 Star 数最多的 10 个项目，看完之后很意外!](docs/tools/github/github-star-ranking.md)
- [年末将至，值得你关注的16个Java 开源项目！](docs/github-trending/2019-12.md)
- [Java 项目月榜单](docs/github-trending/JavaGithubTrending.md)

***

## 待办

- [ ] Netty 总结(---正在进行中---)
- [ ] 数据结构总结重构(---正在进行中---)

## 说明

开源项目在于大家的参与，这才使得它的价值得到提升。感谢🙏有你！

### JavaGuide介绍

开源 JavaGuide 初始想法源于自己的个人那一段比较迷茫的学习经历。主要目的是为了通过这个开源平台来帮助一些在学习 Java 或者面试过程中遇到问题的小伙伴。

*  **对于 Java 初学者来说：** 本文档倾向于给你提供一个比较详细的学习路径，让你对于Java整体的知识体系有一个初步认识。另外，本文的一些文章
也是你学习和复习 Java 知识不错的实践；
*  **对于非 Java 初学者来说：** 本文档更适合回顾知识，准备面试，搞清面试应该把重心放在那些问题上。要搞清楚这个道理：提前知道那些面试常见，不是为了背下来应付面试，而是为了让你可以更有针对的学习重点。

Markdown 格式参考：[Github Markdown格式](http://u.720life.cn/g/61a8162b46994a094a73a09d7686563452361333eaa4bf88d4e0a0dabf65b9c2a2d94c2c5ad6e53fae61299eaafd6d4b4d88fbef3c0beae4fe3668b56c567475f6aba6aa36a283cf8200e28d12337ff8f95573b2dc93633a97b9ef6ddeec5c1b  CHEAT SHEET]https://www.webpagefx.com/tools/emoji-cheat-sheet/)。

利用 docsify 生成文档部署在 Github pages: [docsify 官网介绍](http://u.720life.cn/g/b46a37fd5c7f516475e4d28661ce41b000b67f27655493cec801936b38254979) 

### 关于转载

如果你需要转载本仓库的一些文章到自己的博客的话，记得注明原文地址就可以了。

### 如何对该开源文档进行贡献

1. 笔记内容大多是手敲，所以难免会有笔误，你可以帮我找错别字。
2. 很多知识点我可能没有涉及到，所以你可以对其他知识点进行补充。
3. 现有的知识点难免存在不完善或者错误，所以你可以对已有知识点进行修改/补充。

### 联系我

![个人微信](https://my-blog-to-use.oss-cn-beijing.aliyuncs.com/2019-7/wechat3.jpeg)

### Contributor

下面是笔主收集的一些对本仓库提过有价值的pr或者issue的朋友，人数较多，如果你也对本仓库提过不错的pr或者issue的话，你可以加我的微信与我联系。下面的排名不分先后！

 
     
 
 
     
 
   
     
 
   
     
 

 
      
 
     
 
 
      
 
     
 
 
     
 
 
     
 "
   
     
 
   
     
 
   
     
 
   
     
 
   
     
 
   
     
 
   
     
 

### 公众号

如果大家想要实时关注我更新的文章以及分享的干货的话，可以关注我的公众号。

**《Java面试突击》:** 由本文档衍生的专为面试而生的《Java面试突击》V2.0 PDF 版本[公众号](#公众号)后台回复 **"Java面试突击"** 即可免费领取！

**Java工程师必备学习资源:** 一些Java工程师常用学习资源公众号后台回复关键字 **“1”** 即可免费无套路获取。 

![我的公众号](https://my-blog-to-use.oss-cn-beijing.aliyuncs.com/2019-6/167598cd2e17b8ec.png)





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)