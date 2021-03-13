# Spring-neo4j
 作为Nosql家族的一员，图存数据库在推荐系统，社交关系等领域拥有广泛应用。本项目基于Spring-data-neo4j,整合图存数据库Noe4j，
 实现增删改查的功能。主要功能包括：
 
 1.基于spring-data-neo4j 3.2.0通过REST远程连接Neo4j服务器，并非嵌入式连接；
 
 2.创建接口用于创建一个简单的图存数据库，实现一个中心点到其他十个点的连接；
 
 3.提供删除接口，可删除所有点和边；
 
 4.提供查询操作，可按照点的属性查找对应的点。
 
 5.创建接口
 http://localhost:8080/Spring-neo4j/create
 
 删除接口
 http://localhost:8080/Spring-neo4j/delete
 
 创建后到neo4j控制台查看的效果图
![输入图片说明](http://git.oschina.net/uploads/images/2017/0209/090929_a6f0e164_1110335.jpeg "在这里输入图片标题")

### 附录：个人作品索引目录（持续更新）

#### 基础篇:职业化，从做好OA系统开始
1. [SpringMVC,Mybatis,Spring三大框架的整合实现增删改查](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572561792735261a32bb4eb77fa95835490c5) 
2. [Struts2,Hibernate,Spring三大框架的整合实现增删改查](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256f41b457f53f752eee8a79c949e3bccb5) 
3. [Spring,SpringMVC和Hibernate的整合实现增删改查](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256673d1cf49d64c37bed5a9badf9e06386) 
4. [Spring平台整合activiti工作流引擎实现OA开发](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572569186b5133b3133627b659352d032f45a) 
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
14. Spring框架的session模块实现集中式session管理（[购买]https://www.fageka.com/store/item/s/id/fwW1QEK2848.html)）
15. [Spring整合websocket实现即时通讯](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256aa1410207072711266bc55b5923ad248) 
16. 使用Spring boot整合mybatis,rabbitmq,redis,mongodb实现增删改查（[购买]https://www.fageka.com/store/item/s/id/0feQDHL1913.html)）
17. [Spring MVC整合FastDFS客户端实现文件上传](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca5357256dc08e1d9aa30eaf02c6c12a9a1dd4b0a) 
18. 23种设计模式，源码、注释、使用场景（[购买]https://www.fageka.com/store/item/s/id/TuSSL2r3330.html)）
19. [使用ETL工具Kettle的实例](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e6aa36f44e2202351d5e31f8d62d305ec20cd2db6a5f65a3e7a66472a651d63ac) 
20. Git指南和分支管理策略（[购买]https://www.fageka.com/store/item/s/id/Z7uh2iF1620.html)）
#### 高级篇：架构之美
21. [zookeeper原理、架构、使用场景和可视化](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ecfadb17f1c4c1dca7f53b58a2b84c96eeb9fabde14737868f33dc431aa8b5d661a2415a183b90c01ddc7949fe7c0fdcd) 
22. Spring框架整合dubbo框架实现分布式服务治理（SOA架构）（[购买]https://www.fageka.com/store/item/s/id/tTEHOF42241.html)）
23. Spring框架整合dubbox实现微服务架构（MSA架构）
24. 使用Spring Cloud实现微服务架构（MSA架构）（[购买]https://www.fageka.com/store/item/s/id/5T5cEY80304.html)）
25. 使用jenkins+centos+git+maven搭建持续集成环境自动化部署分布式服务（[购买]https://www.fageka.com/store/item/s/id/TvLt0pr4205.html)）
26. 使用docker+compose+jenkins+gitlab+spring cloud实现微服务的编排、持续集成和动态扩容（[购买]https://www.fageka.com/store/item/s/id/7Gi4FeN2111.html)）
27. 使用FastDFS搭建分布式文件系统（高可用、负载均衡）（[购买]https://www.fageka.com/store/item/s/id/sAKgl2n4209.html)）
28. 搭建高可用nginx集群和Tomcat负载均衡（[购买]https://www.fageka.com/store/item/s/id/78bvd6N2534.html)）
29. 搭建可扩展的ActiveMQ高可用集群（[购买]https://www.fageka.com/store/item/s/id/H1nWZ4j4443.html)）
30. 实现Mysql数据库的主从复制、读写分离、分表分库、负载均衡和高可用（[购买]https://www.fageka.com/store/item/s/id/lojrGCH2016.html)）
31. 搭建高可用redis集群实现分布式缓存（[购买]https://www.fageka.com/store/item/s/id/02HwT2W4038.html)）
32. [Spring整合SolrJ实现全文检索](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee47c28d44de0f80ef0769f7ca53572567287290147f1680b3b9f66a4e0a2585e) 
#### 特别篇：分布式事务和并发控制
33. 基于可靠消息最终一致性实现分布式事务（activeMQ）（[购买]https://www.fageka.com/store/item/s/id/qwCZgHD2224.html)）
34. 使用TCC框架实现分布式事务（dubbo版）（[购买]https://www.fageka.com/store/item/s/id/woVwDpD0145.html)）
35. 使用TCC框架实现分布式事务（Spring Cloud版）（[购买]https://www.fageka.com/store/item/s/id/VZ4lvg40739.html)）
36. 决战高并发：数据库锁机制和事务隔离级别的实现（[购买]https://www.fageka.com/store/item/s/id/Xvk7DZI2400.html)）
37. 决战高并发：使用redis实现分布式锁（[购买]https://www.fageka.com/store/item/s/id/uFQStQ61656.html)）
38. 决战高并发：使用zookeeper实现分布式锁（[购买]https://www.fageka.com/store/item/s/id/NQp8kpF1940.html)）
39. 决战高并发：Java多线程编程实例（[购买]https://www.fageka.com/store/item/s/id/k6MzK041644.html)）
40. 决战高并发：使用netty实现高性能NIO通信（[购买]https://www.fageka.com/store/item/s/id/VtwnbVN5319.html)）

### 网店入口
[我的网店](http://u.720life.cn/g/5d49be387f8da10d3acd1a25d7d4e61a6d6eeda40130b321e210ff1eb569a01d7271e5ee320e6b6586ea20e98a37eff1f4b89b32fad09062753e706f6bef1fb2) 
   


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)