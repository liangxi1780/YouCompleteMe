 
   
    
   
 

 
  为简化开发工作、提高生产率而生
 

 
   
     
   

   
     
   
 

# 简介 | Intro

Mybatis 增强工具包 - 只做增强不做改变，简化`CRUD`操作

> 技术讨论 QQ 群  492238239、121472998

# 优点 | Advantages

- **无侵入**：Mybatis-Plus 在 Mybatis 的基础上进行扩展，只做增强不做改变，引入 Mybatis-Plus 不会对您现有的 Mybatis 构架产生任何影响，而且 MP 支持所有 Mybatis 原生的特性
- **依赖少**：仅仅依赖 Mybatis 以及 Mybatis-Spring
- **损耗小**：启动即会自动注入基本CURD，性能基本无损耗，直接面向对象操作
- **预防Sql注入**：内置Sql注入剥离器，有效预防Sql注入攻击
- **通用CRUD操作**：内置通用 Mapper、通用 Service，仅仅通过少量配置即可实现单表大部分 CRUD 操作，更有强大的条件构造器，满足各类使用需求
- **多种主键策略**：支持多达4种主键策略（内含分布式唯一ID生成器），可自由配置，完美解决主键问题
- **支持热加载**：Mapper 对应的 XML 支持热加载，对于简单的 CRUD 操作，甚至可以无 XML 启动
- **支持ActiveRecord**：支持 ActiveRecord 形式调用，实体类只需继承 Model 类即可实现基本 CRUD 操作
- **支持代码生成**：采用代码或者 Maven 插件可快速生成 Mapper 、 Model 、 Service 、 Controller 层代码，支持模板引擎，更有超多自定义配置等您来使用（P.S. 比 Mybatis 官方的 Generator 更加强大！）
- **支持自定义全局通用操作**：支持全局通用方法注入（ Write once, use anywhere ）
- **支持关键词自动转义**：支持数据库关键词（order、key......）自动转义，还可自定义关键词
- **内置分页插件**：基于Mybatis物理分页，开发者无需关心具体操作，配置好插件之后，写分页等同于写基本List查询
- **内置性能分析插件**：可输出Sql语句以及其执行时间，建议开发测试时启用该功能，能有效解决慢查询
- **内置全局拦截插件**：提供全表 delete 、 update 操作智能分析阻断，预防误操作

# 文档 | Documentation

[中文](http://u.720life.cn/g/cc2472c166ad93a8385c9f9684a56a6b40ba6d7dfa2fdb6f28fa2e9922b0547f) 

# 原理 | Principle

[Mybatis-Plus 实践及架构原理](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d82864d7b0a38a115d77a4f44d639a2092eb8cd461c5d56ac6c7d8c02dad2fff6e12694436135255e5c3da59ec84f1db5) 

# 应用实例 | Demo

[Spring-MVC](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36b5127c0d2c866f29060e0df89c192e0d9648595f6d3d27c55f08c9e81ae042769a1372062248325b5d5ae0259bfce3bfa) 

[Spring-Boot](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36b5127c0d2c866f29060e0df89c192e0d9648595f6d3d27c55f08c9e81ae042769e26f7adde650159623c7a3262773e181) 

[SSM-实战 Demo](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844dedb554eaa5380af407ad6b5ee46b8fdbead8a72f953ca7f53f0232380fd6d09d) 

# 下载地址 | Download

[点此去下载](http://u.720life.cn/g/7ac6c78c1476cbeebbf102fcae85687908f8bc6fc6dc5aff690809827af2769e38de3f7bc8e057f7ed9bbbfd2cebc3e350608420cf28ee02b2430a5af858cdec) 

```xml
 
     com.baomidou 
     mybatis-plus 
     maven 官方最新版本为准 
 
```

# 结构目录 | Architecture

![项目结构说明](http://git.oschina.net/uploads/images/2016/0821/161516_58956b85_12260.png "项目结构说明")

# 其他开源项目 | Other Project

- [基于Cookie的SSO中间件 Kisso](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d82864d7b0a38a115d77a4f44d639a209d796f7a3ffe355814d2b1f13295b6409) 
- [Java快速开发框架 SpringWind](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844dedb554eaa5380af407ad6b5ee46b8fdbead8a72f953ca7f53f0232380fd6d09d) 
- [基于Hibernate扩展 Hibernate-Plus](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d82864d7b0a38a115d77a4f44d639a2099eff843838d01cca11dde5070b9d7ef6) 

# 期望 | Futures

> 欢迎提出更好的意见，帮助完善 Mybatis-Plus

# 版权 | License

[Apache License 2.0](http://u.720life.cn/g/c0fe1da5278ca9f6360e901f74721f845e8fe6a63a2e42f1caa9cfc3bfda716480d0beb5865d0b08259d3122330d798e) 

# 捐赠 | Donate

> [捐赠记录,感谢你们的支持！](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d82864d7b0a38a115d77a4f44d639a209833f31bdf290bc45e7af0c0799cc299877911a412b44209a351869a7275f42325d4d2e17762890240d17b2599b6c842c) 

![捐赠 mybatis-plus](http://git.oschina.net/uploads/images/2015/1222/211207_0acab44e_12260.png "支持一下mybatis-plus")

# 关注我 | About Me

![程序员日记](http://git.oschina.net/uploads/images/2016/0121/093728_1bc1658f_12260.png "程序员日记")



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)