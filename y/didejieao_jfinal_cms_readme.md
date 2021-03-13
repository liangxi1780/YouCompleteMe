jfinal cms
------------------------

> 1. jfinal cms，采用了简洁强大的JFinal作为web框架，模板引擎用的是beetl，数据库用mysql，前端bootstrap框架。 
> 2. 后台模块包含：栏目管理，栏目公告，栏目滚动图片，文章管理，回复管理，意见反馈，我的相册，相册管理，图片管理，专辑管理，视频管理，缓存更新，友情链接，访问统计，联系人管理，模板管理，组织机构管理，用户管理，角色管理，菜单管理，参数配置，数据字典管理。
> 3. 后端模板支持：bootstrap默认样式、bootstrap黑色样式和flat-ui样式
> 4. 前端模板支持：默认内容发布、官网模板、图片模板和视频模板
> 5. jfinal cms交流群：568909653。 文档见doc/jfinal cms文档.docx

* 管理地址：http://${ip:port}/${project_name}/admin
* 测试账号: admin/admin123 或 test/123456

平台部署和配置说明
------------------------

> 1. 下载项目代码，安装jdk、maven、mysql。
> 2. 在项目目录下运行mvn install，提示BUILD SUCCESS即可。
> 3. 创建mysql用户和数据库，运行/jfinal_cms/sql下对应jfinal_cms_v4.sql。
> 4. 数据库配置文件：/jfinal_cms/src/main/resources/conf/db.properties
> 5. 如需要oauth2的，设置src/conf/oauth.properties
> 6. 运行：mvn tomcat:run
> 7. 系统默认采用单站点模式，各个站点可以在“其他管理”下“站点管理”菜单方便的切换。
> 8. 如果使用多站点，可以在“系统管理”下“多站点标示”菜单中，将“多站点标示”项目修改为true。
> 9. 多站点需要设置各个站点对应的域名，通过域名解析到不同的站点模板。


项目源码地址：
------------------------

github地址：https://github.com/jflyfox/jfinal_cms

码云地址：https://gitee.com/jflyfox/jfinal_cms

API Clinet 项目源码地址：
------------------------

github地址：https://github.com/jflyfox/jfinal_cms_api_client

码云地址：https://gitee.com/jflyfox/jfinal_cms_api_client

演示效果截图
------------------------

#### 网站CMS地址：[http://mtg.jflyfox.com/](http://u.720life.cn/g/beaa6ee9555d402dd778ed40f98b822642332c4fd33527b95471082c50840273)  ####
![网站](http://static.oschina.net/uploads/img/201601/21022316_Nk5M.gif "jfinal cms")

#### 网站官网模板：[http://website.jflyfox.com/](http://u.720life.cn/g/74f4dc8ff1b56bbf2938e9bac3014869e75c8f5f90c905adca7dc1f80e10f31a)  ####
![官网](http://static.oschina.net/uploads/img/201601/21022316_XkxY.gif "jfinal cms")

#### 博客模板模板：[http://blog.jflyfox.com/](http://u.720life.cn/g/b112cb3d4696be5fb74e9de9b3edfe9085eb80a93f6f9c1497a24970caf4250e)  ####
![官网](http://static.oschina.net/uploads/space/2016/0622/002206_Rla0_166354.jpg "jfinal cms")

#### 相册管理模板：[http://photo.jflyfox.com/](http://u.720life.cn/g/f23e779d629a587061c144bf554f8d324c84bb7a2193436b1df1addbf78f6964)  ####
![官网](http://static.oschina.net/uploads/space/2016/0306/144741_ldOJ_166354.gif "jfinal cms")

#### 视频管理模板：[http://video.jflyfox.com/](http://u.720life.cn/g/6ed27c62fad9d65c82073fba831a5fe6fe25a8561c03b834cb97597f32a359a6)  ####
![官网](http://static.oschina.net/uploads/space/2016/0306/144754_FXhR_166354.gif "jfinal cms")

#### 后台页面主题： ####
![后台管理](http://static.oschina.net/uploads/img/201601/28091447_rQtD.gif "jfinal cms")

鸣谢
------------------------

 1. [JFinal](http://u.720life.cn/g/645cc88ca89f110495efb2e933a9316ee25b04a7215b3ba4421949c540db9bde) 
 2. [beetl](http://u.720life.cn/g/414ae20d41cd3495c197ae3ba6d18135ef3589c4de367a2241a39405f3414f1a) 
 3. [oschina](http://u.720life.cn/g/645cc88ca89f110495efb2e933a9316e57f6cb6c5d22336490f27f3f346088b0) 

项目支持
------------------------

- 项目的发展，离不开大家得支持~！~

- [阿里云最新活动：双11最新活动，低至1折；还有新人礼包；请点击这里](http://u.720life.cn/g/cc176fdce68265104b8a4a80987ffe3926399b160acb0696d825845fe6926adf02ff04cf4aed2e648381c0b7fbb7489915ca2a18bd0b1b18b8c5537df66824a9f157f112ec9c61a6ba81278a136017fed54d91c8b8451c40958d4a53a35694cbc6c3574e7331371a0cee765f25ab3511) 
- 1核2G1M40G盘，86元/1年， 
- 2核4G3M40G盘，799元/3年，
- 2核8G5M40G盘，1399元/3年。

- [阿里云：ECS云服务器2折起；请点击这里](http://u.720life.cn/g/cc176fdce68265104b8a4a80987ffe393341191609ce6d7204053ccb6e2617c9a652fea74962ec906688a0977ec5a1b3dbe116ef9c7c804d9cb8375bceb122a302d2507d58df32794d42516409ea00c09d8c9443d354a4c74042967a831981091c176a5620e3545390c402fec85caea3) 
- [阿里云：ECS云服务器新人优惠券；请点击这里](http://u.720life.cn/g/60ffc7ca72c10e3c1846b3e8c088fa57c29c7e6762ea5b9e7f1afc6a47f6db431f23f4b41e06a4fbbe4d5093861e684d1a16e6335423e1cf38502e735ef8740ed9e6d133eb628a6475a1a26ff85ff985) 

- 也可以请作者喝一杯咖啡:)

![jflyfox](https://raw.githubusercontent.com/jflyfox/jfinal_cms/master/doc/pay01.jpg "Open source support")


捐赠名单
------------------------

| 名字      | 金额   |  备注  | 时间  |

| :-------: |:----: | :-----:|----- |-----|

| 阿涛 | ￥200.00 | 支付宝捐赠 | 2018-09-17 13:41|

| 阿楞 | ￥100.00  | 微信捐赠    | 2018-08-23 11:03|

| 欣喜若狂 | ￥50.00  | 支付宝捐赠    | 2018-01-12 18:10|

| 欣喜若狂 | ￥50.00  | 支付宝捐赠    | 2018-01-12 18:10|

| 奥里吉德 | ￥50.00  | 支付宝捐赠    | 2017-08-20 20:10|

| 错觉  | ￥20.00  | 微信捐赠    | 2017-07-18 18:34|

| 弱水穿云天  | ￥50.00  | 支付宝捐赠    | 2017-04-28 10:17|

| 牛牛  | ￥100.00  | 微信捐赠    | 2017-04-17 17:36|

| 2001来北京的麦田  | ￥50.00  | 微信捐赠    | 2017-03-09 16:58|

| 今生的你  | ￥20.00  | 支付宝捐赠    | 2017-02-13 12:32|

| 建强  | ￥500.00  | 支付宝捐赠    | 2017-01-19 23:04|

| 小军  | ￥10.00  | 支付宝捐赠    | 2016-11-30 22:58|

| 小军  | ￥10.00  | 支付宝捐赠    | 2016-11-19 09:34|

| 郑州誉品电子商务有限公司  | ￥300.00  | 支付宝捐赠    | 2016-09-23 14:13|

| 周克涛  | ￥10.00  | 支付宝捐赠    | 2016-08-12 19:43|

| 扬某   | ￥1.00  | 支付宝捐赠    |  2016-06-29  14:12|

| magicbug   | ￥500.00  | 支付宝捐赠    |  2016-06-20  15:14|

| 杜育轩   | ￥100.00  | 支付宝捐赠    |  2016-05-29  10:48|

| 谢协湃  | ￥20.00  | 支付宝捐赠    | 2016-05-01 22:33|

| 粪发涂墙  | ￥1.00  | 微信捐赠    | 2016-04-17 21:18|

| 胡海峰  | ￥10.00  | 微信捐赠    | 2016-04-12 15:23|

| 李守敬 | ￥10.00  | 支付宝捐赠    | 2016-03-10 17:20|

| 韩千叶  | ￥20.00  | 支付宝捐赠    | 2016-03-05 18:35|

| 神仙下凡  | ￥1.00  | 微信捐赠    | 2016-03-03 18:30|

| 张润佘  | ￥1.00  | 支付宝捐赠    | 2016-03-01 21:18|

| 李胜发  | ￥20.00  | 支付宝捐赠    | 2016-02-23 22:25|

| 贾小龙  | ￥20.00  | 微信捐赠    | 2016-02-20 15:20|

| 韩刚龙  | ￥20.00  | 支付宝捐赠    | 2016-02-10 16:17|

| 黄颖 | ￥10.00  | 支付宝捐赠    | 2016-02-08 16:25|

| 孔维源  | ￥20.00  | 支付宝捐赠    | 2016-02-07 18:40|

| 小猪  | ￥10.00  | 微信捐赠    | 2016-02-07 18:20|

| 田野  | ￥20.00  | 支付宝捐赠    | 2016-02-07 16:15|

| Allen  | ￥10.00  | 支付宝捐赠    | 2016-02-07 15:25|

| 飞龙在天  | ￥20.00  | 微信捐赠    | 2016-02-05 15:20|

| 仇国林  | ￥5.00  | 支付宝捐赠    | 2016-02-05 16:17|

| 李荣富  | ￥50.00  | 支付宝捐赠    | 2016-01-05 14:15|

| 夏舒征  | ￥1.00  | 微信捐赠    | 2015-12-03 18:30|

| 郭俊立  | ￥10.00  | 支付宝捐赠    | 2015-11-23 21:25|

| 侯善稚  | ￥5.00  | 支付宝捐赠    | 2015-11-10 12:30|

| Dave  | ￥20.00  | 微信捐赠    | 2015-09-05 15:10|

| 李具匡  | ￥1.00  | 支付宝捐赠    | 2015-08-03 23:30|

| 文子隐  | ￥20.00  | 微信捐赠    | 2015-07-23 19:20|

| 何望  | ￥10.00  | 支付宝捐赠    | 2015-07-10 17:29|

| 李新革  | ￥20.00  | 支付宝捐赠    | 2015-05-07 20:00|

| 苏某  | ￥20.00  | 支付宝捐赠    | 2015-04-01 20:18|

| 寒云  | ￥10.00  | 支付宝捐赠    | 2015-02-01 20:18|

| lucky  | ￥10.00  | 支付宝捐赠    | 2015-01-20 15:10|

| 王锋  | ￥10.00  | 支付宝捐赠    | 2015-01-10 22:00|



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)