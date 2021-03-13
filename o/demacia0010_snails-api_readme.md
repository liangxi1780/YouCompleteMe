### 源码仓库已迁移到 [gitee.com/kuzank](gitee.com/kuzank)，此账号下的工程不再提供维护，请移步访问[gitee.com/kuzank](gitee.com/kuzank)


# snails-api
`snails-api` 为 `snails-web` 提供后台 `REST API` 接口

- `Snails 框架`：是一个基于 Spring-Boot + Angular + Ng-Zorro 前后端分离项目的简单实现
- `snails-web 前端`：[Angular](http://u.720life.cn/g/8fd75c07dc4cbb8ed759f099d2fc1cb1505e2651b3049745325a8342ce05f7dd)  + [Ng-Zorro](http://u.720life.cn/g/8924562f6e22955b64d005dfba7246deb96eddf82b770577e49d5f3fdc610fee1613b4af3c6d2079d5eb38bb12a3cc8f)  + [Ng-Alain](http://u.720life.cn/g/0b1496ac89232028b6a7a545d7074fc261be794acce5fc95f197b3ff5bd57743) 
- `snails-api 后台`：[SpringBoot](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d74791681f9785d83f6cd6c957366ad1debb29bb8c32cd47aff960e71f7893090)  + [JPA ](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263dbe905ae631048feaf69eced65a71a46eab8b80b596b0c8a17472dc8d0797c9bc379530e7442dda3a724927e2b2a878d1  [lombok](http://u.720life.cn/g/9cec729ef2d3c72b70f7caf7a64fe54c004be7f5a331560d74f301adfc8849d5)  + [Java8](http://u.720life.cn/g/85a9f52868358c3208a4b5fd9062e993cf51ed4e030337272b88113597fbb3d1)  + Mysql

|      `框架源码`     | Gitee                                                        | GitHub                                                       |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Snails** 框架      | [https://gitee.com/kuzank/snails](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e49c99e6e9eb9317b92274a30119450cd)  | [https://github.com/kuzank/snails](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5258bf9a5de373b76594c11d8098808)  |
| **Snails-web** 前端  | [https://gitee.com/kuzank/snails-web](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e768e56463b2f073a32f3e05f21ed7d1938e82c3349438b20d7b701eae9a00bea)  | [https://github.com/kuzank/snails-web](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5258bf9a5de373b76594c11d80988084a8e149c4299288723b3a3a93fd338fc)  |
| **Snails-api**  后台 | [https://gitee.com/kuzank/snails-api](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e768e56463b2f073a32f3e05f21ed7d1900acafd0f6dac2dbed958e00ff81f8b4)  | [https://github.com/kuzank/snails-api](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5258bf9a5de373b76594c11d809880837a7362b4d9e40179cf3ed1cea6e6a14)  |

## 开发环境要求
- Java 8
- Maven
- Mysql

## Mysql 数据库初始化
```sql
CREATE DATABASE IF NOT EXISTS snails DEFAULT CHARSET utf8 COLLATE utf8_general_ci;
grant all privileges on snails.* to 'root'@'%' identified by '123456';
flush privileges;
```

## 启动程序 - 方法一
前提：系统已安装 docker

注意：若 mysql 运行在 docker 中，会出现错误，docker 两个实例之间不能互相访问，需要进行配置处理
```shell script
# maven 清理
mvn clean;
# 打包为 docker 镜像
mvn package docker:build
# 启动程序
docker run -d --name snails-api -p 8081:8081 -t snails-api
# 查看运行中的 docker 实例
docker ps -a 
```

## 启动程序 - 方法二
```shell script
maven clean;     # maven 清理
maven package    # 打包
# 启动程序
java -jar target/snails-0.1.jar
```

## 启动程序 - 方法三
![](https://images.gitee.com/uploads/images/2020/0210/145459_d1a54739_2129289.jpeg)
```shell script
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v2.2.2.RELEASE)

2020-01-14 15:27:32.381  WARN 29267 --- [  restartedMain] o.s.boot.StartupInfoLogger               : InetAddress.getLocalHost().getHostName() took 5006 milliseconds to respond. Please verify your network configuration (macOS machines may need to add entries to /etc/hosts).
2020-01-14 15:27:37.387  INFO 29267 --- [  restartedMain] com.kuzank.snails.SnailsApplication      : Starting SnailsApplication on fanghaoshengdeMacBook-Pro.local with PID 29267 (/Users/kuzan/Documents/snails/snails-api/target/classes started by kuzan in /Users/kuzan/Documents/snails/snails-api)
2020-01-14 15:27:37.388  INFO 29267 --- [  restartedMain] com.kuzank.snails.SnailsApplication      : No active profile set, falling back to default profiles: default
2020-01-14 15:27:37.460  INFO 29267 --- [  restartedMain] o.s.b.devtools.restart.ChangeableUrls    : The Class-Path manifest attribute in /Users/kuzan/.m2/repository/org/glassfish/jaxb/jaxb-runtime/2.3.2/jaxb-runtime-2.3.2.jar referenced one or more files that do not exist: file:/Users/kuzan/.m2/repository/org/glassfish/jaxb/jaxb-runtime/2.3.2/jakarta.xml.bind-api-2.3.2.jar,file:/Users/kuzan/.m2/repository/org/glassfish/jaxb/jaxb-runtime/2.3.2/txw2-2.3.2.jar,file:/Users/kuzan/.m2/repository/org/glassfish/jaxb/jaxb-runtime/2.3.2/istack-commons-runtime-3.0.8.jar,file:/Users/kuzan/.m2/repository/org/glassfish/jaxb/jaxb-runtime/2.3.2/stax-ex-1.8.1.jar,file:/Users/kuzan/.m2/repository/org/glassfish/jaxb/jaxb-runtime/2.3.2/FastInfoset-1.2.16.jar,file:/Users/kuzan/.m2/repository/org/glassfish/jaxb/jaxb-runtime/2.3.2/jakarta.activation-api-1.2.1.jar
2020-01-14 15:27:37.460  INFO 29267 --- [  restartedMain] .e.DevToolsPropertyDefaultsPostProcessor : Devtools property defaults active! Set 'spring.devtools.add-properties' to 'false' to disable
2020-01-14 15:27:37.460  INFO 29267 --- [  restartedMain] .e.DevToolsPropertyDefaultsPostProcessor : For additional web related logging consider setting the 'logging.level.web' property to 'DEBUG'
2020-01-14 15:27:37.974  INFO 29267 --- [  restartedMain] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFAULT mode.
2020-01-14 15:27:38.055  INFO 29267 --- [  restartedMain] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 74ms. Found 6 JPA repository interfaces.
2020-01-14 15:27:38.322  INFO 29267 --- [  restartedMain] trationDelegate$BeanPostProcessorChecker : Bean 'org.springframework.transaction.annotation.ProxyTransactionManagementConfiguration' of type [org.springframework.transaction.annotation.ProxyTransactionManagementConfiguration] is not eligible for getting processed by all BeanPostProcessors (for example: not eligible for auto-proxying)
2020-01-14 15:27:38.586  INFO 29267 --- [  restartedMain] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8081 (http)
2020-01-14 15:27:38.594  INFO 29267 --- [  restartedMain] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2020-01-14 15:27:38.594  INFO 29267 --- [  restartedMain] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.29]
2020-01-14 15:27:38.661  INFO 29267 --- [  restartedMain] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2020-01-14 15:27:38.662  INFO 29267 --- [  restartedMain] o.s.web.context.ContextLoader            : Root WebApplicationContext: initialization completed in 1201 ms
2020-01-14 15:27:38.821  INFO 29267 --- [  restartedMain] o.hibernate.jpa.internal.util.LogHelper  : HHH000204: Processing PersistenceUnitInfo [name: default]
2020-01-14 15:27:38.973  INFO 29267 --- [  restartedMain] org.hibernate.Version                    : HHH000412: Hibernate Core {5.4.9.Final}
2020-01-14 15:27:39.071  INFO 29267 --- [  restartedMain] o.hibernate.annotations.common.Version   : HCANN000001: Hibernate Commons Annotations {5.1.0.Final}
2020-01-14 15:27:39.151  INFO 29267 --- [  restartedMain] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2020-01-14 15:27:39.263  INFO 29267 --- [  restartedMain] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Start completed.
2020-01-14 15:27:39.274  INFO 29267 --- [  restartedMain] org.hibernate.dialect.Dialect            : HHH000400: Using dialect: org.hibernate.dialect.MySQL5InnoDBDialect
2020-01-14 15:27:40.028  INFO 29267 --- [  restartedMain] o.h.e.t.j.p.i.JtaPlatformInitiator       : HHH000490: Using JtaPlatform implementation: [org.hibernate.engine.transaction.jta.platform.internal.NoJtaPlatform]
2020-01-14 15:27:40.033  INFO 29267 --- [  restartedMain] j.LocalContainerEntityManagerFactoryBean : Initialized JPA EntityManagerFactory for persistence unit 'default'
2020-01-14 15:27:40.058  INFO 29267 --- [  restartedMain] o.s.b.d.a.OptionalLiveReloadServer       : LiveReload server is running on port 35729
2020-01-14 15:27:40.699  WARN 29267 --- [  restartedMain] JpaBaseConfiguration$JpaWebConfiguration : spring.jpa.open-in-view is enabled by default. Therefore, database queries may be performed during view rendering. Explicitly configure spring.jpa.open-in-view to disable this warning
2020-01-14 15:27:40.881  INFO 29267 --- [  restartedMain] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8081 (http) with context path ''
2020-01-14 15:27:40.884  INFO 29267 --- [  restartedMain] com.kuzank.snails.SnailsApplication      : Started SnailsApplication in 18.837 seconds (JVM running for 24.498)
2020-01-14 15:27:41.029  INFO 29267 --- [  restartedMain] com.kuzank.snails.init.DBInit            : ApplicationReadyEvent : init DB successful !
```


## 学习资源
- [Angular快速上手](http://u.720life.cn/g/8fd75c07dc4cbb8ed759f099d2fc1cb1038975cd0ffe4d0438674a605a2cefd89cd80d7f0fe6b0c457567c77f597a4d2) 
- [Ng-Zorro](http://u.720life.cn/g/8924562f6e22955b64d005dfba7246deb96eddf82b770577e49d5f3fdc610fee1613b4af3c6d2079d5eb38bb12a3cc8f) 
- [Ng-Alain](http://u.720life.cn/g/0b1496ac89232028b6a7a545d7074fc2474a862c01fbda319c5090f80e7f5bc6) 
- [Sprint系列-程序员DD](http://u.720life.cn/g/43cbeb0b30a8046cf65fde9a4dd1cf2e362d2970b1cbb0718e7a080e081d2de5) 
- [Sprint系列-纯洁的微笑](http://u.720life.cn/g/a7aa90cf5fe79726b10a2a75b316765703c7dcb58f135471010b7a077e999b3059fa78805c53afcf8a354628c6041f5f) 
- [Java8](http://u.720life.cn/g/85a9f52868358c3208a4b5fd9062e993cf51ed4e030337272b88113597fbb3d1) 
- [lombok](http://u.720life.cn/g/8a0e6e781ca1335d5641e0f9d5e96ab910cc07fec2381979ee0eccaedb31c24e60bef370e29737e0298e092aaf954066) 
- [SpringBoot 中 JPA 的使用](http://u.720life.cn/g/8a0e6e781ca1335d5641e0f9d5e96ab914e5bbae167cd5fd72c38691f6d3d6b61ca31c7daccd60736ff69f1b43a666e9) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)