## ShiroJwt

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/wang926454/ShiroJwt/pulls)
[![GitHub stars](https://img.shields.io/github/stars/wang926454/ShiroJwt.svg?style=social&label=Stars)](https://github.com/wang926454/ShiroJwt)
[![GitHub forks](https://img.shields.io/github/forks/wang926454/ShiroJwt.svg?style=social&label=Fork)](https://github.com/wang926454/ShiroJwt)

> 前端地址:[https://github.com/wang926454/VueStudy/tree/master/VueStudy08-JWT](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e90c88943464bfada129ab1cbf0a3d37843f8308fc52da1031e5daea556cc7004bf429f27332ac4fa59abcc162305c2211f617a67fd15ea49d84c90591a2adf) 

#### Issues

1. [#14 重复请求会不会生成多个token](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c4b65af76e7b5113a7ad36a4df094294af292f78f45ba2f8499a85c544debd80) 
2. [#19 跨域sso问题](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c4b65af76e7b5113a7ad36a4df0942943dcf93cd0e4b646b6364459f268ff670) 
3. [#22 如果是微服务的话，是不是每个微服务都的写一套这样的shiro?](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c4b65af76e7b5113a7ad36a4df094294c7f6da2bf33bd19e4931c1451b603d7a) 

#### 项目相关

* JavaDoc:[https://apidoc.gitee.com/dolyw/ShiroJwt](http://u.720life.cn/g/b6749edd47dfb34db84492b28bcc9586c6740badc43fdeb3bb3c8bdbdec8dfb101fbb255fda77a5058945f1c478f968b) 
* 接口文档:[https://github.com/wang926454/MyDocs/blob/master/Project/ShiroJwt/ShiroJwt-Interface.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462682c05c83cb6b8eae8ce4a9fa45824eaa34d4bac8839e747254f694c917c6c6b08d4afc5ae61736f816200163fce03fc45884e3e1768ef8b0f04168f6889cc2508634a9a0affe26e2b7f300c5154b90) 
* 教程目录:[https://github.com/wang926454/MyDocs/blob/master/Project/ShiroJwt/ShiroJwt01.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462682c05c83cb6b8eae8ce4a9fa45824eaa34d4bac8839e747254f694c917c6c6b08d4afc5ae61736f816200163fce03f339bfb56abf9cc3544cec76cf1e467fb) 
* 改为数据库形式(MySQL):[https://github.com/wang926454/MyDocs/blob/master/Project/ShiroJwt/ShiroJwt02-MySQL.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462682c05c83cb6b8eae8ce4a9fa45824eaa34d4bac8839e747254f694c917c6c6b08d4afc5ae61736f816200163fce03f643cd93eadcbf2266bd12a13a823073152a8c5251543cf7d5a8914731bd4e2eb) 
* 解决无法直接返回401错误:[https://github.com/wang926454/MyDocs/blob/master/Project/ShiroJwt/ShiroJwt03-401.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462682c05c83cb6b8eae8ce4a9fa45824eaa34d4bac8839e747254f694c917c6c6b08d4afc5ae61736f816200163fce03fbc0922981b100c352a625598bfb09adb277e5e297faef78d7811fc1a46977d02) 
* 实现Shiro的Cache(Redis)功能:[https://github.com/wang926454/MyDocs/blob/master/Project/ShiroJwt/ShiroJwt04-Redis.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462682c05c83cb6b8eae8ce4a9fa45824eaa34d4bac8839e747254f694c917c6c6b08d4afc5ae61736f816200163fce03f56ba6eb6a459a02403fcc7a45bcbbd1dc418dcedb72bbccef550aad0d7c34bfb) 

#### 项目介绍

1. RESTful API
2. Maven集成Mybatis Generator(逆向工程)
3. Shiro + Java-JWT实现无状态鉴权机制(Token)
4. 密码加密(采用AES-128 + Base64的方式)
5. 集成Redis(Jedis)
6. 重写Shiro缓存机制(Redis)
7. Redis中保存RefreshToken信息(做到JWT的可控性)
8. 根据RefreshToken自动刷新AccessToken

##### 关于Shiro + Java-JWT实现无状态鉴权机制(Token)
```txt
首先Post用户名与密码到user/login进行登入，如果成功返回一个加密的AccessToken，失败的话直接返回401错误(帐号或密码不正确)，以
后访问都带上这个AccessToken即可，鉴权流程主要是重写了Shiro的入口过滤器JWTFilter(BasicHttpAuthenticationFilter)，判断请求
Header里面是否包含Authorization字段，有就进行Shiro的Token登录认证授权(用户访问每一个需要权限的请求必须在Header中添加Author
ization字段存放AccessToken)，没有就以游客直接访问(有权限管控的话，以游客访问就会被拦截)
```

##### 关于AES-128 + Base64当两个用户的明文密码相同时进行加密，会发现数据库中存在相同结构的暗文密码
```txt
大部分是以MD5 + 盐的形式解决了这个问题(详细自己百度)，我采用AES-128 + Base64是以帐号+密码的形式进行加密密码，因为帐号具
有唯一性，所以也不会出现相同结构的暗文密码这个问题
```

##### 关于将Jedis工具类与SpringBoot整合
```txt
本来是直接将JedisUtil注入为Bean，每次使用直接@Autowired注入使用即可，但是在重写Shiro的CustomCache无法注入JedisUtil，所以
就改成静态注入JedisPool连接池，JedisUtil工具类还是直接调用静态方法，无需@Autowired注入
```

##### 关于Redis中保存RefreshToken信息(做到JWT的可控性)
```txt
登录认证通过后返回AccessToken信息(在AccessToken中保存当前的时间戳和帐号)，同时在Redis中设置一条以帐号为Key，Value为当前时
间戳(登录时间)的RefreshToken，现在认证时必须AccessToken没失效以及Redis存在所对应的RefreshToken，且RefreshToken时间戳和Ac
cessToken信息中时间戳一致才算认证通过，这样可以做到JWT的可控性，如果重新登录获取了新的AccessToken，旧的AccessToken就认证不
了，因为Redis中所存放的的RefreshToken时间戳信息只会和最新的AccessToken信息中携带的时间戳一致，这样每个用户就只能使用最新的
AccessToken认证，Redis的RefreshToken也可以用来判断用户是否在线，如果删除Redis的某个RefreshToken，那这个RefreshToken所对
应的AccessToken之后也无法通过认证了，就相当于控制了用户的登录，可以剔除用户
```

##### 关于根据RefreshToken自动刷新AccessToken
```txt
本身AccessToken的过期时间为5分钟(配置文件可配置)，RefreshToken过期时间为30分钟(配置文件可配置)，当登录后时间过了5分钟之后
，当前AccessToken便会过期失效，再次带上AccessToken访问JWT会抛出TokenExpiredException异常说明Token过期，开始判断是否要进
行AccessToken刷新，首先Redis查询RefreshToken是否存在，以及时间戳和过期AccessToken所携带的时间戳是否一致，如果存在且一致就
进行AccessToken刷新，过期时间为5分钟(配置文件可配置)，时间戳为当前最新时间戳，同时也设置RefreshToken中的时间戳为当前最新时
间戳，刷新过期时间重新为30分钟过期(配置文件可配置)，最终将刷新的AccessToken存放在Response的Header中的Authorization字段返
回(前端进行获取替换，下次用新的AccessToken进行访问)
```

#### 软件架构

1. SpringBoot + Mybatis核心框架
2. PageHelper插件 + 通用Mapper插件
3. Shiro + Java-JWT无状态鉴权认证机制
4. Redis(Jedis)缓存框架

#### 安装教程

1. 数据库帐号密码默认为root，如有修改，请自行修改配置文件application.yml
2. 解压后执行src\main\resources\sql\MySQL.sql脚本创建数据库和表
3. Redis需要自行安装Redis服务，端口密码默认
4. SpringBoot直接启动即可，测试工具PostMan

#### 使用说明

##### Mybatis Generator使用(可视化自定义模板快速生成基础代码:[https://github.com/wang926454/ViewGenerator](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046decf31ef85574c244593a43981cee8e94858779d2d608f0857d09f2d634e9422) 

先配置src\main\resources\generator\generatorConfig.xml文件(默认配置都在原来包的下一级reverse包下)，在pom.xml这一级目录(即项目根目录下)的命令行窗口执行(前提是配置了mvn)(IDEA可以直接在Maven窗口Plugins中双击执行)
```txt
mvn mybatis-generator:generate
```

##### PostMan使用(Token获取及使用)

```txt
先设置Content-Type为application/json
```
![image text](https://docs.dolyw.com/Project/ShiroJwt/image/20181006001.PNG)
```txt
然后填写请求参数帐号密码信息
```
![image text](https://docs.dolyw.com/Project/ShiroJwt/image/20181006002.PNG)
```txt
进行请求访问，请求访问成功
```
![image text](https://docs.dolyw.com/Project/ShiroJwt/image/20181006003.PNG)
```txt
点击查看Header信息的Authorization属性即是Token字段
```
![image text](https://docs.dolyw.com/Project/ShiroJwt/image/20181006004.PNG)
```txt
访问需要权限的请求将Token字段放在Header信息的Authorization属性访问即可
```
![image text](https://docs.dolyw.com/Project/ShiroJwt/image/20181006005.PNG)
```txt
Token的自动刷新也是在Token失效时返回新的Token在Header信息的Authorization属性
```

#### 搭建参考

1. 感谢SmithCruise的Shiro+JWT+Spring Boot Restful简易教程:[https://www.jianshu.com/p/f37f8c295057](http://u.720life.cn/g/8a0e6e781ca1335d5641e0f9d5e96ab925a7bf366d73096a8071f40d7859513f47a24ad115f3044dbf5c426f976a74e6) 
2. 感谢王洪玉的[Shiro入门]（一）使用Redis作为缓存管理器:[https://blog.csdn.net/why15732625998/article/details/78729254](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded5c0ecf3e0463b7bb1113e7acf9000844631143156d65adf82094b9aa57b6f5278ff9230cf7ce6ec81d9d131133e778ad) 
3. 感谢袋🐴饲养员的springboot(七).springboot整合jedis实现redis缓存:[http://www.cnblogs.com/GodHeng/p/9301330.html](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f766ff8102f46c2e4c2fdb622883006bfd1e146d42c84509f0993b833f496b1b5) 
4. 感谢W_Z_W_888的spring注入静态变量的三种方法及其注意事项:[https://blog.csdn.net/W_Z_W_888/article/details/79979103](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded0ae98598237be8d9e77d2835a2ad4111e283f2a401b9f17c7d4ceecd2d86f5560dc1e747c78d47e6b08bdf1280ad1890) 
5. 感谢天降风云的Vue2.0+ElementUI+PageHelper实现的表格分页:[https://blog.csdn.net/u012907049/article/details/70237457](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded0f16e451a0354451c19e22947c0523cb0e2acd587150c6f19fb66e93eafc84c06dee5705e9019aa82b7bf4cdfa83dca9) 
6. 感谢yaxx的Vuejs之axios获取Http响应头:[https://segmentfault.com/a/1190000009125333](http://u.720life.cn/g/6900aa436d7855810ebad430307e6f91c8b258b81c5d2f9bc5f21dfc6a8e3e4701876d7571884f7eb12ce1d7cdc75141) 
7. 感谢Twilight的解决使用jwt刷新token带来的问题:[https://segmentfault.com/a/1190000013151506](http://u.720life.cn/g/6900aa436d7855810ebad430307e6f91c8b258b81c5d2f9bc5f21dfc6a8e3e47f4acd1f4c2345130ad617b92613680f7) 
8. 感谢chuhx的shiro拦截器，返回json数据:[https://blog.csdn.net/chuhx/article/details/51148877](http://u.720life.cn/g/ce3f6174933242f367d8a4cd3fa79ded4e84b37b7fe56d0aa5e832bdbcbab38c4f4d1d3c72428ab169440a53d477f38b0d115a4db80dd346355a533510b9f432) 
9. 感谢yidao620c的Shiro自带拦截器配置规则:[https://github.com/yidao620c/SpringBootBucket/tree/master/springboot-jwt](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ca0d563cb40b9d80633f0a712da27eb038ac535f24ff26d653813a782ac4681ab34ef84abc1ae088b5fb48f6d29cca7c449e6fa14f3a4fadd4c5baa789858346) 

#### 参与贡献

1. Fork 本项目
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)