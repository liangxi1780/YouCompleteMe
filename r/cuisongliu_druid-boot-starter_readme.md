[![Build Status](https://travis-ci.org/cuisongliu/druid-boot-starter.svg?branch=master)](https://travis-ci.org/cuisongliu/druid-boot-starter)
[![Dependency Status](https://www.versioneye.com/user/projects/5918687ae1638f0051a0a62c/badge.svg?style=flat-square)](https://www.versioneye.com/user/projects/5918687ae1638f0051a0a62c)
[![license](https://img.shields.io/badge/gradle-3.3-brightgreen.svg)](https://gradle.org)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://opensource.org/licenses/mit-license.php)

#  [Druid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a)   integration  with springboot

Druid-Spring-Boot-Starter 帮助你集成通用 [Druid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a)  到 Spring Boot。

Druid-Spring-Boot-Starter will help you use [Druid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a)  with Spring Boot.

## How to use

### maven

在pom.xml加入nexus资源库（解决中国访问慢的问题,已经加入中央仓库）

Add the following nexus repository(fix china access slow problem,already append to central nexus.)  to your pom.xml:

     
         
             nexus 
             nexus 
             http://maven.cuisongliu.com/content/groups/public 
             
                 true 
             
             
                 false 
             
         
     

在pom.xml加入依赖

Add the following dependency to your pom.xml:

     
        com.cuisongliu 
        druid-spring-boot-starter 
        1.1.0 
      

### gradle

在build.gradle加入nexus资源库（解决中国访问慢的问题,已经加入中央仓库）

Add the following nexus repository(fix china access slow problem,already append to central nexus.)  to your build.gradle:

    allprojects {
        repositories {
            mavenLocal()
            maven { url "http://maven.cuisongliu.com/content/groups/public" }
            mavenCentral()
            jcenter()
        }
    }
    
在build.gradle加入依赖

Add the following dependency to your build.gradle:
    
    compile "com.cuisongliu:druid-spring-boot-starter:1+"
    
### springboot properties set

在application.properties 或者application.yml加入[相关参数](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62aa8b46fdf220c8e4dcaa1eff97908b86992db072770c891715d190e425678c7939f4ee5a266e996561f1ed38b9d193d179e213a71cd4ba9527387d49ed3897f6a8cdc481cb0b77f190a36c3abb91a35dc) 

at  application.properties or application.yml append some properties.

| properties | IsNull? | Defaults |
| :------|:------|:------|
|spring.datasource.url|no|null|
|spring.datasource.username|no|null|
|spring.datasource.password|no|null|
|spring.datasource.druid.max-active|yes|8|
|spring.datasource.druid.min-idle|yes|0|
|spring.datasource.druid.initial-size|yes|0|
|spring.datasource.druid.max-wait|yes|-1|
|spring.datasource.druid.time-between-eviction-runs-millis|yes|60 * 1000L|
|spring.datasource.druid.max-open-prepared-statements|yes|-1|
|spring.datasource.druid.test-on-borrow|yes|false|
|spring.datasource.druid.validation-query|yes|null|
|spring.datasource.druid.test-on-return|yes|false|
|spring.datasource.druid.test-while-idle|yes|true|
|spring.datasource.druid.pool-prepared-statements|yes|false|
|spring.datasource.druid.filters|yes|false|
|spring.datasource.druid.max-pool-prepared-statement-per-connection-size|yes|-1|
|spring.datasource.druid.validation-query-timeout|yes|-1|
|spring.datasource.druid.min-evictable-idle-time-millis|yes|1000L * 60L * 30L|
|spring.datasource.druid.connection-properties|yes|null|

sql slow config:

    spring:
     datasource:
        druid:
          connection-properties:
            - druid.stat.mergeSql=true
            - druid.stat.slowSqlMillis=5000

[servlet properties](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a33fe67d7bd83a2bf034cf792bf5d163130e461bd1f40bd3532b775c3c4fbbbfeaf49d6e37c03b85dc553d2a5232df9a0da32b9b1dae91b7afe4867e29749fb9a) 

| properties | IsNull? | Defaults |
| :------|:------|:------|
|spring.datasource.druid.servlet.enable|yes|true|
|spring.datasource.druid.servlet.url-mappings|yes|/druid/*|
|spring.datasource.druid.servlet.allow|yes|null|
|spring.datasource.druid.servlet.deny|yes|null|
|spring.datasource.druid.servlet.login-username|yes|null|
|spring.datasource.druid.servlet.login-password|yes|null|
|spring.datasource.druid.servlet.reset-enable|yes|null|

[filter properties](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a33fe67d7bd83a2bf034cf792bf5d16317d447e5ba5732bf71ef00c5185b0c372ce7fe1526aa5d08168d9fd602ff9942888ac28d96eeb18da2d965e79d8b77acd) 

| properties | IsNull? | Defaults |
| :------|:------|:------|
|spring.datasource.druid.servlet.enable|yes|false|
|spring.datasource.druid.servlet.exclusions|yes|*.js,*.gif,*.jpg,*.png,*.css,*.ico,/druid/*|
|spring.datasource.druid.servlet.url-pattern|yes|/*|
|spring.datasource.druid.servlet.session-stat-max-count|yes|1000|
|spring.datasource.druid.servlet.session-stat-enable|yes|false|
|spring.datasource.druid.servlet.principal-session-name|yes|USER_SESSION|
|spring.datasource.druid.servlet.principal-cookie-name|yes|USER_COOKIE|
|spring.datasource.druid.servlet.profile-enable|yes|true|

[stat properties](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a33fe67d7bd83a2bf034cf792bf5d16315e3b5dd408363b510d8906851d1e6c859711b528ae6eed59fcc652a0614d323a60d99df2a38858859c819527e71be1001a9abbd5c8281e64eac67e49c1819370ae2d2b3878615c7b9336a9dedb3e2005a123c4688eb0c06dddda537c726b7188) 

| properties | IsNull? | Defaults |
| :------|:------|:------|
|spring.datasource.druid.stat.enable|yes|false|
|spring.datasource.druid.stat.aop-types|yes|null|
|spring.datasource.druid.stat.target-bean-type|yes|null|
|spring.datasource.druid.stat.bean-names|yes|null|
/spring.datasource.druid.stat.patterns|yes|null|

spring.datasource.druid.stat.aop-types  待选值有[ ***type,name,pointcut*** ]

当enable=true时候,aop-types必须有type或者name的其中一项.

- 当aop-types有name值时,bean-names不能为空.
- 当aop-types有type值时,target-bean-type不能为空.
- 当aop-types有pointcut值时,patterns不能为空.

spring.datasource.druid.stat.aop-types  selected value is [ ***type,name,pointcut*** ]


When ```enable=true``` , aop-types must have either ```type``` or  ```name```.

 - When ```aop-types``` has ```name``` value, ```bean-names``` can not be null.
 - When ```aop-types``` have ```type``` values, ```target-bean-type``` can not be empty.
 - When ```aop-types``` have ```pointcut``` values, ```patterns``` can not be empty.

## Example


    spring:
      datasource:
        url: xxx
        username: xxx
        password: xxx
        druid:
              filters: stat,wall,log4j
              connection-properties:
                - druid.stat.mergeSql=true
                - druid.stat.slowSqlMillis=5000
              filter:
                enable: true
                principal-session-name: session_admin
                profile-enable: true
                principal-cookie-name: session_admin
                session-stat-enable: true
              stat:
                enable: true
                aop-type: 
                   - name
                   - type
                   - pointcut
                target-bean-type: com.cuisongliu.springboot.core.mapper.MyMapper
                bean-names:
                   - UserMapper
                   - userMapper
                patterns:
                  - com.xinyuewulian.mapper.*
                  - com.xinyuewulian.service.*

## Acknowledgments

 [druid](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464e9ab1ba10d3588ded212abb6198c62a0d3d58c25d31097e144472fceff24708 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)