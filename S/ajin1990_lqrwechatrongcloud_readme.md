高仿微信6.5.7（融云版）
============

## 目录
* [一、简述](#一、简述)
* [二、功能](#二、功能)
* [三、效果图](#三、效果图)
* [四、其他相关](#四、其他相关)
* [五、打赏支持](#五、打赏支持)

# 一、简述

>本项目由 wangjin 个人独立开发。
>
>项目博客地址：[高仿微信6.5.7（融云版）](http://u.720life.cn/g/edab4f07812b57c7ea69fa7b67a55e9e994ea7855abc0da62448319e39756ef77a924e77d7b429b01a4b94b40c93081f) 
>
>项目源码地址：[码云：LQRWeChatRongCloud](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36b2e70f66edb9b2391e1ec2ebf7ff68a756e9a2e3a9d8502a516a9dbc3d0e9271f0d77c25c2815295d1d75213a934a6be7) 
>
>项目DemoApp下载：[Demo](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36b2e70f66edb9b2391e1ec2ebf7ff68a756e9a2e3a9d8502a516a9dbc3d0e9271f2b159478bd07095edd40b1dc656ffc7a1340d50edff892bdcc8a1a837ab02f2bcf0392f272d1fca501be6516c519c2a2d2a48eecf49c7a20f4484b185e7c0e4ad066c5ac845f2993ad88a1ae7de535f8c8fc587d2d0f9fd7f11d7eb568d62ff9aadf6cd5b7f89f5311d59b712fa503ed495867dcccb0afcbce7ea19bd0893fe2ab29a0eb277d0f2aa228793523ca37ea5db7e25bdd248c3ab8e4e5f8e9de6e8f) 
	
## 1、简单介绍一下：
这个项目是本人独立开发的第二个高仿微信项目，仿最新版微信6.5.7（除图片选择器外）。本项目基于融云SDK，使用目前较火的 Rxjava+Retrofit+MVP+Glide 技术开发。相比上个版本，加入发送位置消息，红包消息等功能。本项目由码云平台托管，欢迎start和fork~~

## 2、制作该开源项目的原因有：

1. 熟练使用 Rxjava+Retrofit+MVP+lambda 等新安卓技术。
2. 熟悉融云等SDK的使用。
3. 向高手进阶过渡。

## 3、统一回复下网友的问题：
有网友说看我上一个项目有别人提出的很多问题，而且我都没有回复并解决，实际是有的，只不过那时已经在着手准备开发这个新的高仿微信，而且因为上一个版本使用的是网易云SDK，开发上比较简单，同时该SDK的封装实在是太好了，所以没地方可以施展Retrofit，达不到我预计的提升要求，于是便选用了融云SDK干脆做了一个新的，上版中存在的一些问题已经在这个版本中基本解决，同时制作并更新了几个自己的库（如：表情库和语音库等）。

# 二、功能

## 1、好友

1. 查询好友
1. 发起添加好友请求
1. 查看好友个人信息
1. 设置备注
1. 删除好友
1. 扫码加好友
1. 查看新加朋友

## 2、群组

1. 拉人进群
1. 踢人去群
1. 修改群昵称
1. 查看群二级码
1. 扫码加入群组
1. 解散群（群主）
1. 退出群（群成员）

## 3、个人

1. 查看头像
1. 上传更新头像
1. 修改个人昵称
1. 查看个人二维码

## 4、会话

1. 会话置顶
1. 取消置顶
1. 删除会话
1. 撤回消息
1. 发送文本消息
1. 发送图片消息
1. 发送视频消息
1. 发送语音消息
1. 发送贴图消息
1. 发送位置消息
1. 发送红包消息

## 5、系统

1. 登录
1. 注册
1. 退出当前账号
1. 退出APP

## 6、尚未完成

1. 消息通知
1. @功能
1. 对方输入状态提示

# 三、效果图

![主界面](screenshots/1.gif)
![会话控制](screenshots/2.gif)
![录制、发送语音](screenshots/3.gif)
![发送表情文字](screenshots/4.gif)
![发送红包](screenshots/5.gif)
![抢红包](screenshots/6.gif)
![发送位置](screenshots/7.gif)
![录制、发送小视频](screenshots/8.gif)
![选择、发送图片](screenshots/9.gif)
![查看、撤回消息](screenshots/10.gif)
![拉人入群](screenshots/11.gif)
![踢人出群](screenshots/12.gif)
![修改群昵称](screenshots/13.gif)
![发起群聊](screenshots/14.gif)


# 四、其他相关

## 1、该项目使用到的技术有：

1. Rxjava 2.0
1. Retrofit 2.0
1. MVP 
1. Glide
1. lambda
1. ...

## 2、用到的主要库有：

### 主要的大神库：

1. [鸿神的AutoLayout](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466abac79393294543e733de6a55212261110d12ea87f67f0817fd4c17012c1b9c7f5d209b711443801cc99ba2f172cdae) 
1. [郭神的LitePal](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dc27476bd8068d6098d299797d2dcf002d51aa6ddee21196da21faa4e9159122) 
1. [bingoogolapple的万能刷新控件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ce98eb8618488063718f408cfe11985786c42082956908af812c72cd0c3fec9d80e4eeb5bd84b2025fedca5807d060dc) 
1. [bingoogolapple的二维码控件扫描库](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ce98eb8618488063718f408cfe119857336ce778899df57b4da8364f8f9b63915788a64484d566ec22b90dd826f5ea35) 
1. [CJT2325的仿微信拍照Android控件](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304669f5756ea6b0a0396ef6756e425e6dd9ceb4564a9d8d7dc41bc0fb89c513f504) 
1. ...

### 自己(wangjin)做的库：

1. [万能适配器](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304618fce4bf24c63bb28f66b52d7b8ce303489fefbaad365dc8f957c397064fcbb9) 
1. [包装过的RecyclerView](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a15b6efbb51969928a4984ad31725d49a05fdad67c228c87b7d727a8a4a26f99) 
1. [高仿微信表情库](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467dd51c5efbfaf403c2a519e9b0a9b29bd1a21fe75d68aa847368b96d47cbebd7) 
1. [高仿微信主意库](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bd2e31925e1fc4b838fd299c1fcadd820c299091c6b282133baed460a5ffdc06) 
1. [高仿微信图片选择器](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a56229ce99f8f93566ed0207f55ddc4e919e34ccbcb901cf9c4cfdcdce452165) 
1. [高仿微信九宫格控件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c3c95ff71a31cf509694b5f50a01d91c26b4cbe6d143a53cf29efbbb6bd000a8) 
1. [常用选项条目库](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ba3ad87a214a6b89ed87f8244ec92f6c6684a552096f0b4aaf115e8dceae93db) 

## 3、说明与鸣谢：

不提供测试号，请使用自己手机注册后登录，因为本人手机号有限，测试上很有局限，可能存在一些我不知道的bug，请多包涵，可在项目中提出issue。本人做这个项目只为提升个人安卓开发能力，故依赖融云官方给出的server端做为本项目的后台服务，该server源码使用Node.js开发，目前本人只会用java开发后端，所以如果要搞点别的功能的话，目前是不可能啦，有兴趣的同学可以看看这个[嗨豹 IM 应用服务器]https://github.com/sealtalk/sealtalk-server)，当然融云也有它的坑，特别是红包module，我干脆不用它的了，希望该项目可以帮到那些正在踩坑的人（至少我已经踩了一次了，嘿嘿），此外，很感谢很多网友对我的支持，还有专门跑到CSDN跟我私信给我鼓励的，真的很感动，谢谢。

# 五、打赏支持

最后，如果觉得本项目对您有用，请随意打赏，鼓励我继续创作，谢谢啦。

![wechat](screenshots/wechat_pay.png)
![alipay](screenshots/alipay.png)





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)