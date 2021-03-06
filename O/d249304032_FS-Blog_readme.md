 
     
         
     
 

# FS-Blog



[![LICENSE](https://img.shields.io/hexpm/l/plug.svg)](./LICENSE)
[![Build Status](https://www.travis-ci.org/JamesZBL/FS-Blog.svg?branch=master)](https://www.travis-ci.org/JamesZBL/FS-Blog)


## 基于 Spring Boot 的个人博客


### 1. 涉及技术及工具

- 核心框架：SpringBoot
- ORM 框架：MyBatis
- MyBatis 工具：MyBatis Mapper 
- MVC 框架：Spring MVC
- 模板引擎：Freemarker
- 编译辅助插件：Lombok
- CSS 框架：BootStrap 4.0
- Markdown 编辑器：Editor.md
- 数据库：MySQL


### 2. 效果图

#### 2.1 首页
![首页](screenshots/home.png)

#### 2.2 博客列表页
![文章列表](screenshots/posts.png)


#### 2.3 博客阅读页
![文章阅读](screenshots/blog.png)


#### 2.4 个人简历页
![个人简历](screenshots/resume.png)


#### 2.5 文章编辑页
![编辑器](screenshots/editor.png)


### 3. 构建及运行

#### 3.1 服务器环境

- 安装 ``MySQL``
- 安装 ``Gradle``
- 在项目目录下运行 ``gradle clean build``，生成的 jar 包位于 ``build/libs`` 目录下，使用 ``java -jar .../fsblog.jar`` 运行
- 在 ``application-dev.yml`` 中配置数据库用户名和密码，默认为：``username: root password: root``
- 默认自动创建数据库、数据表并自动导入初始数据，同样在``application-dev.yml``中配置
- 后台管理默认用户名为 ``admin``，密码为 ``123456``

#### 3.2 开发环境

- 可直接在 IntelliJ IDEA 或 Eclipse 中打开项目进行二次开发

### 4. 联系方式

QQ：1146556298

Email：zhengbaole_1996@163.com


### 5. 相关链接

- FS-Blog [在线 Demo](http://u.720life.cn/g/d8c5f1da312ca38aa4d10462b220c2a31952cf6afb7d80ef6de4e87e6966eacf) 

- 我的个人博客 [James' Blog](http://u.720life.cn/g/6b4494f05807c76a30d4cf8f9fc8d39975064132ae55914a083e580f7db917e7) 

### 6. 开源协议

[Apache License 2.0](http://u.720life.cn/g/c11fd891584afae2a884d206f8d21ebb829eb3e4d6d9a531bd681ed9fab4d7b151502113e73ea5b5d80978cc8bab7be7) 

Copyright (c) 2017-present, JamesZBL


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)