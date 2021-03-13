## smart-socket
smart-socket是一款国产开源的Java AIO框架，追求代码量、性能、稳定性、接口设计各方面都达到极致。如果smart-socket对您有一丝帮助，请Star一下我们的项目并持续关注；如果您对smart-socket并不满意，那请多一些耐心，smart-socket一直在努力变得更好。
### Maven
     
         org.smartboot.socket 
         aio-core 
         1.3.1 
     

[开发手册]http://smartsocket.mydoc.io/)（很抱歉个人开源项目，文档更新会有点滞后）

## 工程结构
1. aio-core		
smart-socket的核心代码
2. smart-protocol-http		
简单实现Http协议编解码，目前的实现并不规范，仅合适ab测试
3. smart-protocol-p2p	
实现了私有协议P2P，性能测试也是基于该协议进行的

## 性能测试报告

| 项目 | 结果 |
| --- | --- |
|CPU| i7-4790 3.60Ghz|
|内存| 8G|
|测试代码|服务端：P2PServer，客户端：P2PMultiClient|
|测试时长|大于两分钟（服务端与客户端启动后的第一分钟数据是无效的，因为实际未跑满一分钟）
|时间单位|1分钟|
|数据总流量|7064MB|
|消息大小|33B|
|消息数|224484842|

## 标题党
- [《每秒处理 500W 条消息，人、机为之颤抖》](http://u.720life.cn/g/1dbc517b01e71dde51eaf55b6f5fa83342e25fc9a1469857d551c296cc273b1ab7e11c3d57a5115a1bfb7d15a6ce2ca4f4e8f9a61989717ee56dbf7a371f0be0) 
- [《再见，Netty！你好，smart-socket!》](http://u.720life.cn/g/1dbc517b01e71dde51eaf55b6f5fa83342e25fc9a1469857d551c296cc273b1ab7e11c3d57a5115a1bfb7d15a6ce2ca4f4e8f9a61989717ee56dbf7a371f0be0) 

## 社区互助
如果您在使用的过程中碰到问题，可以通过下面几个途径寻求帮助，同时我们也鼓励资深用户给新人提供帮助。

1. 加入QQ群：172299083   
2. Email：zhengjunweimail@163.com
3. [开源问答](http://u.720life.cn/g/1dbc517b01e71dde51eaf55b6f5fa83387d0b98cc5171fc0b7e222dfc1e6a2c50dc66587dadcf23f227f3053a3979174e2dcfbef9a95b73289cb9388d528e56a) 

## 参与贡献
我们非常欢迎您的贡献，您可以通过以下方式和我们一起共建 :smiley:：

- 在您的公司或个人项目中使用 smart-socket。
- 通过 [Issue](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ed58d661652530124bc457132b64b31433a867bbbba267defa62d9a75d182d39e)  报告 bug 或进行咨询。
- 提交 [Pull Request](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ed58d661652530124bc457132b64b3143dc25dc45bfecdccf8e3461144579e78f)  改进 smart-socket 的代码。
- 在开源中国发表smart-socket相关的技术性文章。

## 推荐项目
- [NIO版smart-socket（无限期暂停维护...）](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d8d8495baa320a0d3c5980163749941c1190790e7f587b5d007a2f4d3331fdade) 
- [smart-boot](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d40441255f12016236afb93f35391567477b6b696e5340ee7c6b6a0e3c1628084) 
- [maven-mydalgen-plugin](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d40441255f12016236afb93f353915674eb242d6ba3968a68a0c2387aec683957b2aa7fde034341071e6ea43ee10ec5ac) 

## 关于作者
Edit By 三刀  
E-mail:zhengjunweimail@163.com  
QQ:504166636

Update Date: 2018-02-03


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)