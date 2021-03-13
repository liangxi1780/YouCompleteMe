# MyBatis通用Mapper3

[![Build Status](https://travis-ci.org/abel533/Mapper.svg?branch=master)](https://travis-ci.org/abel533/Mapper)
[![Maven central](https://maven-badges.herokuapp.com/maven-central/tk.mybatis/mapper/badge.svg)](https://maven-badges.herokuapp.com/maven-central/tk.mybatis/mapper)
[![Dependency Status](https://www.versioneye.com/user/projects/593212c722f278006540a1d1/badge.svg?style=flat)](https://www.versioneye.com/user/projects/593212c722f278006540a1d1)

通用Mapper都可以极大的方便开发人员。可以随意的按照自己的需要选择通用方法，还可以很方便的开发自己的通用方法。

极其方便的使用MyBatis单表的增删改查。

支持单表操作，不支持通用的多表联合查询。

## 新书《MyBatis 从入门到精通》

![MyBatis 从入门到精通](https://github.com/mybatis-book/book/raw/master/book.png)

购买地址：[京东](http://u.720life.cn/g/7b2b4b420a3d295955078cf4db9efbc3a2d0ea6187a984523fe4078276f99a77bf1d201e34ffbafa5ca6ea7a3c9030b3fe275f7fcaf81f6d82ec582e2d6ac71d643a4f94df87a1f8dc3c7aece42064e63f766c27708568f4640273938b792adfb2dcdb2bf90cf05ae6d63f342ba9e92395bfc78fd327748318ae5ac3a2e0f20e7eb88c35398d3edb44b36129815adc3c78a9d405e785bbd5bdf62f004ef277bd527422b45992c8eb74caa6db0005fff075f09c665fa9bc5ac255a4682104220552e31c1289ca558916ca37950e24b819b26be3938c81b0702f801f95f93904702c37f37233eb4ab53c3e724b8f30942a) 

CSDN博客：http://blog.csdn.net/isea533/article/details/73555400

GitHub项目：https://github.com/mybatis-book/book

## 通用 Mapper 支持 Mybatis-3.2.4 及以上版本
## 不是表中字段的属性必须加 `@Transient` 注解

## Spring DevTools 配置
感谢[emf1002](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c125477c8cc9c0d254058af2ba593fa4b1ca9875b44a1d0f37cf4d27f75596fea8d7cd2aa0aa856440c000ff6b1eb1d8 

在使用 DevTools 时，通用Mapper经常会出现 `class x.x.A cannot be cast to x.x.A`。

同一个类如果使用了不同的类加载器，就会产生这样的错误，所以解决方案就是让通用Mapper和实体类使用相同的类加载器即可。

DevTools 默认会对 IDE 中引入的所有项目使用 restart 类加载器，对于引入的 jar 包使用 base 类加载器，因此只要保证通用Mapper的jar包使用 restart
类加载器即可。

在 `src/main/resources` 中创建 META-INF 目录，在此目录下添加 spring-devtools.properties 配置，内容如下：
```properties
restart.include.mapper=/mapper-[\\w-\\.]+jar
restart.include.pagehelper=/pagehelper-[\\w-\\.]+jar
```
使用这个配置后，就会使用 restart 类加载加载 include 进去的 jar 包。

## 项目文档

### https://mapperhelper.github.io

在你打算使用通用 Mapper 前，一定要看看下面的文档，许多人在初次使用时遇到的问题，99% 都在文档中有说明！！

1. [如何集成通用Mapper](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db5188662b30f0a9c654025bb4c0b8bc12a0bd4d0ceb47ec3a124213a49998105e7) 
2. [如何使用通用Mapper](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db594fac672191cd2c052b8b77a074114f05497b7e115db7fceb344c7a28ddffe4e) 
2. [3.3.0版本新增功能用法文档](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db58c76315b5511288340056316e0598312bf92dab9edba1419604bd74d789c2d41) 
3. [根据需要自定义接口](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db5fdb7fe1c3020dce90bd578fe22dd74761b70c0f82f76854625b715ba8a216669) 
4. [Mapper3通用接口大全](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db5247f24286bff4644a10cd8804ad3d5b06544bce7d2c9f10f8193287d55b3e32e) 
5. [扩展通用接口](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db58951418244edb1a4e342f26cc9c9fa984c12b20536a2e7c6a63075b20f6511c8) 
6. [使用Mapper专用的MyBatis生成器插件](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db5e37901a4dd27daeb77e7c53397027cac0e771984fcc5da274f5dff1bda713ad7) 
7. [在Spring4中使用通用Mapper](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd4035b3450e6f64c21ad9b3bd9e9ddd4e210fa51140a876666d891bab29c76f36ad928d918face138a08a71a9dd2c32fffef) 
8. [Mapper3常见问题和用法](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db5173d382f2b9d28457d559e23d853b0f7f8be8b0222fa14b51b518debad619839) 

### 如何让作者为你开发通用方法？

实际上，只要你看看上面的第 6 个文档，你完全可以自己开发出来。

或者你可以通过赞助作者 10~50 元来让作者根据你的需求开发**一个**通用方法。

赞助后保留截图，将截图和需求内容发邮件到 abel533@gmail.com 和作者联系。

你还可以通过开源中国众包购买服务[开发 MyBatis 通用 Mapper 通用方法](http://u.720life.cn/g/01c4f4dfc91fba8d52cad17b954b3c4c6bada3db2c6817acd0c15b747ca91fd9d7b40ddd2734a67abf9e1480982ea8176e2e57d35791be003ccaa5b9c76868be) 

## 通用 Mapper - 简单用法示例

全部针对单表操作，每个实体类都需要继承通用Mapper接口来获得通用方法。

示例代码：

    CountryMapper mapper = sqlSession.getMapper(CountryMapper.class);
    //查询全部
    List  countryList = mapper.select(new Country());
    //总数
    Assert.assertEquals(183, countryList.size());

    //通用Example查询
    Example example = new Example(Country.class);
    example.createCriteria().andGreaterThan("id", 100);
    countryList = mapper.selectByExample(example);
    Assert.assertEquals(83, countryList.size());

    //MyBatis-Generator生成的Example查询
    CountryExample example2 = new CountryExample();
    example2.createCriteria().andIdGreaterThan(100);
    countryList = mapper.selectByExample(example2);
    Assert.assertEquals(83, countryList.size());

CountryMapper代码如下：

    public interface CountryMapper extends Mapper  {
    }

这里不说更具体的内容，如果您有兴趣，可以查看下面的 项目文档 

## 实体类注解

从上面效果来看也能感觉出这是一种类似hibernate的用法，因此也需要实体和表对应起来，因此使用了JPA注解。更详细的内容可以看下面的 项目文档 。

Country代码：

    public class Country {
        @Id
        private Integer id;
        @Column
        private String countryname;
        private String countrycode;
        //省略setter和getter方法
    }
    
[使用Mapper专用的MyBatis Generator插件](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db5e37901a4dd27daeb77e7c53397027cac0e771984fcc5da274f5dff1bda713ad7)  可以方便的生成这些（带注解的）实体类。

## 使用 Maven
```xml
 
     tk.mybatis 
     mapper 
     最新版本 
 
```
如果你使用 Spring Boot 可以直接引入：
```xml
 
 
     tk.mybatis 
     mapper-spring-boot-starter 
     最新版本 
 
```
具体用法可以参考：[MyBatis-Spring-Boot](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469b5c2f2d461134b0dd9e74580a9555661873e5a72c81c218eb097340da4e6ed7)  

## 引入 Jar 包，下载地址：

https://oss.sonatype.org/content/repositories/releases/tk/mybatis/mapper

http://repo1.maven.org/maven2/tk/mybatis/mapper

由于通用Mapper依赖JPA，所以还需要下载persistence-api-1.0.jar：

http://repo1.maven.org/maven2/javax/persistence/persistence-api/1.0/

## [更新日志](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d9dd92fe5a8305dae04a7e26aadecd403f827e047e6d734c548f072fb345d5db5e81d35833eeb1ba9c7774ca7e6976383) 

##作者信息

MyBatis 工具网站:[http://mybatis.tk](http://u.720life.cn/g/5d88e5a59ccc688f2e74c4a956a26a21614412bd4b91ddfa786780e41f99f519) 

作者博客：http://blog.csdn.net/isea533

作者邮箱： abel533@gmail.com

如需加群，请通过 http://mybatis.tk 首页按钮加群。

推荐使用Mybatis分页插件:[PageHelper分页插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e46d295ad2841af2558737b9b48e7f525f5d9e37bc321a699ae434b02ff50941) 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)