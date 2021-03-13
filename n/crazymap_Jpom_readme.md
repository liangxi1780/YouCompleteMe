 
	 
	     
	 
 
 
	 一款简而轻的低侵入式在线构建、自动部署、日常运维、项目监控软件 
 

 
     
         
     
     
         
     
     
         
     
     
         
     
     
         
     
     
         
     
     
         
     
     
         
     
 
 
	 https://jpom.io/  |  https://jpom-site.keepbx.cn/  |  https://jpom.keepbx.cn/ 
 

 
#### 你为什么需要[Jpom](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee676903a636c1b6e86c8db69a4e5af59) 

> Java 项目在实际部署运维，通用的方法是登录服务器上传新的项目包，执行相应命令管理，如果管理多个项目则重复操作上述步骤

> 此方法不足的是：
> 1. 需要每次登录服务器（专业软件）
> 2. 多个项目有多个管理命令（不易记、易混淆）
> 3. 查看项目运行状态需要再次使用命令
> 4. 同时面对多个运维都需要知道服务器密码（安全性低）
> 5. 集群项目需要挨个操作项目步骤

> 在使用Jpom后：
> 1. 使用浏览器登录方便快捷管理项目
> 2. 界面形式实时查看项目运行状态以及控制台日志
> 3. 运维有对应的账号密码不需要知道服务器密码（并且有操作日志）
> 4. 集群项目使用项目分发一键搞定多机部署
> 5. 项目状态监控异常自动报警
> 6. 在线构建不用手动上传项目包

#### 项目主要功能及特点

1. 创建、修改、删除项目、Jar包管理
2. 实时查看控制台日志、备份日志、删除日志、导出日志
3. cpu、ram 监控、导出堆栈信息、查看项目进程端口、服务器状态监控
4. 多节点管理、多节点自动分发
5. 实时监控项目状态异常自动报警
6. 在线构建项目发布项目一键搞定
7. 多用户管理，用户项目权限独立(上传、删除权限可控制),完善的操作日志
8. 系统路径白名单模式，杜绝用户误操作系统文件
9. 在线管理Nginx配置、ssl证书文件
10. Tomcat状态、文件、war包在线实时管理

> 特别提醒：在Windows服务器中可能有部分功能因为系统特性造成兼容性问题，建议在实际使用中充分测试。Linux目前兼容良好

### 一键安装

#### 服务端

```
yum install -y wget && wget -O install.sh https://keepbx.gitee.io/jpom/install.sh && bash install.sh Server

备用地址

yum install -y wget && wget -O install.sh https://cdn.jsdelivr.net/gh/jiangzeyin/Jpom/docs/install.sh && bash install.sh Server

```

#### 插件端

```
yum install -y wget && wget -O install.sh https://keepbx.gitee.io/jpom/install.sh && bash install.sh Agent

备用地址

yum install -y wget && wget -O install.sh https://cdn.jsdelivr.net/gh/jiangzeyin/Jpom/docs/install.sh && bash install.sh Agent

```

### 下载安装

> [帮助文档](http://u.720life.cn/g/70ef460ee377959b21eb4e443c488dbabd5c61aaa5fa044cdadc16f26b02c59674a089df5041593379c1269d99631749309e2512c64a624eec78b102ff0d3de3) 

1. 下载安装包 [https://gitee.com/keepbx/Jpom/attach_files](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e7e1b196b247a3aec7df1f8459927de206223c6830e88f907b2e5d54f820814d2) 
2. 解压文件
3. 安装插件端（[流程说明]https://jpom-site.keepbx.cn/docs/#/安装使用/开始安装?id=安装插件端)）
    1. agent-x.x.x-release 目录为插件端的全部安装文件
    2. 上传到对应服务器
    3. 命令运行（Agent.sh、Agent.bat）
4. 安装服务端（[流程说明]https://jpom-site.keepbx.cn/docs/#/安装使用/开始安装?id=安装服务端)）
    1. server-x.x.x-release 目录为服务端的全部安装文件
    2. 上传到对应服务器
    3. 命令运行（Server.sh、Server.bat）

### 编译安装

> [帮助文档](http://u.720life.cn/g/70ef460ee377959b21eb4e443c488dbabd5c61aaa5fa044cdadc16f26b02c59674a089df5041593379c1269d99631749309e2512c64a624eec78b102ff0d3de3) 

1. 访问[Jpom]https://gitee.com/keepbx/Jpom的码云主页,拉取最新完整代码建议使用master分支
2. 进入项目目录执行:`mvn clean package`
3. 安装插件端（[流程说明]https://jpom-site.keepbx.cn/docs/#/安装使用/开始安装?id=安装插件端)）
    1. 查看插件端安装包 modules/agent/target/agent-x.x.x-release
    2. 打包上传服务器运行
    3. 命令运行（Agent.sh、Agent.bat）
4. 安装服务端（[流程说明]https://jpom-site.keepbx.cn/docs/#/安装使用/开始安装?id=安装服务端)）
    1. 查看插件端安装包 modules/server/target/server-x.x.x-release
    2. 打包上传服务器运行
    3. 命令运行（Server.sh、Server.bat）

### 编译运行

1. 访问[Jpom]https://gitee.com/keepbx/Jpom的码云主页,拉取最新完整代码建议使用master分支、如果想体验新功能请使用dev分支
2. 运行插件端   
    1. 运行`io.jpom.JpomAgentApplication`
    2. 注意控制台打印的默认账号密码信息
3. 运行服务端
    1. 运行`io.jpom.JpomServerApplication`
    2. 浏览器访问（如：http://127.0.0.1:2122）

### 管理命令
1. windows中Agent.bat 、Server.bat
```
# 服务端
Server.bat     启动管理面板(按照面板提示输入操作)

# 插件端
Agent.bat     启动管理面板(按照面板提示输入操作)
```
2. linux中Agent.sh 、Server.sh
```
# 服务端
Server.sh start     启动Jpom服务端
Server.sh stop      停止Jpom服务端
Server.sh restart   重启Jpom服务端
Server.sh status    查看Jpom服务端运行状态

# 插件端
Agent.sh start     启动Jpom插件端
Agent.sh stop      停止Jpom插件端
Agent.sh restart   重启Jpom插件端
Agent.sh status    查看Jpom插件端运行状态
```

### Jpom 的参数配置

   在项目运行的根路径下的`extConfig.yml`文件
   1. 插件端示例：[`extConfig.yml`](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e901f4ec53352591b069873debfbdb7951ae837c17a34a2fc4d5d02590682a5b4971d215bd25bf9057011da64330758cf3d616598045ac502fcef4ef60e04b5354a6228fdcfac4e1eb0f5ce9a15b1d049)  
   2. 服务端示例：[`extConfig.yml`](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e901f4ec53352591b069873debfbdb7951ae837c17a34a2fc4d5d02590682a5b40f03c5f7c11fd02c316c3726736b1ba1e7aff5d38924d817645602194a1a5e1963c18f4249a35af5d5ba54864309d1fe) 

### 演示项目

   [https://jpom.keepbx.cn](http://u.720life.cn/g/c69fc64abe79034649ec8377dc357c6021424e382f5c52a584d7db03a498b683) 
```   
账号：demo
密码：demo123
```    
   > 演示系统有部分功能做了限制，完整功能请自行部署体验
   
   > 如果出现登录不上，请联系我们，联系方式在最底部
    
   1. [Jboot案例代码](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6effb652a5c8d5c93c86aed2bd415449374a6470014ce1836550144e44660937cd08cc0ed0f77587d20fb36e550af33d30) 
   2. [SpringBoot案例代码(ClassPath)](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6effb652a5c8d5c93c86aed2bd415449374a6470014ce1836550144e44660937cdd21fb079ff6b4bd2c1269d07edc5d8bda51cda7e9447036b32b267f8c9f6ced2) 
   3. [SpringBoot案例代码(Jar)](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6effb652a5c8d5c93c86aed2bd415449374a6470014ce1836550144e44660937cdd21fb079ff6b4bd2c1269d07edc5d8bdb53c0f987c333f5acbf854c666b045a5) 

### 常见问题、操作说明

[https://jpom-site.keepbx.cn/docs/](http://u.720life.cn/g/70ef460ee377959b21eb4e443c488dbabd5c61aaa5fa044cdadc16f26b02c596463a379e3824faf5417d04ed80eff38d)  

[https://jpom-site.keepbx.cn/docs/#/FQA/FQA](http://u.720life.cn/g/70ef460ee377959b21eb4e443c488dbabd5c61aaa5fa044cdadc16f26b02c59672be2a594dd958b0988a53dc8144e41f) 

[Jpom 插件开发](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e21cbca069a2ce89bea2ecb77ec16c5a8166b296ef6d10130d17c7a40ca58bcfb) 

### 交流讨论 、提供bug反馈或建议

  1. QQ群：[136715345](http://u.720life.cn/g/e4cdc8a5afa7a074f5195772284c0c5f8e5b843143288222f8a8ec57b75dca805e5f20e09b64dda1756c7164e2f90f694663a56c69850e40c419223edeca00d860321c4746a980344cd1106c8d410deb73ef10d2ac557ee12187ca217fc113f91bf406f39ead6e639f6f56e8d9a0a71c) 
  
  2. 微信公众号：[CodeGzh](http://u.720life.cn/g/586f7cded5bf957de0e4d30e3929c8c1f3afb8f5417aa31023378d47fa1ced48f25ddae126222b9d1ae8068c87633636592d101ae6d55806f0ef6c9ec6acb258739a157178c3bfdc7b576fcc8889a85d) 
  
  3. 码云： [issues](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e0cfcbcb8454ffde6df52e69a649526ee0d40321033e877fe5b110670285b6215) 
  
  4. [捐赠、打赏 在码云仓库项目首页下方捐赠即可](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ee676903a636c1b6e86c8db69a4e5af59) 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)