## WxJava - 微信开发 Java SDK（开发工具包） [![LICENSE](https://img.shields.io/badge/License-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE) [![Badge](https://img.shields.io/badge/Link-996.icu-red.svg)](https://996.icu/#/zh_CN) [![Badge](https://img.shields.io/badge/Link-专属福利-red.svg)](https://mp.weixin.qq.com/s/dfwatgMgARaBjh421Todyg)

[![码云Gitee](https://gitee.com/binary/weixin-java-tools/badge/star.svg?theme=blue)](https://gitee.com/binary/weixin-java-tools)
[![Github](http://github-svg-buttons.herokuapp.com/star.svg?user=Wechat-Group&repo=WxJava&style=flat&background=1081C1)](https://github.com/Wechat-Group/WxJava)
[![GitHub release](https://img.shields.io/github/release/Wechat-Group/WxJava.svg)](https://github.com/Wechat-Group/WxJava/releases)
[![Maven Central](https://img.shields.io/maven-central/v/com.github.binarywang/wx-java.svg)](http://mvnrepository.com/artifact/com.github.binarywang/wx-java)
[![Build Status](https://travis-ci.org/Wechat-Group/WxJava.svg?branch=develop)](https://travis-ci.org/Wechat-Group/WxJava)
[![使用IntelliJ IDEA开发维护](https://img.shields.io/badge/IntelliJ%20IDEA-提供支持-blue.svg)](https://www.jetbrains.com/?from=WxJava-weixin-java-tools)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

#### 支持包括微信支付、开放平台、公众号、企业微信/企业号、小程序等微信功能的后端开发。

 
	 
		 
			 
         
				   
         
			 
			 
				 
					 
				 
			 
			 
				 
					 
				 
			 
			 
				 
					 
				 
			 
			 
				 
					 
				 
			 
		 
	 
 

### 重要信息
1. **2020-02-29 发布 [【3.7.0正式版】]https://github.com/Wechat-Group/WxJava/releases)**！
1. 新手重要提示：本项目仅是一个SDK开发工具包，未提供Web实现，建议使用 `maven` 或 `gradle` 引用本项目即可使用本SDK提供的各种功能，详情可参考 **[【Demo项目】](demo.md)** 或本项目中的部分单元测试代码；另外微信开发新手请务必阅读[【开发文档 Wiki 首页】](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046201a511e2ba300ebaea50f02340949bccde63eef5f1923397dd872a9caa4001b8da4c6d518fd86f02d29058dad9dff4ba39903333fb2dc80e1389737bee2c983c47887dd3dab77923a87ffdde257cdebe74816915ab4e374f0cd1c6925b261e552e7a7bb828f1fc3ef0941ce9124946b 
1. 技术交流群：想获得QQ群/微信群/钉钉企业群等信息的同学，请使用微信扫描上面的微信公众号二维码关注 `WxJava` 后点击相关菜单即可获取加入方式，同时也可以在微信中搜索 `weixin-java-tools` 或 `WxJava` 后选择正确的公众号进行关注，该公众号会及时通知SDK相关更新信息，并不定期分享微信Java开发相关技术知识；
1. 付费QQ群：（**注意：刚入群会有5分钟禁言，稍等片刻即可正常发言**） [![加入QQ群](https://img.shields.io/badge/QQ群-343954419-blue.svg)](http://shang.qq.com/wpa/qunwpa?idkey=731dc3e7ea31ebe25376cc1a791445468612c63fd0e9e05399b088ec81fd9e15) 或 [![加入QQ群](https://img.shields.io/badge/QQ群-343954419-blue.svg)](http://jq.qq.com/?_wv=1027&k=40lRskK)，或者请自行搜索群号`343954419`进行添加；当然由于某种原因无法入群的，可关注公众号后获取其他群的加入方式；
1. 钉钉群号： 30294972，或者[请点击链接申请加入钉钉企业组织](http://u.720life.cn/g/817e59162edd059e3bf9e401f9ed47c5a54199b94e95c24eeeb1b0346a8c767bf309a4215a68d3dddc94b20727dc4c5bd9e17fa048c46a2eab3a4d53840c87c6781ea17e83667d56763693a3028751c6a8c3fe152ba924202ee8b358eb707ef2b1dc85dd8116cc48fb3c25955255ec2f)  或者 [用手机钉钉APP扫码](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ef1ba300cdf9e88dd16cc5670fc1de4b051cd99399c2675577f9fa2f3af6e1ed50929f9a142abbc9b4847890c58abae532fa82e220f3f84f61752d43c297c2fe4)  申请加入。
1. 微信开发新手或者Java开发新手在群内提问或新开Issue提问前，请先阅读[【提问的智慧】](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f5210044125273f31569688ea3381c47a41430aaa047b52667b118d03cfa9296a136f6681d845421a308dc5cac9024fa5704596da2930f9ccddd2f673037d4be3951e1127a5459400330533a0df2cff10c7b848b7fdad4db345ec2533674da332672717fafee473f8f7bf398ae265dbf  [【开发文档Wiki】](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046baa7244917c0ef77762f29cdc461153c20dbeacc992383298ddc69d0da2b2df6)  ，避免浪费大家的宝贵时间；
1. 寻求帮助时需贴代码或大长串异常信息的，请利用 http://paste.ubuntu.com 

--------------------------------
### 其他说明
1. **阅读源码的同学请注意，本SDK为简化代码编译时加入了`lombok`支持，如果不了解`lombok`的话，请先学习下相关知识，比如可以阅读[此文章]https://mp.weixin.qq.com/s/cUc-bUcprycADfNepnSwZQ)；**
1. 如有新功能需求，发现BUG，或者由于微信官方接口调整导致的代码问题，可以直接在[【Issues】]https://github.com/Wechat-Group/WxJava/issues)页提出issue，便于讨论追踪问题；
1. 如果需要贡献代码，请务必在提交PR之前先仔细阅读[【代码贡献指南】](CONTRIBUTING.md)，谢谢理解配合；
1. 本SDK要求的最低JDK版本是1.7，还在使用JDK6的用户请参考[【此项目】]( https://github.com/binarywang/weixin-java-tools-for-jdk6) ，而其他更早的JDK版本则需要自己改造实现。
1. [开源中国本项目的首页]https://www.oschina.net/p/weixin-java-tools-new)，欢迎大家积极留言评分 🙂
1. SDK开发文档请查阅 [【开发文档Wiki】](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046baa7244917c0ef77762f29cdc461153c2cb66bbc8168f1a9215c0e9f55896bcbbf80856d1562096d7cef6255ea6a450d06482f6219110f83da192ac6a15347259a7b561087c948d2146eded8db6463b78c8603b6a868fa2e0bf8e92e30ee1aefd1d293fd2d92eae913948e47668fcd9b0a07bd1056ce037440f12ed03aea970b 
1. **如果本开发工具包对您有所帮助，欢迎对我们的努力进行肯定，可以直接前往[【托管于码云的项目首页】]http://gitee.com/binary/weixin-java-tools)，在页尾部分找到“捐助”按钮进行打赏，多多益善 😄。非常感谢各位打赏和捐助的同学！**
1. 各个模块的Javadoc可以在线查看：[weixin-java-miniapp]http://binary.ac.cn/weixin-java-miniapp-javadoc/、[weixin-java-pay]http://binary.ac.cn/weixin-java-pay-javadoc/、[weixin-java-mp]http://binary.ac.cn/weixin-java-mp-javadoc/、[weixin-java-common]http://binary.ac.cn/weixin-java-common-javadoc/、[weixin-java-cp]http://binary.ac.cn/weixin-java-cp-javadoc/、[weixin-java-open]http://binary.ac.cn/weixin-java-open-javadoc/
1. 本SDK项目在以下代码托管网站同步更新:
* 码云：https://gitee.com/binary/weixin-java-tools
* GitHub：https://github.com/wechat-group/WxJava

---------------------------------
### Maven 引用方式
注意：最新版本（包括测试版）为 [![Maven Central](https://img.shields.io/maven-central/v/com.github.binarywang/wx-java.svg)](http://mvnrepository.com/artifact/com.github.binarywang/wx-java)，以下为最新正式版。

```xml
 
   com.github.binarywang 
   （不同模块参考下文） 
   3.7.0 
 
```

  - 微信小程序：`weixin-java-miniapp`   
  - 微信支付：`weixin-java-pay`
  - 微信开放平台：`weixin-java-open`   
  - 公众号（包括订阅号和服务号）：`weixin-java-mp`    
  - 企业号/企业微信：`weixin-java-cp`


---------------------------------
### 版本说明

 
 点此展开查看 
  
1. 本项目定为大约每两个月发布一次正式版（同时 `develop` 分支代码合并进入 `master` 分支），版本号格式为 `X.X.0`（如`2.1.0`，`2.2.0`等），遇到重大问题需修复会及时提交新版本，欢迎大家随时提交Pull Request；
1. BUG修复和新特性一般会先发布成小版本作为临时测试版本（如`3.6.8.B`，即尾号不为0，并添加B，以区别于正式版），代码仅存在于 `develop` 分支中；
1. 目前最新版本号为 [![Maven Central](https://img.shields.io/maven-central/v/com.github.binarywang/wx-java.svg)](http://mvnrepository.com/artifact/com.github.binarywang/wx-java) ，也可以通过访问链接 [【微信支付】](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22com.github.binarywang%22%20AND%20a%3A%22weixin-java-pay%22) 、[【微信小程序】](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22com.github.binarywang%22%20AND%20a%3A%22weixin-java-miniapp%22) 、[【公众号】](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22com.github.binarywang%22%20AND%20a%3A%22weixin-java-mp%22) 、[【企业微信】](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22com.github.binarywang%22%20AND%20a%3A%22weixin-java-cp%22)、[【开放平台】](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22com.github.binarywang%22%20AND%20a%3A%22weixin-java-open%22)
分别查看所有最新的版本。 

 

----------------------------------
### 使用案例
完整案例登记列表，请[【访问这里】]https://github.com/Wechat-Group/weixin-java-tools/issues/729)查看，欢迎登记更多的案例。

以下为部分案例列表：

#### 开源项目：
- 基于微信公众号的签到、抽奖、发送弹幕程序：https://github.com/workcheng/weiya
- XxPay聚合支付：https://github.com/jmdhappy/xxpay-master
- 微同商城：https://gitee.com/fuyang_lipengjun/platform
- 微信点餐系统：https://github.com/sqmax/springboot-project
- 专注批量推送的小而美的工具：https://github.com/rememberber/WePush
- yshop意象商城系统：https://gitee.com/guchengwuyue/yshopmall
- wx-manage（微信公众号管理项目）：https://github.com/niefy/wx-manage
- 基于若依开发的微信公众号管理系统：https://gitee.com/joolun/JooLun-wx

#### 小程序：
- （京东）友家铺子，友家铺子店长版，京粉精选
- [喵星人贴吧助手(扫码关注)](http://u.720life.cn/g/0b1e802cae4421653873ac634f70b143b501e2f0d853c8d1fcd305fce14dbaa13f3af199c5f1a3fe29f1865b2d558ed839449251ec54243a78ddcc440e5b55fa) 
- 树懒揽书+
- 广廉快线，鹏城巴士等
- 当燃挑战、sportlight轻灵运动
- 360考试宝典
- 民医台
- 来一团商家版
- 史必达（史丹利）

#### 公众号：
- 中国电信上海网厅（sh_189）
- E答平台
- 宁夏生鲜365
- 通服货滴
- 神龙养车
- 沃音乐商务智能
- 光环云社群
- 手机排队
- [全民约跑健身便利店](http://u.720life.cn/g/36b70055edaf2cd6f28877c4c8e426145bcee1c8a013a6c6a2fe62433a5adb8d) 
- [洽洽食品]https://mp.weixin.qq.com/cgi-bin/showqrcode?ticket=gQFM8TwAAAAAAAAAAS5odHRwOi8vd2VpeGluLnFxLmNvbS9xLzAycDRPOXBZbVZib2UxMDAwME0wN2gAAgRIu4RbAwQAAAAA、[洽洽合伙人]https://mp.weixin.qq.com/cgi-bin/showqrcode?ticket=gQFP8jwAAAAAAAAAAS5odHRwOi8vd2VpeGluLnFxLmNvbS9xLzAyOUpJaU5VcXBlWTAxMDAwME0wN1oAAgSau4RbAwQAAAAA
- 民医台
- YshopMall
- 好行景区直通车以及全国40多个公众号

#### 企业号/企业微信：
- 洽洽企业号
- HTC企业微信
- 掌上史丹利

#### 其他：
- 高善人力资源
- [小猪餐餐](http://u.720life.cn/g/36ffb061987569450550171cebb4f2bd9983c969bae2f1bff5ac4ab108c4946f) 
- [餐饮系统](http://u.720life.cn/g/69bc678920091a4233a9bb77cd3373acdccbd05c5d5cb0477829c80b61b4fec1) 
- 微信公众号管理系统：http://demo.joolun.com
- 锐捷网络：Saleslink

----------------------------------
### 贡献者列表
特别感谢参与贡献的所有同学，所有贡献者列表请在[此处](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046201a511e2ba300ebaea50f02340949bc3e7fc9b676bb9da8f638291ab753f02a25c225c10d6532313807a7646060f663ab3609e8c0d7dfd0072a1016c63e5aacc22bdd751f5106c8b69939d45c564b659f9a7071cca9f3ca092dd95eb3f7a361 
 
 点击此处展开查看贡献次数最多的几位同学 

1. [chanjarster (Daniel Qian)](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d39dd8d452637e8e67b052f2b86c068e1e) 
1. [binarywang (Binary Wang)](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d315d264942efecc9b7f53d6b42d88f16e) 
1. [mgcnrx11](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d39eb9ef8f841598381d94b8fd31333ea0) 
1. [007gzs](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d33419949801adae43e030ee831aacb8dd) 
1. [aimilin6688 (Jonk)](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3a86f43abf38374bb144a17dde9f61582) 
1. [kakotor](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3940dd19e8fe7b2fd47722c64da0838b6) 
1. [kareanyi (MillerLin)](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3f4ede29bd281cc6d9ec95a60846663a9) 
1. [tianmu](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3ddd44c75425c588832c28c94d4d96f7a) 
1. [rememberber (周波)](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d31856bbca3c2fe758825c0bdf46e32550) 
1. [charmingoh (Charming)](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d33d7442be77753d49cf72bc453d850994) 

 

### GitHub Stargazers over time

[![Stargazers over time](https://starchart.cc/Wechat-Group/WxJava.svg)](https://starchart.cc/Wechat-Group/WxJava)     



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)