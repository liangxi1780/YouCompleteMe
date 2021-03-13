# Spring-rabbitMQ
  - 在业务逻辑的异步处理，系统解耦，分布式通信以及控制高并发的场景下，消息队列有着广泛的应用。本项目基于Spring的AMQP模块，整合流行的开源消息队列中间件rabbitMQ,实现一个向rabbitMQ添加和读取消息的功能。并比较了两种模式：生产者-消费者模式和发布-订阅模式的区别。AMQP作为比JMS更加高级的消息协议，支持更多的消息路由和消息模式。
  
- 包含的特性如下：

  ![输入图片说明](http://git.oschina.net/uploads/images/2017/0223/081751_c96aa8d6_1110335.png "在这里输入图片标题")
  
1. 如上图，生产者消费者模型：添加了一个队列，并创建了两个消费者用于监听队列消息，我们发现，当有消息到达时，两个消费者会交替收到消息。这一过程虽然不用创建交换机，但会使用默认的交换机，并用默认的直连（default-direct）策略连接队列；

![输入图片说明](http://git.oschina.net/uploads/images/2017/0223/081802_088eb810_1110335.png "在这里输入图片标题")

2. 如下图，发布订阅模型，添加两个队列，分别各用一个消费者监听，设置一个交换机，类型为广播（fanout），交换机会将收到的消息广播给所有相连的队列：

![输入图片说明](http://git.oschina.net/uploads/images/2017/0223/081828_bb1c0dad_1110335.png "在这里输入图片标题")
![输入图片说明](http://git.oschina.net/uploads/images/2017/0223/081836_cf8c1eca_1110335.png "在这里输入图片标题")
![输入图片说明](http://git.oschina.net/uploads/images/2017/0223/081845_581684b4_1110335.png "在这里输入图片标题")

3. direct直连交换机通信模型，包括一个direct交换机，三个binding，两个队列，两个消费者监听器，消息只会被投入到routingkey一致的队列中

 ![输入图片说明](https://git.oschina.net/uploads/images/2017/0902/111518_ec24f2cf_1110335.png "3.png")
 ![输入图片说明](https://git.oschina.net/uploads/images/2017/0902/111713_388a2cb4_1110335.png "5.png")

4.topic主题交换机通信，包括一个topic交换机，三个binding，两个队列，两个消费者监听器，消息只会被投入到routingkey能够匹配的队列中，#表示0个或若干个关键字，*表示一个关键字

![输入图片说明](https://git.oschina.net/uploads/images/2017/0902/122830_278b8f19_1110335.png "4.png")
![输入图片说明](https://git.oschina.net/uploads/images/2017/0902/122904_a0229951_1110335.png "6.png")

5. 进入http://localhost:8080/Spring-rabbitMQ/demo 可向rabbitMQ发送消息，如下图：
 ![输入图片说明](https://git.oschina.net/uploads/images/2017/0902/122918_5adae2c4_1110335.png "QQ截图20170902122553.png")

### 附录：个人作品索引目录（持续更新）

#### 基础篇:职业化，从做好OA系统开始
1. [SpringMVC,Mybatis,Spring三大框架的整合实现增删改查](https://gitee.com/shenzhanwang/SSM)![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题")
2. [Struts2,Hibernate,Spring三大框架的整合实现增删改查](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256f41b457f53f752eee8a79c949e3bccb5) 
3. [Spring,SpringMVC和Hibernate的整合实现增删改查](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256673d1cf49d64c37bed5a9badf9e06386) 
4. [Spring平台整合activiti工作流引擎实现OA开发](https://gitee.com/shenzhanwang/Spring-activiti)![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题")
5. [Spring发布与调用REST风格的WebService](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256a15ad2f399b2629aad6bd6890be26509) 
6. [Spring整合Apache Shiro框架，实现用户管理和权限控制](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572560e15a6a603e2a6aad04c1225dba3a82a) 
7. [使用Spring security做权限控制](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ea1b55249ff5e0aa1098a1b8735fdf79a44e80cff8a13092f3253f494058601e4f800132011545e84b233147817883946) 
8. [Spring整合Jasig CAS框架实现单点登录](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572565fcc6178502fb6bef5570b08591a4518) 
#### 中级篇：中间件的各种姿势
9. [Spring连接mongoDB数据库实现增删改查](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256b40ef1016535817ae51e05c5bf9677d0) 
10. [Spring连接Redis实现缓存](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256ef89d0f29a359796b0213b03dcb76ea7) 
11. [Spring连接图存数据库Neo4j实现增删改查](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572563c588a99507acc91e1539a6116854402) 
12. [Spring平台整合消息队列ActiveMQ实现发布订阅、生产者消费者模型（JMS）](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572561151494a8000934f90156dbe02965f42) 
13. [Spring整合消息队列RabbitMQ实现四种消息模式（AMQP）](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572566af86eaf061f2c7c1a888d6b29fa38c2) 
14. Spring框架的session模块实现集中式session管理 [购买](http://u.720life.cn/g/f0683772ade2d68220b1dc71f0db3b4de02947ed2cdb225cccb737fa7010d3b8) 
15. [Spring整合websocket实现即时通讯](https://gitee.com/shenzhanwang/Spring-websocket)![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题")
16. 使用Spring boot整合mybatis,rabbitmq,redis,mongodb实现增删改查 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5fd2287dab80216f844858260b68e73134) 
17. [Spring MVC整合FastDFS客户端实现文件上传](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256dc08e1d9aa30eaf02c6c12a9a1dd4b0a) 
18. 23种设计模式，源码、注释、使用场景 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5ffc6f6a095564048a8967dd032902b453) 
19. [使用ETL工具Kettle的实例](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e6aa36f44e2202351d5e31f8d62d305ec20cd2db6a5f65a3e7a66472a651d63ac) 
20. Git指南和分支管理策略 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f7c84e86e287270d9a969a25739b7e4f2) 
21. 使用数据仓库进行OLAP数据分析（Mysql+Kettle+Zeppelin） ![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题")[购买](http://t.cn/Ai8Y7dVD)
#### 高级篇：架构之美
22. [zookeeper原理、架构、使用场景和可视化](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ecfadb17f1c4c1dca7f53b58a2b84c96eeb9fabde14737868f33dc431aa8b5d661a2415a183b90c01ddc7949fe7c0fdcd) 
23. Spring boot整合Apache dubbo v2.7实现分布式服务治理（SOA架构） ![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题") [购买](http://t.cn/Ai8YzoYt)
24. 使用Spring Cloud实现微服务架构（MSA架构）![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题")   [购买](http://t.cn/Ai8YzrB6)
25. 使用jenkins+centos+git+maven搭建持续集成环境自动化部署分布式服务 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5fb2cfe53ae79b50eeca3994fc3560bd80) 
26. 使用docker+compose+jenkins+gitlab+spring cloud实现微服务的编排、持续集成和动态扩容 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f08d1d689f4f61a05295b40a13fc92b3e) 
27. 使用FastDFS搭建分布式文件系统（高可用、负载均衡）[购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f66e709d2ac22a8f1f96100c38073e440) 
28. 搭建高可用nginx集群和Tomcat负载均衡 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f630f77db167d73c1847266ec8c7745c4) 
29. 搭建可扩展的ActiveMQ高可用集群 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5facf329109c000c2a003acabef8ca4bbd) 
30. 实现Mysql数据库的主从复制、读写分离、分表分库、负载均衡和高可用 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5fdbde41f49148212053e597e6848e4055) 
31. 搭建高可用redis集群实现分布式缓存 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5fbdfe063ef5233860daf6bef7cf33cde8) 
32. [Spring整合Elastic search实现全文检索](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572568f1f0ba4652542c621706bab4c07233269c40fd054e3893b129482dc5b63a85a) 
#### 特别篇：分布式事务和并发控制
33. 基于可靠消息最终一致性实现分布式事务（activeMQ）[购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5fc1d51d570c8646adf23753d10c840a9d) 
34. 使用TCC框架实现分布式事务（dubbo版）[购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5fd289883308f5f0f00f46903e77d7f26f) 
35. 使用TCC框架实现分布式事务（Spring Cloud版）[购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5fc0c1e76bc8eff16f22b273dc253acb6b) 
36. 决战高并发：数据库锁机制和事务隔离级别的实现![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题") [购买](http://t.cn/Ai8YyAQE)
37. 决战高并发：使用redis实现分布式锁  ![输入图片说明](https://img.shields.io/badge/-%E7%B2%BE%E5%93%81-orange.svg "在这里输入图片标题")[购买](http://t.cn/Ai8Y4bER)
38. 决战高并发：使用zookeeper实现分布式锁 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5ff22be492df2691487db39090722c017c) 
39. 决战高并发：Java多线程编程实例 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f5149938a30350a0132a0104e21317567) 
40. 决战高并发：使用netty实现高性能NIO通信 [购买](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f3a47824ebc3262433a0b2c8947a52371) 

### 快捷入口
[我的网店](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f47c8fde60ca50d588f53fb519b300ca1) 

[购买全套](http://u.720life.cn/g/f3d2956a8781929c275f787580326a5f7f111d52c3d15694450b301dd04472ac) 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)