fastweixin
==========
作者:peiyu 
[我的微博](http://u.720life.cn/g/c1e3906cb73241d8bdbe53b5d457b17de49e2e0da5dba22c3e9cca114e24a1d3)  
QQ:125331682 

项目主页:[https://github.com/sd4324530/fastweixin](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e4604db3c2c3b589e3c254c7663ec482db7498dbe14e42089b8c7750084ec66b)  
开源中国主页:[http://git.oschina.net/pyinjava/fastweixin](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d205caed03ea2c0bf8d99a3b929157e3638458c4cca01964bacf79090b184ec24)  
csdn主页:[https://code.csdn.net/sd4324530/fastweixin](http://u.720life.cn/g/9bca56b54153ae84ff5fbca741606b116fe9dd60dbabe1387d50bd147ab0445a0de6e6966a6f6905509ba7e07495c8f7)  

### Version
[![Build Status](https://api.travis-ci.org/sd4324530/fastweixin.png?branch=master)](https://travis-ci.org/sd4324530/fastweixin)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.github.sd4324530/fastweixin/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.github.sd4324530/fastweixin)
[![Circle CI](https://circleci.com/gh/sd4324530/fastweixin/tree/master.svg?style=svg)](https://circleci.com/gh/sd4324530/fastweixin/tree/master)

#快速搭建微信公众平台服务器 
简单封装了所有与微信服务器交互的消息:文本消息、图片消息、图文消息等等 
提供了基于`springmvc`以及基于`servlet`框架的控制器，集成了微信服务器绑定、监听所有类型消息的方法 
使用时继承，重写即可，十分方便 
v1.2.0开始支持高级接口的API，https请求基于org.apache.httpcomponents 4.3.X，json解析基于fastjson 1.1.X 
框架中提供MenuAPI、CustomAPI、QrcodeAPI、UserAPI、MediaAPI、OauthAPI用于实现所有高级接口功能，使用极其简单 
内部实现token过期自动刷新，不用再关注token细节 

v1.2.6开始支持微信消息安全模式，但由于jdk的限制，导致想使用安全模式，必须修改jdk内部的jar包 
在官方网站下载： 
[JCE无限制权限策略文件JDK7](http://u.720life.cn/g/0832d3c13dcf440b8c2ddd37014597194dfce0f4546bd12c9ba469d981d9d729007ebfc8068b2baf5cdf0064d40d4999791743570b1c7d2ca2dc6509997ab3e5bb7cdab304d5a6035f91230a45606ddb07ac85b48fb795f578e8b4ebf44ae19c)  
[JCE无限制权限策略文件JDK8](http://u.720life.cn/g/0832d3c13dcf440b8c2ddd37014597194dfce0f4546bd12c9ba469d981d9d729007ebfc8068b2baf5cdf0064d40d4999e79fd490f387972131eda157e6b402ce2d8c61c6a3e714da3ec95fcafedd448ba3a9639b48d7bde5976bf5f58a59a7d0)  

下载后解压，可以看到local_policy.jar和US_export_policy.jar以及readme.txt 
如果安装了JRE，将两个jar文件放到%JRE_HOME%\lib\security目录下覆盖原来的文件 
如果安装了JDK，将两个jar文件放到%JDK_HOME%\jre\lib\security目录下覆盖原来文件 


##基于`springmvc`项目的集成方法
```Java
@RestController
@RequestMapping("/weixin")
public class WeixinController extends WeixinControllerSupport {
        private static final Logger log = LoggerFactory.getLogger(WeixinController.class);
        private static final String TOKEN = "myToken";
        //设置TOKEN，用于绑定微信服务器
        @Override
        protected String getToken() {
            return TOKEN;
        }
        //使用安全模式时设置：APPID
        @Override
        protected String getAppId() {
            return null;
        }
        //使用安全模式时设置：密钥
        @Override
        protected String getAESKey() {
            return null;
        }
        //重写父类方法，处理对应的微信消息
        @Override
        protected BaseMsg handleTextMsg(TextReqMsg msg) {
            String content = msg.getContent();
            log.debug("用户发送到服务器的内容:{}", content);
            return new TextMsg("服务器回复用户消息!");
        }
        /*1.1版本新增，重写父类方法，加入自定义微信消息处理器
         *不是必须的，上面的方法是统一处理所有的文本消息，如果业务觉复杂，上面的会显得比较乱
         *这个机制就是为了应对这种情况，每个MessageHandle就是一个业务，只处理指定的那部分消息
         */
        @Override
        protected List  initMessageHandles() {
                List  handles = new ArrayList ();
                handles.add(new MyMessageHandle());
                return handles;
        }
        //1.1版本新增，重写父类方法，加入自定义微信事件处理器，同上
        @Override
        protected List  initEventHandles() {
                List  handles = new ArrayList ();
                handles.add(new MyEventHandle());
                return handles;
        }
}
```

##基于`servlet`项目的集成方法
```Java
public class WeixinServlet extends WeixinServletSupport {
        private static final Logger log = LoggerFactory.getLogger(WeixinController.class);
        private static final String TOKEN = "myToken";
        //设置TOKEN，用于绑定微信服务器
        @Override
        protected String getToken() {
            return TOKEN;
        }
        //使用安全模式时设置：APPID
        @Override
        protected String getAppId() {
            return null;
        }
        //使用安全模式时设置：密钥
        @Override
        protected String getAESKey() {
            return null;
        }
        //重写父类方法，处理对应的微信消息
        @Override
        protected BaseMsg handleTextMsg(TextReqMsg msg) {
            String content = msg.getContent();
            log.debug("用户发送到服务器的内容:{}", content);
            return new TextMsg("服务器回复用户消息!");
        }
        //1.1版本新增，重写父类方法，加入自定义微信消息处理器
        @Override
        protected List  initMessageHandles() {
            List  handles = new ArrayList ();
            handles.add(new MyMessageHandle());
            return handles;
        }
        //1.1版本新增，重写父类方法，加入自定义微信事件处理器
        @Override
        protected List  initEventHandles() {
            List  handles = new ArrayList ();
            handles.add(new MyEventHandle());
            return handles;
        }
}
```
 
web.xml配置

```xml
 
     weixin 
	 xxx.xxx.WeixinServlet 
 

 
     weixin 
     /weixin 
 
```


Change Log
=========
[https://github.com/sd4324530/fastweixin/wiki/Change-Log](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e4604db3c2c3b589e3c254c7663ec4825a920468c43ccbae8ee1d9d5c001183216476812f297dbd0b3154fc7b6902d4d) 

Why Use
=========
[https://github.com/sd4324530/fastweixin/wiki/Why-use](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e4604db3c2c3b589e3c254c7663ec48286068ba2a786992503e692608ea37d011bf9ab5556374489fc5135300dd82044) 

Maven 项目引入
==========
```xml
 
     com.github.sd4324530 
     fastweixin 
     1.2.10 
 
```

开源协议
==========
[Apache License](http://u.720life.cn/g/c0fe1da5278ca9f6360e901f74721f845e8fe6a63a2e42f1caa9cfc3bfda716480d0beb5865d0b08259d3122330d798e) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)