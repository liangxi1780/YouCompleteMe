#Spring-Boot-Tio
使用SpringBoot，融合[tio即时通讯框架](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d8cd0e48e89b4be8f044a1f7754d6b745e127e95621e7a37871e7e201d83720cd  "tio即时通讯框架")。


tio采用 消息头+消息体的模式，为了兼容现有设备的Socket（无消息头），对Server的Handler进行调整，encode加消息头；decode无消息头。

测试类在test/，直接运行XXXClientTest的main方法即可。



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)