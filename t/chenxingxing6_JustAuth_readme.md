 
	   
 
 
	 Login, so easy. 
 
 
	 
		  
	 
	 
		  
	 
	 
		  
	 
	 
		  
	 
	 
		 
	 
	 
	    
	 
	 
		  
	 
 

 
     
         
                 
                 
                 
                 
                 
                 
                 
                 
                 
                 
                 
                 
                 
                 
                 
         
     
     
         
                 
                 
                 
                 
                 
                 
                 
                 
                 
         
     
 

-------------------------------------------------------------------------------



JustAuth，如你所见，它仅仅是一个**第三方授权登录**的**工具类库**，它可以让我们脱离繁琐的第三方登录SDK，让登录变得**So easy!**

项目开源地址：[gitee](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9894d7f9ce3e60d4881ec4b106227d88476)  | [github](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046066dd74459bee98bfd188515b03f16770c296c2a74d25b559d1d9874813de6f8) 

## 特点

废话不多说，就俩字：

1. **全**：已集成十多家第三方平台（国内外常用的基本都已包含），后续依然还有扩展计划！
2. **简**：API就是奔着最简单去设计的（见后面`快速开始`），尽量让您用起来没有障碍感！

## 快速开始

- 引入依赖
```xml
 
     me.zhyd.oauth 
     JustAuth 
     1.9.5 
 
```
- 调用api
```java
// 创建授权request
AuthRequest authRequest = new AuthGiteeRequest(AuthConfig.builder()
        .clientId("clientId")
        .clientSecret("clientSecret")
        .redirectUri("redirectUri")
        .build());
// 生成授权页面
authRequest.authorize();
// 授权登录后会返回code（auth_code（仅限支付宝））、state，1.8.0版本后，可以用AuthCallback类作为回调接口的参数
// 注：JustAuth默认保存state的时效为3分钟，3分钟内未使用则会自动清除过期的state
authRequest.login(callback);
```

**配套Demo**：
- [Springboot版](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d98962baab8e3c248c30c9d34dcaa7c90d6a) 
- [jFinal版](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461305096b70886e73e4eb7440d4188fe05b509d4a8bbfdb2b02e67bfe8041555a) 
- [ActFramework版](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d7ffd2db1661ab704424145ddefe4db9b886c542662872da08b8b64e31d94199) 

**扩展工具**

- [justauth-spring-boot-starter](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304695c90a9189b8e3d77cd5670079fb66cb2f90e49815a63eb0f468accd72a0fbf97628f425c2855f1cf0ab313c30164bf9  Spring Boot 集成 JustAuth 的最佳实践

**配套SpringBoot starter**：

[justauth-spring-boot-starter](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304695c90a9189b8e3d77cd5670079fb66cb2f90e49815a63eb0f468accd72a0fbf9c1c997ea09e9304956995bc84259d450) 

具体的例子可以参考：

- [实现Gitee授权登录](http://u.720life.cn/g/5d81a8ca0ea302f3ba1dc8d3b9aead0f8e6c7cc866eb89b5f0e55201f8c0f704) 
- [实现Github授权登录](http://u.720life.cn/g/0da1eacdf39532cff4a861ca237e150c75f8555b84cea17342cdf7e96795b642) 
- [Spring Boot 快速集成第三方登录功能](http://u.720life.cn/g/031634f1d22d2e7585cda6928e6c86bc056337eef62288ed6aca63f6365b4ba3) 

#### API列表
|  :computer: 平台  |  :coffee: API类  |  :page_facing_up: SDK  |
|:------:|:-------:|:-------:|
|     |  [AuthGiteeRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f3128dae0ea4c36b11fcb1f1e3c8a74047cb4f203c0f6a67ed2c5982d823e4628)   |  参考文档  |
|     |  [AuthGithubRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f3128dae0ea4c36b11fcb1f1e3c8a74047cb4f203c0f6a67ed2c5982d823e4628)   |   参考文档  |
|     |  [AuthWeiboRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f3128dae0ea4c36b11fcb1f1e3c8a74047cb4f203c0f6a67ed2c5982d823e4628)   |   参考文档   |
|     |  [AuthDingTalkRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f2d12f60ea75700c025625584043b3a38a449e546136bd9efe4b83dce1a627ee5)   |   参考文档   |
|     |  [AuthBaiduRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f475a630befad01e9fa80e73fdd53cff1788817dd9f3c4ad9136c0d472c086ac0)   |   参考文档   |
|     |  [AuthCodingRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f3d58dbc6e4461a215c8d5b42d37a46e8a754c5f9752f273526f9e51596569dc6)   |   参考文档  |
|     |  [AuthTencentCloudRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fd68c97c77feda923ba6d3352e24518060678dbe0a81f009ec38eda256b0048b3a70ac4315186f3c07d889025a72d1759)   |   参考文档  |
|     |  [AuthOschinaRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fb3ed3e2599032fb18a5dfe1f8a33003a9d898503310a6a728d13844736a95844)   |   参考文档  |
|     |  [AuthAlipayRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670ffd9d76414bc3572a7a4c5c381fd3e37bc6585f2f4e658586c8193bf232c17a9f)   |   参考文档  |
|     |  [AuthQqRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f55527daab1e867bd87be3f40b647d1fde7e0b096911071082ec3f928e8b5714f)   |   参考文档   |
|     |  [AuthWeChatRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f8488741c91f92cef8b2c57cd2db87f221fb63db4ca2e9faa0973bfe807f63763)    |   参考文档   |
|     |  [AuthTaobaoRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fce9f6c0a8ec4635c464c0f3c0200361e516a94adaac9f3b97fca9ca7510a631b)    |   参考文档   |
|     |  [AuthGoogleRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fb9da3bf2d65cf8640a2f4d90737862c34a94e983b15f7ac571de5e3e727da351)    |   参考文档   |
|     |  [AuthFacebookRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fd5775d0dc0cadd6f1b2ac44d6f1ae690cbfe14b2728aa3599ec9f123172e1927)    |   参考文档   |
|     |  [AuthDouyinRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fd38ecb3db78beafc59b7c21322d16829e84c3f54edbb8ccfc418b3fdb80a8d31)    |   参考文档   |
|     |  [AuthLinkedinRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fcbaed732c99bc54a38fe416a46ef9421c0cb967917a420f4e33cbaef2a1f65eb)    |   参考文档   |
|     | [AuthMicrosoftRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f53073ee3f609bedae3ec54dc8df943460667d7ddf09c033bc582470991a43e177518a8cc04182e4c5fa64567d3a709d0)  |  参考文档  |
|     | [AuthMiRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f1898b1e63495696345591437a6907790d69926c570ae5c9ee735ddf99e1d5ea4)  |  参考文档  |
|     | [AuthToutiaoRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fc4267fb44896d2de7aacc7415b3aa3b0c710a0af0ccfd4628737716ed27aba96)  |  参考文档  |
|     | [AuthTeambitionRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f6ed87ea43f49101e0ee4ada0e00c4e53c41901884f45b016e0a28afa12c95494ce0db9f367eb8a7449a96e10bd17b28a)  |  参考文档  |
|     | [AuthRenrenRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670fe9a13b1995849707c4ac45183a836b8a6840ddce038104a27925dc27e96d3ea4)  |  参考文档  |
|     | [AuthPinterestRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f54549df390cc804b6ca21bedf6007206d46d9e4801e91344064bef21f456a69614d32fce1bcceab1284dc0665a9867c9)  |  参考文档  |
|     | [AuthStackOverflowRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f381678181fb51f99bde8945c14cb738646e926b8c479b0c037101256bea74975709ab761d3ca3762fdeba229d324f961)  |  参考文档  |
|     |  [AuthCsdnRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f67b3907488011ecabd2af8f503485e205accc9a3cd71fc0f1355ff8ca49b5015)   |  无 |

_请知悉：经咨询CSDN官方客服得知，CSDN的授权开放平台已经下线。如果以前申请过的应用，可以继续使用，但是不再支持申请新的应用。so, 本项目中的CSDN登录只能针对少部分用户使用了_

## 后续开发计划

参考：[[开发计划] 待扩展的第三方平台](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d98934e21571d60b4b0876bfc1219983457baf4935a05c4692e189ff9fa7b7f7f264) 

另外，期待您和我一起完善这个项目！

## 贡献代码

1. fork本项目到自己的repo
2. 把fork过去的项目也就是你仓库中的项目clone到你的本地
3. 修改代码
4. commit后push到自己的库
5. 发起PR（pull request） 请求，提交到`dev`分支
6. 等待作者合并

## 致谢

在项目立项初期，也对当前开源圈的一些相同类型的项目作过调研，同时本项目也参考过这些项目，再次感谢开源圈内的朋友。

[YurunOAuthLogin](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e740458cdac3393b70d8851ad27141bff7ed3dedf82bb56909b2075242c893c8a  PHP 第三方登录授权 SDK

[阿里妈妈MUX倾力打造的矢量图标库-iconfont](http://u.720life.cn/g/e78198cbca568641bd2625675a127257b1162ff841e727fd60de3d703ac77626b794b8e65898ef9ba385b1d174027313  本文档中的图标大部分取自该平台

[mica]https://github.com/lets-mica/mica)：Spring Cloud 微服务开发核心包，支持 `web `和 `webflux`。注：JustAuth项目中的[UuidUtils]https://gitee.com/yadong.zhang/JustAuth/blob/master/src/main/java/me/zhyd/oauth/utils/UuidUtils.java就是直接使用的mica提供的高性能的uuid创建工具类源码[StringUtil.java]https://github.com/lets-mica/mica/blob/master/mica-core/src/main/java/net/dreamlu/mica/core/utils/StringUtil.java#L335

## 关于OAuth

[The OAuth 2.0 Authorization Framework](http://u.720life.cn/g/a6fc20f29c5b3b6059eab4d4320b2e4d4c7598a0c7f5b34088e1beed2c40a0335115f0c056294c5edcd767144f5b309b) 

## 关注&交流

|  公众号  |  微信(备注:加群)  |
| :------------: | :------------: |
|   |   |

 **QQ群** 

- JustAuth交流群 （230017570）：专业交流该项目

- 开源总群 （190886500）：各个开源项目的都有，也有博客建设等方面的朋友。（注意，该群需付费进入，防止发垃圾广告、垃圾推广等人士）


## 请喝咖啡

| 支付宝  | 微信  |
| :------------: | :------------: |
|   |   |



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)