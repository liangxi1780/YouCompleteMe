Raincat
================

强一致性分布式事务，是基于二阶段提交+本地事务补偿机制来实现。[原理介绍](http://u.720life.cn/g/1d13e76a13ae86e9083de47d983e00c4a8b39976f650b7971b93251da4c9ac5625ff9bfc8057af98bf18204b42b9949f) 

基于java语言来开发（JDK1.8），支持dubbo,motan,springcloud进行分布式事务。

#####  因为文件名太长，大家在拉取代码的时候执git命令：git config --global core.longpaths true

 # Features

  * **框架特性**

      * 无缝集成spring 或 spring boot。

      * 支持dubbo,motan,springcloud,等rpc框架进行分布式事务。

      * 事务发起者，参与者与协调者底层基于netty长连接通信,稳定高效。

      * 协调者采用eureka做注册中心，支持集群模式。

      * 采用Aspect AOP 切面思想与Spring无缝集成。

      * 配置简单，集成简单，源码简洁，稳定性高，已在生产环境使用。

      * 内置经典的分布式事务场景demo工程，并有swagger-ui可视化界面可以快速体验。


 * ***事务角色***

   * 事务发起者（可理解为消费者 如：dubbo的消费者,springcloud的调用方）,发起分布式事务

   * 事务参与者（可理解为提供者 如：dubbo的提供者,springcloud的rest服务提供者),参与事务发起者的事务

   * 事务协调者（tx-manager），协调分布式事务的提交，回滚等。

 * ***技术方案***

   * 协调者（tx-manager）采用eureka作为注册中心，集群配置，达到服务的高可用，采用redis集群来分布式存储事务数据, springboot 提供rest服务，采用netty与参与者，发起者进行长连接通信。

   * 发起者与协调者，采用Aspect AOP 切面思想，SPI，多线程，异步回调，线程池，netty通信等技术。


 * ***SPI扩展***
     * 本地事务恢复，支持redis，mogondb，zookeeper，file，mysql等关系型数据库
     * 本地事务序列化保存，支持java，hessian，kryo，protostuff
     * netty通信序列化方式，支持 hessian，kryo，protostuff

# Design
 ### [架构设计](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462542e68d43df680e383f411732c3f0ac62764c27927cb3b2b6b515df94ada02f) 


# 视频源码分析

 ### [环境搭建](http://u.720life.cn/g/ec8323bf01e557101190483f2a3ac3745d672dcebde67e9e0a661b24834be21a6569a27ab40e79ddee8181ad59a9e0b8) 
 
 ### [启动过程](http://u.720life.cn/g/ec8323bf01e557101190483f2a3ac3746d25219a3d1bfbc37bd215d23df5818f9641b70a9dbb17797beaefe93f89d152) 
 
 ### [事务提交](http://u.720life.cn/g/ec8323bf01e557101190483f2a3ac37486d9b600c9a047c00ea750583eabbc5e34d728237a29e5d757d99b1ea6e43789) 
 
 ### [回滚恢复](http://u.720life.cn/g/ec8323bf01e557101190483f2a3ac37488e32c152b61f2a71d94ed07cff77756ca7d3c10c4660a17593cdb8edea489f6) 
 
 ### [管理后台](http://u.720life.cn/g/ec8323bf01e557101190483f2a3ac374e5f3903a63d3519456d55b424e615a83925835bcc5d9eb72466c7a829e7a0848) 
 
# 流程图

 ![](https://yu199195.github.io/images/Raincat/2pc.png)

#   Configuration

  ###  [配置详解](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462542e68d43df680e383f411732c3f0ac298cb67352872de73d3b6b29af4f083c56a812f2ce9b103e3c5b91d06c72e1d5571f450d39657c0b42adcc780e2c660a491b7854837f1e1694bf0359372ba3e33286bc0e513b2024081ecd64feb8a445) 

# Spring-Boot-Starter-Support

   * ### [Spring-Boot-Starter](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462542e68d43df680e383f411732c3f0ac0ea0ef704b08e57d0023dd9207a7b09694a2aecd800b7a8f13bce58e3e28e108) 

# Prerequisite

  *   #### JDK 1.8+

  *   #### Maven 3.2.x

  *   #### Git

  *   ####  RPC framework dubbo or motan or springcloud。

# Quick Start

   * ### Clone & Build
      ```
      > git clone https://github.com/yu199195/Raincat.git

      > cd Raincat

      > mvn -DskipTests clean install -U
      ```

   ### [快速体验(dubbo)](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462542e68d43df680e383f411732c3f0acdaaf857b8023643a6951db56be03ba45fda6ca9f32bbfb831276eca96fd7f6d05d2ecc7f2eeb8cea24752741c6eef3d4) 

   ### [快速体验(springcloud)](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462542e68d43df680e383f411732c3f0acdaaf857b8023643a6951db56be03ba455d5ee418ce7f60164b5557b07880c78bed0b6dd03ad36b0e50cafc4d460806bdc7cc3e3aaafe6b40bad0a36a67689981) 


# User Guide

###  [dubbo 用户](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462542e68d43df680e383f411732c3f0acbf08a37070115621124be3ba9bf984f1147a2ed436d1ec28d54008479222ba41fdef6c371b4b3b1a9ccbd56c2d9f379c1603314f76884e433d633d923efd873c) 

###  [springcloud 用户](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462542e68d43df680e383f411732c3f0ac01a8e22ffbc4380294307913927246ebc2a7e177354c961e93a9e9a31c1e7c41db739d7e0aa61691d5f7b938248affa61a2440c1c4967b3fe970da3d3da6c1ce) 






# FAQ

* ### 为什么我下载的代码后，用idea打开没有相应的get set 方法呢？
   ##### 答：因为框架使用了Lombok包，它是在编译的时期，自动生成get set方法，并不影响运行，如果觉得提示错误难受，请自行下载lombok包插件，[lombok官网](http://u.720life.cn/g/38e2c0a1caffcef70ab67997ff249482191ef76f813957d36ffa94cc0fd5036e) 

* ### 为什么我运行demo工程，找不到applicationContent.xml呢？
  ##### 答：请设置项目的资源文件夹。

* ### 为什么我启动admin项目的时候，会报mongo 集群连接错误呢？
  ##### 答：这是因为项目里面有mongo代码，spring boot会自动配置，该错误没有关系，只要admin项目能正常启动就行。


# Support

 * ###  如有任何问题欢迎加入QQ群进行讨论
   ![](https://yu199195.github.io/images/qq.png)

 * ###  微信公众号
   ![](https://yu199195.github.io/images/public.jpg)

 # Contribution



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)