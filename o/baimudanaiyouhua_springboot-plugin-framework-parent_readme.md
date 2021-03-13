# springboot插件式开发框架

### 介绍
该框架主要是集成于springboot项目，用于开发插件式应用的集成框架。

### 核心功能
1. 插件配置式插拔于springboot项目。
2. 在springboot上可以进行插件式开发, 扩展性极强, 可以针对不同项目开发不同插件, 进行不同插件jar包的部署。
3. 可通过配置文件指定要启用或者禁用插件。
4. 支持上传插件和插件配置文件到服务器, 并且无需重启主程序, 动态部署插件、更新插件。
5. 支持查看插件运行状态, 查看插件安装位置。
6. 无需重启主程序, 动态的安装插件、卸载插件、启用插件、停止插件、备份插件、删除插件。
7. 在插件应用模块上可以使用Spring注解定义组件, 进行依赖注入。
8. 支持在插件中开发Rest接口。
9. 支持在插件中单独定义持久层访问等需求。
10. 可以遵循主程序提供的插件接口开发任意扩展功能。
11. 插件可以自定义配置文件。目前只支持yml文件。
12. 支持自定义扩展开发接口, 使用者可以在预留接口上扩展额外功能。
13. 支持插件之间的通信。
14. 支持插件中使用事务注解。
15. 支持Swagger。(仅支持首次启动初始化的插件)

### 扩展包功能
1. SpringBoot-Mybatis扩展包

- 支持在插件中自定义Mapper接口、Mapper xml 以及对应的实体bean。

- 支持实体bean的别名。

- 支持集成Mybatis-Plus。

详见 [插件SpringBoot Mybatis扩展](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e4edd87bd12c7006d1d4137a7e191cc3515e31e64bfaf5bab7bafd632230193da5835037e255f478cfbd2209f6495d4f74a0de8a06fda11e46b41b2e9bde2d327c1d0029a6ad55178d95a27b4b9250d2be2c0f6425bf64b0645d14b5096ca842a) 

2. 静态资源访问扩展包

支持通过http访问插件中静态资源。

详见 [插件静态资源访问扩展](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e4edd87bd12c7006d1d4137a7e191cc3515e31e64bfaf5bab7bafd632230193da5835037e255f478cfbd2209f6495d4f74a0de8a06fda11e46b41b2e9bde2d327bd871a02905c871fedb97259ba7269b4aeeeb34fcff2a734b987defb1ce78bef) 

### 运行环境
1. jdk1.8+
2. apache maven 3.6+
3. spring-boot 2.0.0+

### maven 仓库地址

[https://mvnrepository.com/artifact/com.gitee.starblues/springboot-plugin-framework](http://u.720life.cn/g/7ce2d2ef6590cc535c0771ea8b234faeb326ae1cdebeac2489768a7f46dda1a4710ffa0f4fb2386bb3134accd8534b62447f58b42ebb8ef0d06af0c77bea370e4f17200185901d090c337cf846a7cce51851b1ee3eadc476e9fe02c1b28e763f) 

### 文档地址

[https://gitee.com/starblues/springboot-plugin-framework-parent/wikis/pages](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e4edd87bd12c7006d1d4137a7e191cc3515e31e64bfaf5bab7bafd632230193da5835037e255f478cfbd2209f6495d4f751753d11be55a3743b0133ad5e62ab23) 


### QQ交流群
859570617

点赞框架后可进群, 进群前请备注gitee昵称。


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)