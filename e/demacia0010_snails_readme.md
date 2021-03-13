# Snails 框架
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/b_dashboard.jpg)

基于 [SpringBoot](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d74791681f9785d83f6cd6c957366ad1debb29bb8c32cd47aff960e71f7893090)  + [Ng-Alain](http://u.720life.cn/g/0b1496ac89232028b6a7a545d7074fc2474a862c01fbda319c5090f80e7f5bc6)  `前后端分离`的实现，可以作为新手入门项目，也可以作为小项目的`基础框架`去扩展。目前 [Snails](http://u.720life.cn/g/85a9f52868358c3208a4b5fd9062e99395ca6e9c4611c2f7e6290ce72b7645bfecabf6b5f30320ea4e51e79ce3079565)  系统框架已支持基本的后台功能，基于`简单`、`实用`设计，并且已支持 [Docker](http://u.720life.cn/g/d13d2b0ef4a5c92b4f4a6e9ed4270e65b90c4c1e1b506e1a501feef81ad769e9)  进行项目部署。

- `Snails 框架`：编程入门，新手礼赞
- `snails-web 前端`：[Angular](http://u.720life.cn/g/8fd75c07dc4cbb8ed759f099d2fc1cb1505e2651b3049745325a8342ce05f7dd)  + [Ng-Zorro](http://u.720life.cn/g/8924562f6e22955b64d005dfba7246deb96eddf82b770577e49d5f3fdc610fee1613b4af3c6d2079d5eb38bb12a3cc8f)  + [Ng-Alain](http://u.720life.cn/g/0b1496ac89232028b6a7a545d7074fc261be794acce5fc95f197b3ff5bd57743) 
- `snails-api 后台`：[SpringBoot](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263d74791681f9785d83f6cd6c957366ad1debb29bb8c32cd47aff960e71f7893090)  + [JPA ](http://u.720life.cn/g/c6d1b26d763f49c99d62f7dd7e1f263dbe905ae631048feaf69eced65a71a46eab8b80b596b0c8a17472dc8d0797c9bc379530e7442dda3a724927e2b2a878d1  [lombok](http://u.720life.cn/g/9cec729ef2d3c72b70f7caf7a64fe54c004be7f5a331560d74f301adfc8849d5)  + [Java8](http://u.720life.cn/g/85a9f52868358c3208a4b5fd9062e993cf51ed4e030337272b88113597fbb3d1)  + Mysql

**基于国内访问速度考虑，建议使用 [码云](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e49c99e6e9eb9317b92274a30119450cd)  进行访问 [https://gitee.com/kuzank/snails](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e49c99e6e9eb9317b92274a30119450cd)  **

|      `框架源码`     | Gitee                                                        | GitHub                                                       |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Snails** 框架      | [https://gitee.com/kuzank/snails](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e49c99e6e9eb9317b92274a30119450cd)  | [https://github.com/kuzank/snails](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5258bf9a5de373b76594c11d8098808)  |
| **Snails-web** 前端  | [https://gitee.com/kuzank/snails-web](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e768e56463b2f073a32f3e05f21ed7d1938e82c3349438b20d7b701eae9a00bea)  | [https://github.com/kuzank/snails-web](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5258bf9a5de373b76594c11d80988084a8e149c4299288723b3a3a93fd338fc)  |
| **Snails-api**  后台 | [https://gitee.com/kuzank/snails-api](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e768e56463b2f073a32f3e05f21ed7d1900acafd0f6dac2dbed958e00ff81f8b4)  | [https://github.com/kuzank/snails-api](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5258bf9a5de373b76594c11d809880837a7362b4d9e40179cf3ed1cea6e6a14)  |

欢迎到 `Gitee` 或者 `GitHub` 上提 `issue`

| `issue 渠道` | 访问地址                                                     |
| ------------ | ------------------------------------------------------------ |
| **Gitee**    | [https://gitee.com/kuzank/snails/issues](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6efa77f2356bb56c2093c38800dc2679185b6439589173b39070bbeef338484bcc)  |
| **GitHub**   | [https://github.com/kuzank/snails/issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5258bf9a5de373b76594c11d809880884e176925acef7d652211fac1a58b340)  |


## 1、系统功能

* [x]  登陆、登出
* [x]  用户管理
* [x]  组织管理
* [x]  菜单管理，支持菜单配置、菜单权限配置、用户菜单权限预览功能
* [x]  在线用户
* [x]  登陆日志，记录系统用户的登陆登出行为
* [x]  http请求，将系统的所有请求进行拦截，并记录到数据库中
* [x]  系统异常，全局拦截系统的异常，并记录到数据库中
* [x]  支持系统数据初始化
* [x]  支持 `Docker` 部署



## 2、启动系统前提 `Mysql`

Mysql 配置文件地址：`/snails-api/src/main/resources/application.yml`

| IP        | Port | Username | Password | Database |
| --------- | ---- | -------- | -------- | -------- |
| localhost | 3306 | root     | 123456   | snails   |



## 3、启动系统 

### 3.1、方法一 `Docker`

前提：系统已安装和配置 `Java8`、`Git`、`Maven`、`Docker`

```shell
# 1、打包 snails-web 镜像
git clone https://gitee.com/kuzank/snails-web.git
cd snails-web
docker build -t snails-web .

# 2、打包 snails-api 镜像
git clone https://gitee.com/kuzank/snails-api.git
cd snails-api
# 根据步骤 2 所示，修改代码中的 Mysql 配置 /snails-api/src/main/resources/application.yml
# 使用部署系统中 Docker 的 Mysql 作为数据库连接可能导致启动报错
mvn package docker:build

# 3、启动 docker 镜像
# 查看 docker 镜像
docker images | grep snails
# 运行 snails-web
docker run -d --name snails-web -p 4200:4200 snails-web
# 运行 snails-api
docker run -d --name snails-api -p 8081:8081 -t snails-api
# 查看运行中的 docker 实例
docker ps -a | grep snails

# 4、浏览器访问 localhost:4200 即可
```
### 3.2、方法二

前提：系统已安装和配置 `Java8`、`Git`、`Maven`、`Node`

```shell
# 1、运行 snails-web
git clone https://gitee.com/kuzank/snails-web.git
cd snails-web
yarn
npm run start

# 2、运行 snails-api
git clone https://gitee.com/kuzank/snails-api.git
cd snails-api
# 根据步骤 2 所示，修改代码中的 Mysql 配置 /snails-api/src/main/resources/application.yml
mvn package
java -jar target/snails-0.1.jar

# 3、浏览器访问 localhost:4200 即可
```



## 4、系统截图 
> 浏览器访问 localhost:4200

### 4.1、登陆页面

>  系统默认用户、账号、密码信息，数据在 **snails-api** 启动后初始化到数据库中，源码在 snails-api/src/main/java/com/kuzank/snails/init/InitPerson.java

| 用户名     | 账号       | 密码   | 备注                             |
| ---------- | ---------- | ------ | -------------------------------- |
| kuzank     | kuzank     | 123456 | 所属组织：Snails Studio > 技术部 |
| danxiaogui | danxiaogui | 123456 | 所属组织：Snails Studio > 财务部 |

![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/a_login.jpg)

### 4.2、首页
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/b_dashboard.jpg)

### 4.3、用户管理
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/c_userManage.jpg)

### 4.4、组织管理
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/d_orgunitManage.jpg)

### 4.5、菜单管理
> 菜单配置及菜单权限配置

![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/e_menuManage.jpg)

> 用户菜单权限预览

![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/f_menuPermissionPreview.jpg)

### 4.6、在线用户
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/g_onlineUser.jpg)

### 5.7、登陆日志
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/h_loginLog.jpg)

### 4.8、http请求
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/i_httpRequest.jpg)

### 4.9、系统异常
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/j_systemException.jpg)

### 4.10、G2图表
![](https://gitee.com/kuzank/Resource/raw/master/Snails/picture/k_g2Custom.jpg)


## 5、学习资源

- [Angular快速上手](http://u.720life.cn/g/8fd75c07dc4cbb8ed759f099d2fc1cb1038975cd0ffe4d0438674a605a2cefd89cd80d7f0fe6b0c457567c77f597a4d2) 
- [Ng-Zorro](http://u.720life.cn/g/8924562f6e22955b64d005dfba7246deb96eddf82b770577e49d5f3fdc610fee1613b4af3c6d2079d5eb38bb12a3cc8f) 
- [Ng-Alain](http://u.720life.cn/g/0b1496ac89232028b6a7a545d7074fc2474a862c01fbda319c5090f80e7f5bc6) 
- [Spring系列-程序员DD](http://u.720life.cn/g/43cbeb0b30a8046cf65fde9a4dd1cf2e362d2970b1cbb0718e7a080e081d2de5) 
- [Spring系列-纯洁的微笑](http://u.720life.cn/g/a7aa90cf5fe79726b10a2a75b316765703c7dcb58f135471010b7a077e999b3059fa78805c53afcf8a354628c6041f5f) 
- [Java8](http://u.720life.cn/g/85a9f52868358c3208a4b5fd9062e993cf51ed4e030337272b88113597fbb3d1) 
- [lombok](http://u.720life.cn/g/8a0e6e781ca1335d5641e0f9d5e96ab910cc07fec2381979ee0eccaedb31c24e60bef370e29737e0298e092aaf954066) 
- [SpringBoot 中 JPA 的使用](http://u.720life.cn/g/8a0e6e781ca1335d5641e0f9d5e96ab914e5bbae167cd5fd72c38691f6d3d6b61ca31c7daccd60736ff69f1b43a666e9) 


## 开源许可证
MIT



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)