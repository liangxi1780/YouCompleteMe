![logo](https://raw.githubusercontent.com/zlmediakit/ZLMediaKit/master/logo.png)

[english readme](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f83be80a631d4d5711330af8f92a39bd331ec1fa3b84603db46d6da34835461dc2d56f464a1ed9c987ca1e42411344ad8b3b56fa7312dfc6c6006d2189f2a82f) 

# 一个基于C++11的高性能运营级流媒体服务框架

 [![Build Status](https://travis-ci.org/xiongziliang/ZLMediaKit.svg?branch=master)](https://travis-ci.org/xiongziliang/ZLMediaKit)


## 项目特点

- 基于C++11开发，避免使用裸指针，代码稳定可靠，性能优越。
- 支持多种协议(RTSP/RTMP/HLS/HTTP-FLV/Websocket-FLV/GB28181/MP4),支持协议互转。
- 使用多路复用/多线程/异步网络IO模式开发，并发性能优越，支持海量客户端连接。
- 代码经过长期大量的稳定性、性能测试，已经在线上商用验证已久。
- 支持linux、macos、ios、android、windows全平台。
- 支持画面秒开、极低延时([500毫秒内，最低可达100毫秒]https://github.com/zlmediakit/ZLMediaKit/wiki/%E5%BB%B6%E6%97%B6%E6%B5%8B%E8%AF%95))。
- 提供完善的标准[C API]https://github.com/xiongziliang/ZLMediaKit/tree/master/api/include),可以作SDK用，或供其他语言调用。
- 提供完整的[MediaServer]https://github.com/xiongziliang/ZLMediaKit/tree/master/server)服务器，可以免开发直接部署为商用服务器。
- 提供完善的[restful api]https://github.com/xiongziliang/ZLMediaKit/wiki/MediaServer%E6%94%AF%E6%8C%81%E7%9A%84HTTP-API)以及[web hook]https://github.com/xiongziliang/ZLMediaKit/wiki/MediaServer%E6%94%AF%E6%8C%81%E7%9A%84HTTP-HOOK-API)，支持丰富的业务逻辑。
- 打通了视频监控协议栈与直播协议栈，对RTSP/RTMP支持都很完善。
- 全面支持H265/H264/AAC/G711。

## 项目定位

- 移动嵌入式跨平台流媒体解决方案。
- 商用级流媒体服务器。
- 网络编程二次开发SDK。


## 功能清单

- RTSP[S]
  - RTSP[S] 服务器，支持RTMP/MP4/HLS转RTSP[S],支持亚马逊echo show这样的设备
  - RTSP[S] 播放器，支持RTSP代理，支持生成静音音频
  - RTSP[S] 推流客户端与服务器
  - 支持 `rtp over udp` `rtp over tcp` `rtp over http` `rtp组播`  四种RTP传输方式 
  - 服务器/客户端完整支持Basic/Digest方式的登录鉴权，全异步可配置化的鉴权接口
  - 支持H265编码
  - 服务器支持RTSP推流(包括`rtp over udp` `rtp over tcp`方式)
  - 支持任意编码格式的rtsp推流，只是除H264/H265/AAC/G711外无法转协议

- RTMP[S]
  - RTMP[S] 播放服务器，支持RTSP/MP4/HLS转RTMP
  - RTMP[S] 发布服务器，支持录制发布流
  - RTMP[S] 播放器，支持RTMP代理，支持生成静音音频
  - RTMP[S] 推流客户端
  - 支持http[s]-flv直播
  - 支持websocket-flv直播
  - 支持任意编码格式的rtmp推流，只是除H264/H265/AAC/G711外无法转协议
  - 支持[RTMP-H265](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a9d09c8993e88d164d53bc2aa772775dc0caea6f3dd827a5f2bbd97a49e3a57) 

- HLS
  - 支持HLS文件生成，自带HTTP文件服务器
  - 通过cookie追踪技术，可以模拟HLS播放为长连接，实现丰富的业务逻辑
  - 支持完备的HLS用户追踪、播放统计等业务功能，可以实现HLS按需拉流等业务
  - 支持HLS播发器，支持拉流HLS转rtsp/rtmp/mp4

- HTTP[S]
  - 服务器支持`目录索引生成`,`文件下载`,`表单提交请求`
  - 客户端提供`文件下载器(支持断点续传)`,`接口请求器`,`文件上传器`
  - 完整HTTP API服务器，可以作为web后台开发框架
  - 支持跨域访问
  - 支持http客户端、服务器cookie
  - 支持WebSocket服务器和客户端
  - 支持http文件访问鉴权

- GB28181
  - 支持UDP/TCP国标RTP(PS或TS)推流，可以转换成RTSP/RTMP/HLS等协议

- 点播
  - 支持录制为FLV/HLS/MP4
  - RTSP/RTMP/HTTP-FLV/WS-FLV支持MP4文件点播，支持seek
  
- 其他
  - 支持丰富的restful api以及web hook事件 
  - 支持简单的telnet调试
  - 支持配置文件热加载
  - 支持流量统计、推拉流鉴权等事件
  - 支持虚拟主机,可以隔离不同域名
  - 支持按需拉流，无人观看自动关断拉流
  - 支持先拉流后推流，提高及时推流画面打开率
  - 提供c api sdk
  - 支持FFmpeg拉流代理任意格式的流
  - 支持http api生成并返回实时截图
  
## 更新日志
  - 2020/5/17 新增支持hls播发器，支持hls拉流代理


## 编译以及测试
**编译前务必仔细参考wiki:[快速开始]https://github.com/xiongziliang/ZLMediaKit/wiki/%E5%BF%AB%E9%80%9F%E5%BC%80%E5%A7%8B)操作!!!**

## 怎么使用

 你有三种方法使用ZLMediaKit，分别是：

 - 1、使用c api，作为sdk使用，请参考[这里](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f83be80a631d4d5711330af8f92a39bd20833305377eca9c6378e424edb1400838e7f8cf5f634ad5f733c8fd801c18c4cae7f61b15ea29133bc5590ff984e193 
 - 2、作为独立的流媒体服务器使用，不想做c/c++开发的，可以参考[restful api]https://github.com/xiongziliang/ZLMediaKit/wiki/MediaServer%E6%94%AF%E6%8C%81%E7%9A%84HTTP-API)和[web hook](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f83be80a631d4d5711330af8f92a39bd0ee9cfd74c4fccefa30cc0b7d9d99dd6ead23c93bdf08b5d70bb1ea79a8a8bef91ec196046459a9a39a86de6ca6326c9d4a3f42cc94db3a7777a01b4845f0550720138eab81abd52e6866960cc5f223e 
 - 3、如果想做c/c++开发，添加业务逻辑增加功能，可以参考这里的[测试程序](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f83be80a631d4d5711330af8f92a39bd20833305377eca9c6378e424edb14008a845aa18ab4420aa78cc110d1142a1e2 

## Docker 镜像

你可以从Docker Hub下载已经编译好的镜像并启动它：

```bash
docker run -id -p 1935:1935 -p 8080:80 gemfield/zlmediakit:20.04-runtime-ubuntu18.04
```

你也可以根据Dockerfile编译镜像：

```bash
bash build_docker_images.sh
```

## 参考案例

 - [IOS摄像头实时录制,生成rtsp/rtmp/hls/http-flv](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb773d42d286c1d12387d8b2c87d2b9a2aad52a18ca67ca59d3acabcf3fe3bd24) 
 - [IOS rtmp/rtsp播放器，视频推流器](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6edbc9038b6094e1e342b363e47cba7616b39b40e654430b240d7767b15f062d6d) 
 - [支持linux、windows、mac的rtmp/rtsp播放器](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f83be80a631d4d5711330af8f92a39bdbe40ca05209167ef6d4c791830ed3c16) 
 - [基于ZLMediaKit分支的管理WEB网站](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462e876d9eafaafadf1380086b6afee44eefda1aa10e28b51ab4f5bd358d21f76e) 
 - [基于ZLMediaKit主线的管理WEB网站](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e01b9008e9c829a987c9055fb2dda37f4f0c22eb8d2f3bc99dcb07c9e0bbed86b) 
 - [DotNetCore的RESTful客户端](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304655dc9df767b56b2822210b2b2d3e794bfdda9467f7a44aa6beaa5cff7d834c29ca483b1b7d334ac3fbccc16ffba2abfb) 
 - [GB28181-2016网络视频平台](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304678bc4b93bac6438acc107d3189c633dc) 
 

## 授权协议

本项目自有代码使用宽松的MIT协议，在保留版权信息的情况下可以自由应用于各自商用、非商业的项目。
但是本项目也零碎的使用了一些其他的开源代码，在商用的情况下请自行替代或剔除；
由于使用本项目而产生的商业纠纷或侵权行为一概与本项项目及开发者无关，请自行承担法律风险。

## 联系方式

 - 邮箱： (本项目相关或流媒体相关问题请走issue流程，否则恕不邮件答复)
 - QQ群：542509000

## 怎么提问？

如果要对项目有相关疑问，建议您这么做：

 - 1、仔细看下readme、wiki，如果有必要可以查看下issue.
 - 2、如果您的问题还没解决，可以提issue.
 - 3、有些问题，如果不具备参考性的，无需在issue提的，可以在qq群提.
 - 4、QQ私聊一般不接受无偿技术咨询和支持([为什么不提倡QQ私聊](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f83be80a631d4d5711330af8f92a39bd0ee9cfd74c4fccefa30cc0b7d9d99dd6dd5dc9755bc03b59b223913a2d82932d974fe4eee302ea958bab3e5cc3a21b983d8a153d54aa583197c7d4571b1c0107f55d2c89f8d4fc008d857fd0cf4a12eaf08fb47bf4e98eb62f9a9c810c8f9f6ef4dc0facf2bf7b85ec10a2865f6bb708e85adfc61d98dccf55fd4fdf09de1f2698f99a9d452ed203249cdb668c70b838 

## 致谢

感谢以下各位对本项目包括但不限于代码贡献、问题反馈、资金捐赠等各种方式的支持！以下排名不分先后：

[老陈](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304657080654dc7f4095627378fba15f06b9) 
[Gemfield](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466be7ce33a74ecec21065be083ba46346) 
[南冠彤](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ddbe8aafef47f4c615f36e797b121678) 
[凹凸慢](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046615c1a5d15fd9ff3de494f764d103b5c) 
[chenxiaolei](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046171c009d777caa302febaede90f904d1) 
[史前小虫](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468cf7854c6c9f418b7b50e44a1c98ff05) 
[清涩绿茶](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461307d841d0c78ebef32b201a6ac76bd0) 
[3503207480](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046023b67035b08d308b2db2684b6b33613) 
[DroidChow](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b368495b6a5cd416951b193741fe690a) 
[阿塞](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b6d30fddd08787b4b9053dcb8c997a11) 
[火宣](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464574a325f1cba4924fcf5366ff633d64) 
[γ瑞γミ](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e4356dc437f68e97b3d8257908d9fbe) 
[linkingvision](http://u.720life.cn/g/618364a97f17bd8768257eaf44a3ebf9e1972531a41cb6498d122b8b43b0cb23) 
[茄子](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ada38250efd3ab0cabd6a3b5e664dd7c720190e4a5dd1bfaaa846a4243f8a7f1) 
[好心情]( )
[浮沉](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466edd5d8ecd59062a2f64c6eef2ca6e8e) 

## 捐赠

欢迎捐赠以便更好的推动项目的发展，谢谢您的支持!

[支付宝](http://u.720life.cn/g/bb9e19de933fd87f05600116164183c0b3ddd62d3854e3432c88c12f9e59c662974f62f6da7e176dc784afd82d1e81619c7885c8b408c4071e950a7c493055cb56e76c85b869701b4e4fb4877a02578c) 

[微信](http://u.720life.cn/g/bb9e19de933fd87f05600116164183c0b3ddd62d3854e3432c88c12f9e59c662974f62f6da7e176dc784afd82d1e81619c7885c8b408c4071e950a7c493055cbf2f8ada2f88cde0647b478d3bb1307ba) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)