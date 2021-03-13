# ICEAdmin-MS

#### 介绍
ICEAdmin-MS(Microservice)是基于SpringCloud的微服务版后台管理系统，主要服务包含Registry、Gateway、Authority、Admin、Monitor，主要功能包含用户管理、角色管理、机构管理、字典管理、配置管理等功能。

#### 软件架构
软件架构说明


#### 安装教程

1. 导入项目到Eclipse或IDEA
2. 修改Maven的setting.xml配置文件，点我查看修改详情 （注:Maven版本需3.3及其以上）
3. 修改src/main/resources/application.yml文件，修改数据库配置
4. 在mysql中执行 db 下的 ice-admin.mysql.sql，及activiti/create下的 activiti.mysql.create.*.sql
5. 启动Redis及ActiveMQ
6. 运行顺序 registry,gateway,authority,admin

#### 使用说明

1. 本系统用户名:admin,密码:123
2. 前端UI,请移步   点我  
3. xxxx

#### 参与贡献

1. Fork 本仓库
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request


#### 码云特技

1. 使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2. 码云官方博客 [blog.gitee.com](http://u.720life.cn/g/4d9d51ba66eeb41dfb9759648c593bf554785fd0e6ab49d2f13e98afcb69bbc7) 
3. 你可以 [https://gitee.com/explore](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ed27d15edf43aa40a6d37a2a10b263e5a)  这个地址来了解码云上的优秀开源项目
4. [GVP](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb5ad9b84ebe402667383e4a11c785b2d)  全称是码云最有价值开源项目，是码云综合评定出的优秀开源项目
5. 码云官方提供的使用手册 [https://gitee.com/help](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ebbaab544314b1a4bd89bdd984a12bd00) 
6. 码云封面人物是一档用来展示码云会员风采的栏目 [https://gitee.com/gitee-stars/](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e43c4696b881f436e3c9d0b3d64c264cb) 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)