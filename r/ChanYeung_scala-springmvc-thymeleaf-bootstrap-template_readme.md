scala-springmvc-thymeleaf-bootstrap-template
============================================

A starter web application project combining Scala, Spring, Spring MVC, Thymeleaf 2.0, Spring Security and twitter bootstrap.

What is this?
=============
Spring MVC is a powerful web development framework, however it needs to integrated with bunch of other libraries to make it really powerful! However 
putting together everything needed to get things off the ground is still pretty time consuming and challenging and one of the reasons why
we are seeing one-stop frameworks like Play! become popular. 

In this sample project, I also demonstrate using Scala with Spring MVC instead of Java. Additionally, I integrate with
Spring Security and templating with Thymeleaf.

Stack
=====
* Scala 2.9.2
* Spring 3.2.0 RELEASE
* Spring MVC 3.2.0
* Spring Security 3.2.0 M1
* [Spring Security Scala Extensions](http://u.720life.cn/g/3a1ec973f83b3c356caadcf4a744764d6f0e3a7c40a13d6c7171f814341bc0e7f900f4d06f30f06d3cc7d661e015fc8f760829b4566e4cf8b18aec1833dd8df3d96d3cd3efcb3b137776aff3617e2a73)  - Scala extensions for spring
* [Jacks Jackson module](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460022cda25b96bbad0a561abbba7edaf4)  - Handle's serialization of objects to JSON. The default Jackson based mapper does not handle scala case classes.
* [Thymeleaf 2.0](http://u.720life.cn/g/93cb058e2406031f6144e42823783979ea01489469c488420b4e113ccc2745ce)  + [Layout Plugin](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462b8ef819fa43e8ddab980eb4db667f2f0a45ee6041c871529a57a50c636e62fc5240adb0d4c9fc9a47728ae79bd00b42)  - Excellent templating engine. I use 
the layout dialect  to use it for decorating as well.
* Bootstrap - Twitter's Bootstrap CSS
* Logback - for logging. Example showcases how to get Spring to use logback instead of Apache commons logging.
* Maven - For build and jetty integration


How to run
==========
Checkout project, and simply do a  mvn jetty:run and point your browser to http://localhost:8080/

Credits
=======
Based on [thymeleaf-spring-maven-archetype](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304649507cf5bf9d972497a1b7423c5d6d46a28dd29bbb346c16196e3565dde9cbfc11826f7962b05217c97e7ccea66347fc) 

Contact
=======
Twitter: [@zoheb](http://u.720life.cn/g/55c28302c8d6b2a51d2f0facda80b1a8818fb56ff82577830d21de650a19d6dc) 

Web: [zoheb.com](http://u.720life.cn/g/569eff8acbc133ff1a1c06b586cb64da08a6c832aeca99e2112e14b1075c8be5) 

[![endorse](http://api.coderwall.com/zohebsait/endorsecount.png)](http://coderwall.com/zohebsait)




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)