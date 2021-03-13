happylifeplat-tcc
================

碧桂园旺生活平台解决分布式事务方案之tcc开源框架。基于java语言来开发（JDK1.8），支持dubbo，springcloud等rpc框架进行分布式事务。
#####   因为文件名太长，大家在拉取代码的时候执git命令：git config core.longpaths true

 # Features

 * **框架特性**

     * 支持dubbo，springcloud等rpc框架进行分布式事务。

     * 采用Aspect AOP 切面思想与Spring无缝集成，天然支持集群。

     * 配置简单，集成简单，源码简洁，稳定性高，已在生产环境使用。

     * 内置经典的分布式事务场景demo工程，并有swagger-ui可视化界面可以快速体验。


 * **SPI扩展**
     * 本地事务存储，支持redis，mogondb，zookeeper，file，mysql等关系型数据库
     * 序列化方式，支持java，hessian，kryo，protostuff


# TCC原理介绍
  ####  [原理介绍](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e68ab3dd59df75461e3ec1e1ab78a2e344e8104a95ae51a886076f528e5cfdcbbed149f407ebc1b2e01a5de6dd0d36e2b2c68c0991594f6c68ae828f3095587eeb49975c3b58303aec072b0d57965c81) 

#   Configuration

  ####  [配置详解](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e68ab3dd59df75461e3ec1e1ab78a2e344e8104a95ae51a886076f528e5cfdcb26a9e27dd332b8437bc5d493b95d21355059b7df7b4aad2637700df852c14ac55444196175afa70dd1400175f1be395d) 

# Usage

   ### [快速体验(dubbo)](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e68ab3dd59df75461e3ec1e1ab78a2e344e8104a95ae51a886076f528e5cfdcb198769747160e0b7606d1443df51416b0d67087261a5e0719968404fd9c5829819fe01eb520349144dcd460c8d9b23f13787fd851ebe5f1641b626705eec3c04) 

   ### [快速体验(springcloud)](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e68ab3dd59df75461e3ec1e1ab78a2e344e8104a95ae51a886076f528e5cfdcb198769747160e0b7606d1443df51416b0d67087261a5e0719968404fd9c5829819fe01eb520349144dcd460c8d9b23f1b7c75ff778f9900fddff48ba8a3359f652ba778f2d4549ac041df642e13b4688) 


 # Support
   ##### 如有任何问题欢迎加入QQ群：162614487 进行讨论


 # Contribution



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)