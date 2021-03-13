 
	   
 
 
	 Login, so easy. 
 
 
	 
		  
	 
	 
		  
	 
	 
		  
	 
 

 
     
         
             
                     
                     
                     
                     
                     
                     
                     
                     
                     
                     
                     
                     
             
         
         
             
                  Gitee  
                  Github  
                  Weibo  
                  钉钉  
                  百度  
                  CSDN  
                  Coding  
                  腾讯云  
                  OSChina  
                  支付宝  
                  QQ  
                  微信  
             
         
     
 

-------------------------------------------------------------------------------



JustAuth，如你所见，它仅仅是一个**第三方授权登录**的**工具类库**，它可以让我们脱离繁琐的第三方登录SDK，让登录变得**So easy!**

项目开源地址：[gitee](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9894d7f9ce3e60d4881ec4b106227d88476)  | [github](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046066dd74459bee98bfd188515b03f16770c296c2a74d25b559d1d9874813de6f8) 

## 快速开始
- 引入依赖
```xml
 
     me.zhyd.oauth 
     JustAuth 
     1.0.1 
 
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
// 授权登录后会返回一个code，用这个code进行登录
authRequest.login("code");
```

具体的例子可以参考：

- [实现Gitee授权登录](http://u.720life.cn/g/5d81a8ca0ea302f3ba1dc8d3b9aead0f8e6c7cc866eb89b5f0e55201f8c0f704) 
- [实现Github授权登录](http://u.720life.cn/g/0da1eacdf39532cff4a861ca237e150c75f8555b84cea17342cdf7e96795b642) 

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
|     |  [AuthCsdnRequest](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d9895bc80d6dabcc37cc4c7b319724e866a9233daa93b433be27917dd69b095cc11b85684adfa5580dddcd9e60f9218e670f67b3907488011ecabd2af8f503485e205accc9a3cd71fc0f1355ff8ca49b5015)   |  待续 |
|     |  AuthQqRequest  |   参考文档   |
|     |  AuthWechatRequest  |  待续  |

## 后续开发计划

参考：[[开发计划] 待扩展的第三方平台](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e94d1794846e62207de06f8cd5ec9d98934e21571d60b4b0876bfc1219983457baf4935a05c4692e189ff9fa7b7f7f264) 

另外，期待您和我一起完善这个项目！

## 致谢

在项目立项初期，也对当前开源圈的一些相同类型的项目作过调研，同时本项目也参考过这些项目，再次感谢开源圈内的朋友。

[YurunOAuthLogin](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e740458cdac3393b70d8851ad27141bff7ed3dedf82bb56909b2075242c893c8a  PHP 第三方登录授权 SDK


## 参考图例

#### 授权gitee

![Gitee授权登录](https://images.gitee.com/uploads/images/2019/0221/140015_4c09610e_784199.png "Gitee授权登录")

#### 授权github

![Github授权登录](https://images.gitee.com/uploads/images/2019/0221/140032_58f7dfb5_784199.png "Github授权登录")

#### 授权weibo

![微博授权登录](https://images.gitee.com/uploads/images/2019/0222/191210_67d5597c_784199.png "微博授权登录")

#### 授权钉钉

![钉钉授权登录](https://images.gitee.com/uploads/images/2019/0221/140540_8da8d959_784199.jpeg "钉钉授权登录")

#### 授权百度

![百度授权登录](https://images.gitee.com/uploads/images/2019/0221/140607_ebf1dcb6_784199.png "百度授权登录")

#### 授权coding

![Coding授权登录](https://images.gitee.com/uploads/images/2019/0224/192106_fd53b3d7_784199.png "Coding授权登录")

#### 授权腾讯云开发者平台

![腾讯云开发者平台授权登录](https://images.gitee.com/uploads/images/2019/0224/192128_db9e203b_784199.png "腾讯云开发者平台授权登录")

#### 授权oschina

![授权oschina登录](https://images.gitee.com/uploads/images/2019/0322/230652_05b4fd8a_784199.png "授权oschina")

#### 授权支付宝

![授权支付宝登录](https://images.gitee.com/uploads/images/2019/0327/183654_3d4b94eb_784199.png "授权支付宝登录")

#### 授权csdn

待续

#### 授权qq

待续

#### 授权微信

待续

## 请喝咖啡

| 支付宝  | 微信  | 
| :------------: | :------------: | 
|   |   |




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)