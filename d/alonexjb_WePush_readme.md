 
  
 
  
# WePush 
> 专注批量推送的小而美的工具  

[![码云Gitee](https://gitee.com/zhoubochina/WePush/badge/star.svg?theme=blue)](https://gitee.com/zhoubochina/WePush)
[![GitHub stars](https://img.shields.io/github/stars/rememberber/WePush.svg)](https://github.com/rememberber/WePush)
[![Build Status](https://travis-ci.org/rememberber/WePush.svg?branch=master)](https://travis-ci.org/rememberber/WePush)
[![GitHub release](https://img.shields.io/github/release/rememberber/WePush.svg)](https://github.com/rememberber/WePush/releases)
[![GitHub license](https://img.shields.io/github/license/rememberber/WePush.svg)](https://github.com/rememberber/WePush/blob/master/LICENSE.txt)

### 目前已经支持的消息类型
+ 模板消息-公众号  
+ 模板消息-小程序  
+ 微信客服消息  
+ 微信企业号/企业微信消息  
+ 阿里云短信  
+ 阿里大于模板短信  
+ 腾讯云短信  
+ 云片网短信  
+ E-Mail
+ HTTP请求（单次、批量、压测）

### 计划中支持的消息类型
+ 钉钉  
+ 又拍云短信  
+ 七牛云短信  
+ 华为云短信  
+ 网易云信短信  
+ 榛子云短信  
+ Luosimao短信  
+ 极光短信  
+ 极光推送  

### 功能&亮点
1. 支持自定义消息内容并批量推送  
2. 支持变量消息（可实现根据发送目标用户不同每条消息内容不一样）
3. 支持消息编辑、预览、消息管理  
4. 支持通过文件导入用户（txt、csv、excel）  
5. 支持通过MySQL导入用户  
6. 支持微信公众号全员推送  
7. 支持微信全家桶消息（公众号、小程序、企业号）
8. 支持各种粒度的定时推送  
9. 支持推送历史管理和失败重新推送  
10. 支持多账号管理和切换（微信） 
11. 支持各种搜索、导入、导出  
12. 小而美的可视化界面，支持亮暗多种外观风格  
13. 支持全局字体字号设置  
14. 支持推送结果邮件通知  
……

### 截图速览
 
   
    
   
   
 
   
    
   
  
 
   
    
   
  
 
   
    
   
 
 
   
    
   
 
 
   
    
   
 
 
   
    
   
 
 
   
    
   
 
 
   
    
   
 
 
   
    
   
 
 
   
    
   
 

### 更多外观
 
   
    
   
  
 
   
    
   
  

### 安装文件下载

[WePush下载地址](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e555c0e7bb22c80a17d8e8d05238c64018fe6b486264c05a811d0d32872769505dff8ab20a4922e81a38a251e054f4a97)   

安装之前请确认已经安装了jre1.8或者以上版本   
[jre下载地址](http://u.720life.cn/g/0832d3c13dcf440b8c2ddd37014597194dfce0f4546bd12c9ba469d981d9d729007ebfc8068b2baf5cdf0064d40d49999f37f1b6b13595a9266e81f5ec47670ab66be3c380b17ed62254f8a17be36e0e26b634f4bcb3b6ae465a896597ee1475)   

### 环境依赖
+ Java 8
+ lombok

### 使用到的一些小技术点
+ Java  
+ Java Swing  
+ 线程池  
+ 连接池（数据库：HikariCP、HTTP：PoolingHttpClient）  
+ HttpClient  
+ HttpAsyncClient  
+ 定时任务  
+ SQLite  
+ MyBatis  

### 遇到的麻烦和挑战
+ Swing界面不好控制，导致需要投入较多精力和耐心
+ 工作过于饱和，经常到半夜很晚才挤出一点时间
+ 要做的事情有很多，比如WePush中间件及其附属的集消息中心、通知报警、任务、批量、重试、统计等于一身的方便部署的Web管理应用
+ 陪家人时间变少或无
+ 锻炼身体时间变少或无
+ 越来越发现需要不断学习源码和底层的重要性

### 特别感谢
[WxJava](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ef1ba300cdf9e88dd16cc5670fc1de4b0964220f123ec45381aa31749eb44d89d)   
[Hutool](http://u.720life.cn/g/bf4d99695d155e8071cd504c849da2b4325a7ca36388aeee701f3965d379e718)   
[Darcula](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cc11d7eef8d7776cb1aa825a8a34fdb4cae0270ab2120e5ad1b28181c1fa4337)   
[BeautyEye](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e9ab0cf830d1493a03df0fb4ab13ea423f7069d22a23ca3f820e7b1b425da0fb9)   

### 特别说明
WePush所使用的图标来源于https://github.com/JetBrains/intellij-community项目  
版权、专利和许可都归其所有https://github.com/JetBrains/intellij-community/blob/master/LICENSE.txt  
如有冒犯，请及时通知我删除  
Icons in WePush are from Project:https://github.com/JetBrains/intellij-community  
Copy right,patent and license are belong to the "JetBrains/intellij-community"  
https://github.com/JetBrains/intellij-community/blob/master/LICENSE.txt  
If there is any offence, please inform me to delete them in time.  

### 开发&构建

https://gitee.com/zhoubochina/WePush/wikis/build

### 使用帮助

https://gitee.com/zhoubochina/WePush/wikis/help  
微信交流群：
 
   
    
   
 

### 鼓励&赞赏  
**如果WePush对您有所帮助或便利，  
欢迎对我每天下班和周末时光的努力进行肯定，  
您的赞赏将会给我带来更多动力**
 
   
    
   
 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)