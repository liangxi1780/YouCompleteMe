
[![star](https://gitee.com/comsince/vue-chat/badge/star.svg?theme=white)](https://gitee.com/comsince/vue-chat)
[![GitHub stars](https://img.shields.io/github/stars/comsince/vue-chat?style=social)](https://github.com/comsince/vue-chat)

# 飞享

![image](http://image.comsince.cn/fx-chat.png)

该项目是`飞享`聊天系统客户端源码

基于[universe-push]https://github.com/comsince/universe_push)的vue即时通讯web端实现，使用websocket进行消息通讯，支持文本，图片类型发送，支持实时音视频，支持音视频与[android-chat]https://github.com/comsince/android-chat)客户端互通

# 项目截图
* 消息提示

![image](./attachment/vue-chat-unread.png)

* 文字消息

![image](./attachment/vue-chat.png)

* 图片消息

![image](./attachment/vue-chat-pic.png)

* 视频消息

![image](./attachment/vue-chat-video.png)

# 项目演示
* [项目公测地址](http://u.720life.cn/g/70af7c450e8e9243027fbb0fb8b4fa79180717e84a7cf55ecfd84892d932e64b) 
* 请选择其中任何一个帐号密码进行登录即可
```properties
帐号：13800000000, 13800000001, 13800000002
密码：556677
```
* 暂时停止手机验证码注册登录，后续开通QQ群里面通知

## 版本规划
### V1.0.0
* 登录认证流程
* 实现朋友列表展示，用户信息获取
* 会话信息拉取，会话消息缓存
* 纯文本消息通讯
* 支持图片，视频消息展示
* 群会话功能

### V1.0.1
* 增加全屏幕模式支持，点击用户头像即可切换

![image](https://user-gold-cdn.xitu.io/2020/4/13/171719952947e62a?w=1518&h=655&f=png&s=170160)

### V1.0.2
* 计划增加音视频聊天功能
* 实现与android客户端音视频互通

> 语音通话

![image](https://user-gold-cdn.xitu.io/2020/3/20/170f70e65d19d2ac?w=2880&h=1800&f=png&s=1120425)

> 视频通话

![image](https://user-gold-cdn.xitu.io/2020/3/20/170f70e73e8ad91e?w=2880&h=1800&f=png&s=1323835)

### V1.0.3
* 增加好友搜索，好友添加功能，形成功能闭环

### V1.0.4
* 群组用户列表功能

### V1.0.5
* 增加websocket异步回调接口
* 增加创建群组功能
* 退出群聊
* 撤回消息
* 群组踢人与拉人
* 修改群名称

![image](https://user-gold-cdn.xitu.io/2020/5/8/171f4c271ba2b4dd?w=2064&h=1144&f=png&s=428322)

### V1.0.6
* 增加解散群组的功能
* 优化群组退出与解散交互体验
* 对于解散的群组与退出的群组,做删除会话处理
## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev
# 运行请先检查如下配置：TCP服务配置，HTTPS配置，是否支持WSS,是否支持HTTPS，HTTP监听端口8081,HTTPS监听端口8443

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://u.720life.cn/g/ccc863ff3c50910713546545d55dfc23e9ac185cec01d48f3e2685ba0355c450924049249f27d15b18089863ff85ef5c)  and [docs for vue-loader](http://u.720life.cn/g/52e9e4127a7148bfb51aad6bd35973c9001f49abb4ffa9f8150c1f15c44be0c0d8c9f6fef3e1c5f1fadd9874b953f690 



## 参考项目

* [Vue-chat](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304695e56d9632e759a6014dd7908654f9d3ce097ef0e560f9437d382abf868e12bc) 

## 依赖组件
* [常用的 vue 视频插件](http://u.720life.cn/g/6913b20471f2197a83652228c00116da8e93b8a65341dd4e194469d32a0df926) 
* [西瓜播放器](http://u.720life.cn/g/64fe6a8c906670e802e2aba8e693cea026042035803c64bd08d84ae2863f8834cd508b6af362401ec68193e5e100c682) 
* [图标Icon支持](http://u.720life.cn/g/e78198cbca568641bd2625675a127257dc4f7a4d61d238ee161598e78c947b2d975ea672729f9f87f7c9471d6bfcaae28657485ca7e7b2d3c56d309990e2642a831cbc44b6e7fb04822b27007b64e2e65c8287eb942a62e033868299d92a30d15409d8a3ca269c9cbbb2859650be869c) 

## 推荐项目

* [vue-wechat](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046be3d17006518f6bcfd71555f2a60f28251eb01c63488cf1741d915759f6c30ac) 
* [vue-chat](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304686749c16e6403f991c1c9c78a597996d3b3f2d881f8562a2200f80bc6c8e4dec) 
* [QRCodeLogin](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304661cc54263f265080c508002a77a77dd5a27d4265675e5deaf68c39c9d9051c8aa2d0442eccff53de57f23f2fad6b099acae20f87d5fff8f73bb090c66efeef5366e9db460046b4659ac16695ff690a42)  说明二维码和密码登录的切换操作


## 开源协议

本项目使用非商业性署名协议[Creative Commons Attribution Non Commercial 3.0 Unported](LICENSE)

## 一次性赞助

但是随着项目的增长，也需要相应的资金支持，你可以通过以下方式来赞助此项目

| 支付宝      | 微信| 
| :--------: | :--------:| 
| | |

## 技术支持

如果公司采用本项目或者需要有商业需求，需要二次开发,提供技术支持,联系QQ：`1282212195`


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)