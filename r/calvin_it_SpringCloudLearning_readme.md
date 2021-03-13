
>转载请标明出处： 
> http://blog.csdn.net/forezp/article/details/70148833
> 本文出自[方志朋的博客](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a47bc9dc9d262d07014259a514b9889f61) 

错过了这一篇，你可能再也学不会 Spring Cloud 了！Spring Boot做为下一代 web 框架，Spring Cloud 作为最新最火的微服务的翘楚，你还有什么理由拒绝。赶快上船吧，老船长带你飞。终章不是最后一篇，它是一个汇总，未来还会写很多篇。

案例全部采用Spring Boot 1.5.x ,Spring Cloud版本为Dalston.RELEASE

我为什么这些文章？一是巩固自己的知识，二是希望有更加开放和与人分享的心态，三是接受各位大神的批评指教，有任何问题可以联系我: miles02@163.com .
码农下载：[https://git.oschina.net/forezp/SpringCloudLearning](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36b8dc900fdbf0c07a49f8065bad0694056cf842a75cde8bfdbfe7a48cea8c14dfdcc0411ecf726fe0103061ec431c8b81e) 
github下载：[https://github.com/forezp/SpringCloudLearning]https://github.com/forezp/SpringCloudLearning),记得star哦！

### 欢迎购买我的书《深入理解Spring Cloud与微服务构建》

![1.jpg](https://upload-images.jianshu.io/upload_images/2279594-3d9ee1555f555040.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/300)

[京东购买](http://u.720life.cn/g/7b2b4b420a3d295955078cf4db9efbc3b3c563910a7619522ef6491dd7218b90d575e35417472dfa91bcddc87026f60e)   [当当购买](http://u.720life.cn/g/c4870a3df4dbf9b3f895a193ff995ebebd439742d149f1424b0a5b01d88dd1f18ed1a23f3ce412b7265d475263c79d80)  [亚马逊购买](http://u.720life.cn/g/cb03c2a1672c12ec833030607d89ad067466e292b2df49a584e8e01adac7f08c7c190a4693e471cb9eb4423ce2bc25de93481daa81cd104407b5777b9d1858b869e7deeaf01fa39b5adc556b2f3a49be8afedcbd5d75e523fc8aca5cb531b04eacb45840d270b0f0e716686a15366bac) 

#### CSDN专栏汇总：[史上最简单的 SpringCloud 教程](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2612ef83f7306593d38d3ef8310d2848720e4949831b165b603f9610e8feac4e266) 

### 《史上最简单的 SpringCloud 教程》系列：

* [史上最简单的 SpringCloud 教程 | 第一篇: 服务的注册与发现（Eureka）](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261a24e0fbecdb420200284ca2b3ef6516328e5be395a370e2e4a448227f39a64ed) 
* [史上最简单的SpringCloud教程 | 第二篇: 服务消费者（rest+ribbon）](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2619b33a2c763410d47f481484ea73f9144a1b9df593bb087c30986ca37610165a0) 
* [史上最简单的SpringCloud教程 | 第三篇: 服务消费者（Feign）](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261acceefa4028d5bd4f2f60e13e8be257f823a5ed91ddd508965a89f45f43c4cec) 
* [史上最简单的SpringCloud教程 | 第四篇:断路器（Hystrix）](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2613cc73e70b4f97a0dc7272123f9ba6e62eb74a2be393996885104aa7159f4448a) 
* [ 史上最简单的SpringCloud教程 | 第五篇: 路由网关(zuul)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2613cc73e70b4f97a0dc7272123f9ba6e629dd1cfc3f7d96f913e59018b62376fb9) 
* [史上最简单的SpringCloud教程 | 第六篇: 分布式配置中心(Spring Cloud Config)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2611ebeedc5c78e35729372a7bc99310cf4414105af953aaaea3187bea6e0834c8f) 
* [史上最简单的SpringCloud教程 | 第七篇: 高可用的分布式配置中心(Spring Cloud Config)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2611ebeedc5c78e35729372a7bc99310cf49fc16e898b67ce62865e7738ed5786e4) 
* [史上最简单的SpringCloud教程 | 第八篇: 消息总线(Spring Cloud Bus)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2612ef83f7306593d38d3ef8310d2848720116767a9cdaafd105bfb1ebfd92a5c63) 
* [史上最简单的SpringCloud教程 | 第九篇: 服务链路追踪(Spring Cloud Sleuth)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261b585c906054dc96506c82047aad9d1f4c44347fd03046fdae9ccb0edb3efa5bd) 
* [史上最简单的SpringCloud教程 | 第十篇: 高可用的服务注册中心](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261f407fe1558a65147a0ba2ce9c8c83e226d4aa1a2161baada9940f12ed1149cf5) 
* [史上最简单的SpringCloud教程 | 第十一篇:docker部署spring cloud项目](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d26144db679ba0236f285bbd2a0852ef707e035a1be9027c9f0398c5ca8d61a3f1e5) 
* [史上最简单的SpringCloud教程 | 第十二篇: 断路器监控(Hystrix Dashboard)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d26102841c8cc46c97890d442ec1d3c475e1f6d2b14b0cc0c8e7f4d896d86e28dcc9) 
* [史上最简单的SpringCloud教程 | 第十三篇: 断路器聚合监控(Hystrix Turbine)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261eefdda4938d93a27eee369e4fc6493d2c6eb8e93dc13936552d11ff22d7210da) 
* [ 史上最简单的 SpringCloud 教程 | 第十四篇: 服务注册(consul)](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261623eb66740c74458826a3046daeca1e92730edaf278ec1bd3354680d2fc0c188) 
*  未完。。。
*  还有很多篇。。。
 
### 进阶篇

* [ Spring Cloud Sleuth超详细实战](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d26121a4941ae1f46f0d39189222a75b6949716d7d9bc45c50b4cb7bc0c7290c2faf) 

### 源码篇：

* [深入理解Feign之源码解析](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d26105f4e300c35af8ae4c2640a18bd35d1ed2ab3f885bd59a79de53057b2d7fa0b5) 
* [深入理解Eureka之源码解析](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261ba43bbac9182718d5d06be8eb580992dd5c60b43bbdca87d1c5891a50d28f6d9) 
* [深入理解Ribbon之源码解析](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261b38fcf620c723fc40c596c3fb4fa737eeaf7ad19baf2776f188fbfc3b0202410) 
*  [ 深入理解Hystrix之文档翻译](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261b6b6ce62c18ff520494933ce15438acc2968acd7c2a4cca127bf725dd01490dd) 
* [深入理解Zuul之源码解析](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2611aa0ff62f55753b2351332401e12bdeb2bb88d9c213080fc771b90aa8427d9d1) 

### 番外篇：

* [如何使用MongoDB+Springboot实现分布式ID?](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d261acf16319c8bfa5bed4741f732391f2c2274af37e4f120b019bedb048138834a0) 
* [ 如何在springcloud分布式系统中实现分布式锁？](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2617f4a8ca257d94359b60a7d43790ac33beb7f2e355808f708d471db99a4b780c8) 
* [ 如何用Redlock实现分布式锁](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d26168912d7ae100de5d4d206e12c3f044c25bd4a347654aa4838c484523a66306d6) 
* [ 如何在IDEA启动多个Spring Boot工程实例](http://u.720life.cn/g/5997fd1f539dfbe7c9c67736234755a4a6289c8202d9ee07795bb8bf69a7d2613305ff67d4ec0db50c05d34e1f43ebac83fc3c135a3a9484c6ee1a2a58c5e77d) 


### 怎么支持我？

* 这个系列会持续更新，敬请关注！

* 关注我的公众号,精彩内容不能错过！

![forezp.jpg](http://upload-images.jianshu.io/upload_images/2279594-0805748d92bba033.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/200)





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)