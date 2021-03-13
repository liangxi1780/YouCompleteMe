## YApi  可视化接口管理平台
示例站点：
  yapi.demo.qunar.com  


文档：
  hellosean1025.github.io/yapi  

### 平台介绍
![avatar](yapi-base-flow.jpg)

YApi 是 高效 、 易用 、 功能强大 的 api 管理平台，旨在为开发、产品、测试人员提供更优雅的接口管理服务。可以帮助开发者轻松创建、发布、维护 API，YApi 还为用户提供了优秀的交互体验，开发人员只需利用平台提供的接口数据写入工具以及简单的点击操作就可以实现接口的管理。

**QQ交流群**: 644642474

### 特性
*  基于 Json5 和 Mockjs 定义接口返回数据的结构和文档，效率提升多倍
*  扁平化权限设计，即保证了大型企业级项目的管理，又保证了易用性
*  类似 postman 的接口调试
*  自动化测试, 支持对 Response 断言
*  MockServer 除支持普通的随机 mock 外，还增加了 Mock 期望功能，根据设置的请求过滤规则，返回期望数据
*  支持 postman, har, swagger 数据导入
*  免费开源，内网部署，信息再也不怕泄露了

### 内网部署
#### 环境要求
* nodejs（7.6+)
* mongodb（2.6+）
* git
#### 安装
使用我们提供的 yapi-cli 工具，部署 YApi 平台是非常容易的。执行 yapi server 启动可视化部署程序，输入相应的配置和点击开始部署，就能完成整个网站的部署。部署完成之后，可按照提示信息，执行 node/{网站路径/server/app.js} 启动服务器。在浏览器打开指定url, 点击登录输入您刚才设置的管理员邮箱，默认密码为 ymfe.org 登录系统（默认密码可在个人中心修改）。

    npm install -g yapi-cli --registry https://registry.npm.taobao.org
    yapi server 
    
#### 服务管理
利用pm2方便服务管理维护。

    npm install pm2 -g  //安装pm2
    cd  {项目目录}
    pm2 start "vendors/server/app.js" --name yapi //pm2管理yapi服务
    pm2 info yapi //查看服务信息
    pm2 stop yapi //停止服务
    pm2 restart yapi //重启服务

#### 升级
升级项目版本是非常容易的，并且不会影响已有的项目数据，只会同步 vendors 目录下的源码文件。
    
    cd  {项目目录}
    yapi ls //查看版本号列表
    yapi update //更新到最新版本
    yapi update -v {Version} //更新到指定版本
    
### 教程
* [使用 YApi 管理 API 文档，测试， mock](http://u.720life.cn/g/8a35642bd69eb006eb1f0259b3a6f6f09c8313c512923343a823759a07802b2a019ba35ec78ec8230fa05717f55b9b13) 
* [自动更新 Swagger 接口数据到 YApi 平台](http://u.720life.cn/g/8a35642bd69eb006eb1f0259b3a6f6f09d3a877fc6b9e7b53b57c147e57fd4e2113b39330c63456243084774f72c2953) 
* [自动化测试](http://u.720life.cn/g/8a35642bd69eb006eb1f0259b3a6f6f0d6ab48ddd92952400a111f137844b0e2859b0585939b7e801c53be3024263d4c) 

### YApi 插件
* [yapi sso 登录插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462605924f9b319e0bdae730dac5f2fb24c537c568075c01cd96a4a7a79f7e9a13) 
* [yapi cas 登录插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464ffde7debd827c13a3467abae3f7735b5643d841c662635e15baa46f74c7ff54)  By wsfe
* [yapi gitlab集成插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fc851fa28757c9a163887674fd66cb1a6e4eb6efbc796de809aa9dedc92338f0) 
* [oauth2.0登录](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466b877a526533ce999779619bf3d07d553e40932f385cb94f47cc3006ffb71ece) 
* [rap平台数据导入](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304624a13ca56609774696afed2fecb342722757c79d7a1730a53e35d6efcb36d747bf96c8965abc68775fc5ee633963a6b0) 
* [dingding](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b5b9df66f8a280c19fb8ae1b81f9ec1eb977c2e9736cdf4371f44edb631ce462)  钉钉机器人推送插件
* [export-docx-data](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467863f6b68fdc957d2b0397fe7b089e1ae2b311ea56424122acb799aec4fa4e4c905b250b21b369a81be13e792d1a2fe7)  数据导出docx文档
* [interface-oauth-token](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461e6fcd377a07f85eb18364439ccf70448b2f0a033dd2120707d2544953312e7ab41a74f43626459aa352085f5b63d016e19d992d6185e549b3bd35809657a2dd)  定时自动获取鉴权token的插件
* [import-swagger-customize](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b8bd584d05fabfb9c0f7f3b2d78252591c3174155cbf1656fbce5a03e514716052cca59a9bc9e225984187009f3ab9bed3fb93f6d0bf03d45f65f8ed1addab57)  导入指定swagger接口

### 代码生成
* [yapi-to-typescript：根据 YApi 的接口定义生成 TypeScript 的请求函数](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046836c4d1788b74c09e218805afb3e4b418ad0314a484db5574a79db98da2880a2) 
* [yapi-gen-js-code: 根据 YApi 的接口定义生成 javascript 的请求函数](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463f361bd8b1bf520076abb7bcd666dec0dba6261e15c1a26c5001e2b2cb70cdce36df7941f7f3639b3af7afa980f91712) 

### YApi docker部署（非官方）
* [使用 alpine 版 docker 镜像快速部署 yapi](http://u.720life.cn/g/8a0e6e781ca1335d5641e0f9d5e96ab9af821d7af8ca27aeff77c2a1ced8aa802b0f1e6cd6139043ea255f8917795280) 
* [docker-yapi](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469d6786217e7ddac33e453a0f65e2caa9fd1f76069ddf38a9b9608d98e469e41b) 
* [docker-compose一键部署yapi](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046958fcf8054153b82a9886e46e8ae255beba3abf068deef9df9396f1154c5bf63) 
* [docker-YApi: 更易用的 YApi 镜像](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c819b37f304fcedc8dd73fada851788129505fa6c9f777341b4e33c7291e8356) 
* [使用DockerCompose构建部署Yapi](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304684a60a23e9a87561553598378b703d63334899f05355bd3baf71f2d5f5ee1d89627092c865f49e382f578273ee4dc6dd2e62896bae1224eb7b2813ad0c4a1b3765ad5b384ee3a657b3157a1dfa1ba8bcd33431bddcb1a7180c997878a8dea40a9e2d60b2821f54955a333d37bf7c1b0fb16c9566d4b0a658322fd1511739771126c9a277b497c610bf222ab01f734f024f8c81d15eacd47dc8d23eadcc293d26) 

### YApi 一些工具
* [mysql服务http工具,可配合做自动化测试](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463f361bd8b1bf520076abb7bcd666dec05dc7e97048e0070f15bf37b13b5df977d577e2cd8bbd0a5bfd1be83ae2705acf) 
* [idea 一键上传接口到yapi插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ee0cd0ae1fef8f60772645b5d42bcd2d803245baaf6f68d774ef1b47ed16e1ad) 
* [idea 接口上传调试插件 easy-yapi](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d13494b09cb718ff0108d64d6106842f093745ad1d85554119f8f55789040303) 

### YApi 的一些客户
* 去哪儿
* 携程
* 艺龙 
* 美团
* 百度
* 腾讯
* 阿里巴巴
* 京东
* 今日头条
* 唯品支付 
* 链家网
* 快手
* 便利蜂
* 中商惠民
* 新浪
* VIPKID
* 马蜂窝

### Authors
* [hellosean1025](http://u.720life.cn/g/54145d0471d91890860f7f8463c030463f361bd8b1bf520076abb7bcd666dec0) 
* [gaoxiaomumu](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304603aeabc9552ad5f2fd005ae9f9ffbdb8) 
* [zwjamnsss](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461443a33db0a67dd8a112ba20a9b05a37) 
* [dwb1994](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a4847dec640fdf082f41e9ae2a2cc2b6) 
* [fungezi](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ab412898512c45a0f58914a1b04d1338) 


### License
Apache License 2.0




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)