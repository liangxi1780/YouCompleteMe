﻿# BootstrapAdmin

## 项目介绍
一直需要一款后台管理系统，但是网上很多开源项目都是 **Java** 开发的，本人是 **NET** 平台的对 **Java** 一窍不通，C#版本的本来就少而且还没有合适的。于是决定自己开发一套后台管理系统。由于前台采用 **Bootstrap** 布局样式，所以就叫做 **BootstrapAdmin** 。本系统可以用于所有的 Web 应用程序，目前版本已经升级到 **NET CORE** 具备跨平台能力。数据库方面同时支持多种数据库，详细列表见后面**数据库**的详细列表，切换数据源仅需更改配置文件无需重启应用程序，配置简单灵活。UI 前端使用流行的Bootstrap框架布局对移动设备的兼容性非常好，自适应目前市场几乎所有终端设备。本系统还具备单一后台支持多前台的特色，提供 **单点登录（SSO）** 的能力。  

使用 HTML5 + jQuery + NET Core 2.2 + Bootstrap4.1 + PetaPoco 构建的后台管理平台  
### 主要功能  
1. 通过配置与前台网站集成
2. 构建前台系统分层级菜单
3. 提供单一后台支持多前台应用配置
4. 提供单点登录
5. 集成系统认证授权模块
6. 提供角色，部门，用户，菜单，前台应用程序授权  
角色对用户授权  
角色对菜单授权  
角色对部门授权  
角色对应用程序授权（多个前台应用公用一个后台权限管理系统）  
部门对用户授权  
7. 提供字典表用于前台网站个性化配置  
8. 完全响应式布局（支持电脑、平板、手机等所有主流设备）
9. 内置多数据源支持，配置简单立即生效无需重启
10. 内置数据内存缓存机制，页面快速响应
11. 内置数据 **操作日志** 与用户 **登录日志**   
跟踪记录用户 **登录主机地点**  **浏览器**  **操作系统** 信息  

#### 优势
1. 前台系统不用编写登录、授权、认证模块；只负责编写业务模块即可
2. 后台系统无需任何二次开发，直接发布即可使用
3. 前台与后台系统分离，无任何依赖关系

详细资料请点击 [查看文档]https://gitee.com/LongbowEnterprise/BootstrapAdmin/wikis/项目介绍  

## 数据库
数据库支持列表如下：  
**MSSQL/Oracle/SQLite/MySql/MariaDB/Postgresql/Firebird/MsAccess/MongoDB**  

## QQ交流群
群号
795206915  
[快速加群](http://u.720life.cn/g/e4cdc8a5afa7a074f5195772284c0c5f8e5b843143288222f8a8ec57b75dca801ef227aea4277cf7b375e460d3f923409f2f6605009599722755aeb1be71d3b622a55c775e58081f85c6d08cb63305638d80c27e54c265e3cf7176a3be8ad787ecbf6692552229023c6b6df47f37f06d)  

## 安装教程
1. 安装 .net core sdk [官方网址](http://u.720life.cn/g/43d8d3d99c8fd8af6c240816f866ce0c8b13eb7d4d18ef7e176fe2d01e91feca623f97614f43c51b207b842a033b3b54) 
2. 安装 Visual Studio IDE 2017以上 [官方网址](http://u.720life.cn/g/820904a611da240c9864c98b312d88b8c07726139b7dc45e0ef6d2903f520b6f50e1dffe58ee320520982acba69e56be25357d31c73393d8bcc9176de3a03310) 
3. 获取本项目代码 [BootstrapAdmin](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e57ea0884cbb37ee2cbb0c5aa7c340d74e053c450f6dfab45eaccf03604238a367248032563e609e55dd81c9552533a11) 
4. 安装数据库  
以微软MSSQL为例，执行解决方案中SQLServer目录（物理硬盘中DatabaseScripts目录下）Install.sql脚本创建数据库
5. 初始化数据  
执行对应目录下InitData.sql脚本
6. 拷贝Longbow.lic文件  
拷贝Scripts目录下Longbow.lic文件到bin目录下
7. 系统登录用户名与口令  
用户名：**Admin**  
密码：**123789**  

 **dev** 开发分支目前开发环境配置是 windows + SQLite 项目 Clone 到本地后直接即可运行测试  
 **master** 发布分支

**在线演示**  [传送门]   
网站服务器配置：  
CPU: 1核  
MEM: 2G

## 配置说明
详细配置说明请点击 [查看文档](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e57ea0884cbb37ee2cbb0c5aa7c340d74e053c450f6dfab45eaccf03604238a363b83b60ed1d6555c9594670f930e9478)  查看配置说明小节  

## 常见问题Q&A
请点击 [查看文档]https://gitee.com/LongbowEnterprise/BootstrapAdmin/wikis/常见问题Q&A 查看常见问题小节  

## 项目截图

后台首页

![后台首页](https://gitee.com/LongbowEnterprise/Pictures/raw/master/BootstrapAdmin/BA02-01.png "BAHome-01.png")

更多截图请点击 [查看文档](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e57ea0884cbb37ee2cbb0c5aa7c340d74e053c450f6dfab45eaccf03604238a363b83b60ed1d6555c9594670f930e9478)  查看项目截图小节  

## 特别鸣谢
1.  **云龙**  提供云服务器搭建在线演示系统
2.  **一事冇诚**  对MongoDB数据库提供了详细测试

## 参与贡献

1. Fork 本项目
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)