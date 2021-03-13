kisso  =  cookie sso

基于 Cookie 的 SSO 中间件，欢迎大家使用 kisso !! 

http://www.oschina.net/p/kisso

﻿sso
===

kisso cookie sso framework


Usage
====================

[kisso 依赖 jars](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d626733fb1ef81dd3de8db53ee7f8d946f08b3e08c62afe4014cb365717b44dcc) 

[kisso 验证码字体](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d626733fb1ef81dd3de8db53ee7f8d946e5b3143fc0f65614c157ac10883ea812caaef327e43f4114329464a31d926110dcdf0cb35a64650620cedd8eca4e135e) 

[kisso_JFnal 演示 demo](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d626733fb1ef81dd3de8db53ee7f8d946560e622961fc9dfd70a15db73525b4cf) 

[kisso_SpringMvc 演示 demo](http://u.720life.cn/g/5c954f4cd4204fb6c09a7e58aa70844d626733fb1ef81dd3de8db53ee7f8d9468864a06bc6489160f87c5f46ca33f568) 

跨域演示demo待定！！！！

（1）sso 登录状态
--------------------------------------------

 #登录

 

 #登录成功

 



（2）跨域登录
--------------------------------------------

![GitHub](https://raw.githubusercontent.com/leqwang/kisso/master/images/cl.jpg "Kisso,crossdomain login")

hosts:
--------------------------------------------
127.0.0.1 sso.test.com
127.0.0.1 my.web.com

--------------------------------------------

访问 my.web.com:8090/index.html  如果未登录会重定向至sso域登录页面
![GitHub](https://raw.githubusercontent.com/leqwang/kisso/master/images/nologin.jpg "Kisso,crossdomain login")

登录成功 my.web.com 如图
![GitHub](https://raw.githubusercontent.com/leqwang/kisso/master/images/login.jpg "Kisso,crossdomain login")


Supports
====================
1、支持单点登录

2、支持登录Cookie缓存

3、支持防止 XSS攻击, SQL注入，脚本注入

4、支持Base64 / MD5 / AES / RSA 算法

5、支持浏览器客户端校验

6、支持Cookie参数配置及扩展

7、支持跨域登录，模拟登录

Futures
====================
1、实现完整 sso 工程实例


开源赞助我(支付宝)
====================
![GitHub](https://raw.githubusercontent.com/leqwang/kisso/master/images/donate.png "开源赞助我(支付宝)")

copyright
====================
Apache License, Version 2.0


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)