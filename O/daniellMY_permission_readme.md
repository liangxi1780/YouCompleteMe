# Permission 一个权限管理系统

之前有学习了 [张开涛老师](http://u.720life.cn/g/baba311c3867b97b01879eeeeea3661a0d2524320c949110a90e3c30f506aa9b071b72da9d9c3b8943ebdbbf744a2d6d4f5f89140a6e5775094cfea927f2a64f)  老师的作品写的一个简单的 [Shiro入门级权限管理项目]https://github.com/TyCoding/shiro)，但由于一些原因感觉学习的不够深入，最近仔细拜读了 [wuyouzhuguli](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464f90e6edbd23634b0355cd06986c92a7)  大神的作品，学习到了很多，顾写下此项目实战练习。 

**欢迎大家clone下来学习，如果可以，希望能点亮右上角star, fork，给作者一些鼓励**

**线上地址：** [http://39.105.46.235:8083/login](http://u.720life.cn/g/4883047457011282b64052af0ec85930d03e726f2b8ad736cf479fdd601c6cdc) 

| 用户名 | 密码 | 备注 |
| --- | --- | --- |
| admin | 123456 | 管理员，拥有所有权限 |
| tycoding | 123456 | 测试账号，可查看所有页面，但无操作权限 |
| tumo | 123456 | 用户管理员 |

## 致谢

* [wuyouzhuguli](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464f90e6edbd23634b0355cd06986c92a7)  

可以说**本项目**仅是一个学习的项目，非常感谢这位大神的作品：[https://github.com/wuyouzhuguli/FEBS-Shiro]https://github.com/wuyouzhuguli/FEBS-Shiro)，**本项目**就来自学习了大神的项目后把自己理解的部分（加上自己的代码风格、思路）写了出来。欢迎大家学习这个项目，相信对大家的学习很有帮助。

## 功能模块

```
├─项目文档(Swagger2.0)
├─系统管理
│  ├─用户管理
│  ├─角色管理
│  ├─菜单管理
│  └─部门管理
├─系统监控
│  ├─在线用户
│  ├─登录日志
│  ├─系统日志
│  ├─Redis监控
│  └─Druid监控
├─对象储存
│  ├─七牛云
│─网络资源
│  ├─天气查询
│  └─影视资讯
```

## 文档 

* [在基于SpringBoot的前后端分离项目中使用Shiro](http://u.720life.cn/g/e23dee3223d415719c44ac231ed4fb426a9d7ca634bc1ce671e41eb99430f1f4bac12db7c154e20c3f9635223f7308ecdfe57ef025b36e1ab9f765ebdb3dacbf) 

* [Shiro在线会话管理](http://u.720life.cn/g/e23dee3223d415719c44ac231ed4fb42304e106bd0f221794794583dc53577a30651f347f1260804b67a1ed32c7854264714dbcb46f531bd98ec208221a8108f) 

* [Shiro权限管理项目中如何构建权限菜单](http://u.720life.cn/g/e23dee3223d415719c44ac231ed4fb425741123f78d8455eecf9694554b70494b15cb937937c29357c6834d8dcb94080905b150e2c1c40a40e4112e8f6cf2410) 

* [ElementUI - Tree & Shiro](http://u.720life.cn/g/e23dee3223d415719c44ac231ed4fb42304e106bd0f221794794583dc53577a3eec894586ef9755ba8a788fc3c26186bf95c8bc22bf1d8aabc598a9b2a938e99) 

* 文档正在完善中...

## 技术选型

### 后端

* 基础框架： Spring Boot 2.1.2.RELEASE

* 持久层框架： MyBatis 3.4.6 

* 权限框架： Shiro 1.4.0

* 模板引擎： Thymeleaf 3.0.11.RELEASE

* 缓存框架： Redis 

* 其他： Swagger2、七牛云、Mybatis通用Mapper、druid、Logback、fastjson、pageHelper

### 前端

* 基础框架： ElementUI

* JavaScript插件： Vue.js

### 开发环境

* 语言： JDK1.8

* IDE： IDEA 2018.3

* 依赖管理： Maven

* 数据库： Mysql 5.7.24

## 写在前面

如果你看到技术选型可能会疑问前面完全依赖Vue.js，为何还是HTML页面？没错，前端是完全依赖Vue.js的，整个项目都没有用到JQuery。如果你学过Vue肯定熟悉NPM，Vue官方也推荐使用NPM开发，但为了更方便部署学习，这里使用HTML + Thymeleaf 解析页面。

虽然用了Thymeleaf，但也仅是用来解析页面视图地址，并没有在数据层用到Thymeleaf，所有的数据都依赖vue-resource异步获取，我以一张简单的图来解释项目交互流程：

![](http://cdn.tycoding.cn/20190315204846.png)

### 部署

由于一些原因，**线上地址**部署的项目不太完美，推荐大家clone到本地运行。

1. 克隆

```
git clone https://github.com/TyCoding/permission.git
```

2. 使用IDEA打开`permission`项目，创建数据库（执行`db/sys_schema.sql`）。

3. 修改`application.yml`中MySQL、Redis连接信息。（如果需要七牛云另完善七牛云的信息）。

4. 配置好Redis，启动Redis服务。

5. 启动项目，访问`localhost:8080`

#### 服务器部署：

直接将项目打包为jar即可：

```
mvn package
```

将`target`文件夹下出现的`permission-0.0.1-SNAPSHOT.jar`（重命名为`permission.jar`）丢到服务器的任意位置，执行如下命令其中项目：

```
java -jar permission.jar &
```

## 项目截图

![](doc/1.png)

![](doc/2.png)

![](doc/3.png)

![](doc/4.png)

![](doc/5.png)

![](doc/6.png)

![](doc/7.png)

![](doc/8.png)

![](doc/9.png)

![](doc/10.png)

![](doc/11.png)

![](doc/12.png)

![](doc/13.png)





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)