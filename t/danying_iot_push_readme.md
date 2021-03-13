# iot_push
基于netty+mqtt 3.1.1协议开发的物联网消息推送框架。

 ## 项目目录
 * [mqtt简介](#1)
 * [功能](#2)
 * [如何使用](#3)
 ## 更新日志
 基于netty4.1-final+springboot实现的 Mqtt 3.1.1 物联网标准推送协议
 ##  mqtt简介 
 MQTT 协议是 IBM 开发的即时通讯协议，相对于 IM 的实际上的准标准协议 XMPP 来说，MQTT 更小，更快，更轻量。MQTT 适合于任何计算能力有限，工作在低带宽、不可靠的网络中的设备，包括手机，传感器等等。
 ##  功能 
 
 **## 服务端  example(iot_push_server_starter_test)**
 
 #### 已实现：
 * 发布订阅功能
 * 遗言通知
 * 会话session数据
 * 发布保留消息
 * 主题过滤（/test 会接受到 /test/yy 的主题消息）
 * 实现标准的 qos0 qos1 qos2消息确认机制
 * ssl加密
 * 支持ws协议
 * 集成spring容器
   
 
 ####  如何使用 
  * 安装lombok插件  
  * 下载源码
  * springboot
  * jdk8
  * 导入IDE
  * 配置yml 或者properties 文件 [yml](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b8b53ffee22f744d8d777bb274c925df019f7bbaf17e8a9333dbd583d0ce33a3e337dfa9f199183bbd149f13adc57974e54c8b03ca86dd692d37ed28e6ad247fff6be1e6b3e5330c20aef9c0dbcbee04ec3112e6f942df97eb6d720beca112d60a785a950e7129c9f13ada3675840768)   
  * 简单测试：运行包 test 下的 测试 文件，即可开启测试客户端。
  * 压力测试：推荐使用jmeter 的mqtt插件 [插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465dd3313cb342aa294026ef463ab58078f80f6c7af6b715cf829fe09d0a0abb7a) 
 
  **## 客户端  example(iot_push_client_starter_test)**
  
  * 基于springboot 配置方式[yml](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b8b53ffee22f744d8d777bb274c925df019f7bbaf17e8a9333dbd583d0ce33a38dfa1db08419e8dc18e177b71d427df0dd3cae35381dcc564a7974434d0a4c3debad0980a187a2c26a01049e90694321891b598d2b741d4de4c5b377d07cd2b514a8ae9be0a196157845eef65b181d38) 
  
  * 配置实现 MqttListener 类并添加MqttMessageListener指定订阅的topic跟服务质量
     
  * @Autowired Procuder producer 即可使用;
    
  * 编码 [java](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b8b53ffee22f744d8d777bb274c925df019f7bbaf17e8a9333dbd583d0ce33a38dfa1db08419e8dc18e177b71d427df0dd3cae35381dcc564a7974434d0a4c3d2df8778bf46d5486ab4ebc159dca9e1a2432b57c31424ba2bf163810e5bb96a35557db646a0bb5ac6ec47e271d54901f) 
    
 ### 交流群号 658212670

 




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)