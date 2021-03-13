# My Blog

My Blog是由Docker+SpringBoot+Mybatis+thymeleaf等技术实现的Java博客系统，博客模板是[@biezhi](https://github.com/biezhi)大神的开源项目[tale](https://github.com/otale/tale)，本来是一个docker和springboot的实战练习项目，目前已经开源，功能齐全、部署简单及完善的代码，一定会给使用者无与伦比的体验，如果觉得这个项目不错，请为它[点赞](https://github.com/ZHENFENG13/My-Blog/stargazers)支持。

- **你可以拿它作为博客模板，因为My Blog界面十分美观简洁，满足私人博客的一切要求；**
- **你也可以把它作为springboot技术的学习项目，My Blog也足够符合要求，且代码和功能完备；**
- **你还可以将其视为一个docker技术的练手教程，体验和使用红极一时的虚拟容器技术，My Blog中脚本和文档十分完善并且持续更新。**

#### tips

- **数据库文件目录为```docker-extension/mysql/schema.sql```；**
- **部署后你可以根据自己需求修改版权文案、logo图片、备案记录等信息；**
- **My Blog还有许多不完善的地方，鄙人才疏学浅，望见谅！**

演示站点：http://13blog.site

[![Build Status](https://travis-ci.org/ZHENFENG13/My-Blog.svg?branch=master)](https://travis-ci.org/ZHENFENG13/My-Blog)
![Version 3.2.0](https://img.shields.io/badge/version-3.2.0-yellow.svg)
[![License](https://img.shields.io/badge/license-apache-blue.svg)](https://github.com/ZHENFENG13/My-Blog/blob/master/LICENSE)

#### 宣传

十三近期于CSDN上传了一份自己制作的达人课课程,感兴趣的朋友可以看一下：

* [x] [GitChat达人课-SSM搭建精美实用的管理系统]http://u.720life.cn/g/b895c0c72c55fdd6101b6abc729fe43d316e9a4365d8c635aacbb8df24430cbf50198e5a77960730b0b62f005e2095b23ad9eb78080206041c40548c546deeee) 

![gitchat](https://raw.githubusercontent.com/ZHENFENG13/resource/master/images/2018-07-19/gitchat.png)

#### 相关博客文章

* [x] [Docker+SpringBoot+Mybatis+thymeleaf的Java博客系统开源啦]http://u.720life.cn/g/474b3c3120ba1ab1f6f09785ba99e4569a8813c67357856346b198b55046b74380e41b3bfa34d6f70b9944fe8898b875836288a2ca957e7a4704920e64cb8dbe) 
* [x] [My-Blog搭建过程：如何让一个网站从零到可以上线访问]http://u.720life.cn/g/474b3c3120ba1ab1f6f09785ba99e4569a8813c67357856346b198b55046b743f672c2180db1c612f0f8baf111e8707eb3be5a607099c7f4c996a744610965b9) 
* [x] [利用Dockerfile构建mysql镜像并实现数据的初始化及权限设置]http://u.720life.cn/g/474b3c3120ba1ab1f6f09785ba99e4569a8813c67357856346b198b55046b7437d87ff335d6d194bea8fb54ff4907f6d5ddfe8862cdf7ffc171fc08422a57973) 
* [x] [Java开源博客My-Blog之docker容器组件化修改]http://u.720life.cn/g/474b3c3120ba1ab1f6f09785ba99e4569a8813c67357856346b198b55046b743d209eff172eb219993821bb3adbc9ffe76ad06659e36bb96c6fa65296481e1f3) 
* [x] [Java开源博客My-Blog之mysql容器重复初始化的严重bug修复过程]http://u.720life.cn/g/474b3c3120ba1ab1f6f09785ba99e4569a8813c67357856346b198b55046b74391debbfd9a0dde4f24d4fcf4db0d97a87f4e053e2314b5feb0ef92816bcb20c4) 
* [x] [Springboot与Thymeleaf模板引擎整合基础教程]http://u.720life.cn/g/474b3c3120ba1ab1f6f09785ba99e4569a8813c67357856346b198b55046b74377583915b5b26c0fb527340bf8793fddfc9c2a45c533c0dda6811a9622b39dcd) 
* [x] [thymeleaf模板引擎调用java类中的方法]http://u.720life.cn/g/474b3c3120ba1ab1f6f09785ba99e4569a8813c67357856346b198b55046b743fd00d5a8c1c2eabc2a8ee4d7d4a07d1255f587578240c33c009059dd6f5ec0d3) 

#### 捐赠

**网站的持续运行需要各项基础设施的搭建，而服务期的续费和维护及各种配套服务的购买也需要一定的费用，希望朋友们给予一点支持，谢谢！**

**支付宝：** **微信支付：** 

# Quick Start

* [x] [1.如何部署My Blog]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad4f89252a73784bf26e7b64d78f3b36078210ef9aea3f609e3fa18367c04948a1490ff95e437f69fd89a2081f5cf12f7f7b0a376da2151f94bd0062e7f6cf363c3) 
 - [1.0 基础环境搭建]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad47ca16c88e5b22295d90e0a58a59d07d17156cae39e0491b76bf8e8fe6dd20cfc6943244a5fa99ebf25f6c535df8bc22a991e476512a2e01e56b18c9168590ad7) 
 - [1.1 安装Docker环境](https://github.com/ZHENFENG13/My-Blog/wiki/1.1-安装Docker环境
 - [1.2 安装docker-compose]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad4041928a89e562d805db9bec9638dc0921164427b7afecd8b253c028ccd49b8a45dc61cd0194e264c32783dc6fa72b257) 
* [x] [2.通过共享镜像直接部署My Blog]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad44f22fcd592aa27b03793b7b01e43b53d764f0567330b55f775f675b6ed65585b951b9fa1e486ab14af3cc13857d04c9d5033c62db556ef04044891814052425df132173618efdd4cadc7925c3421cba8820ecb69e1ddc37f051be60638ec2d1adaa47e27499d702dae08f146f5bca71b) 
* [x] [3.1 非docker环境运行My Blog]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad428256f484dd383e85b733f4e7e61f81ac6312cde06fcf6c00353717b5f270272b0ff0903a236d20a96c3d08971e5d19c5c9b69f5397d567521ef140db0c7e17835128f90b5bb15764c8c939d8c1c02ea) 
* [x] [3.2 将My Blog部署到tomcat(非docker环境)]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad47fc5664cab0c4887a4fa555fff64322d4a299d6e5f76b2fc39dbee6bf74ff5b9a1b228f040d4188dd491d773f5eecabf216016b7e0e976f6c2f427d53d21383ab815033d0b9a330465661d133a5e01b3b3e32d66efd3cd25a987f518da05b67ffd9d19f2ea3d929b195219e3926b0fe8) 
* [x] [4.开发环境运行代码]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad4975cf573faaa7996e0058e18c3eeb345dd9a5f3d25e153e5b1bfaee01fc38ea1b29dc67ea8237efd4f06614ab000a05bf7af188226c719c5dd6dd43b55969ed2ba37a4f4363d8aa263fe58cb55880f1d1972634a489595e5a1caa19d8d2d6bc8) 
* [x] [5.博客上线及备案相关流程]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad471a7eab7739a2f4e4756688d3e3493b5f0d1268081baae81b5f59e8da3ec3b631f45374f4a94148fea7291c1a93fb131e12e0179f6d2ced3221cf3c4887ba401bb3f2478e76c528b32954b75ca4a7110) 

[**常见问题**]http://u.720life.cn/g/4fef179f29be438184ded056121a041d42d9c501f8c2235c46356066d7ba9ad47fe49dd2c82b9a6f89cab23eb3cef2341bdc4a836653a106544c5b131f8889ef3c98f4115988712bc27a3a724fb63563) 

# Preview

**博客展示页1：**
![My Blog](https://raw.githubusercontent.com/ZHENFENG13/resource/master/images/2018-06-13/my-blog-2.gif)
**博客展示页2：**
![My Blog](https://raw.githubusercontent.com/ZHENFENG13/resource/master/images/2018-06-13/my-blog-1.gif)
**登录页：**
![登录页](http://images2015.cnblogs.com/blog/859549/201705/859549-20170511122916004-738411708.png)
**My Blog后台：**
![My Blog](https://raw.githubusercontent.com/ZHENFENG13/resource/master/images/2018-06-13/My-Blog-admin-1.gif)
**My Blog后台：**
![My Blog](https://raw.githubusercontent.com/ZHENFENG13/resource/master/images/2018-06-13/My-Blog-admin-2.gif)

# Log

2017-03-27 添加docker整合 
2017-03-28 schema.sql修改 
2017-03-28 install步骤，数据库地址配置时:mysql地址写为mysql容器的名字即可,即mysql:3306 
2017-03-29 修复添加评论时空指针异常的bug 
2017-03-30 添加预览功能,限制文章浏览，如果为草稿状态前端即使通过正确的url也不能浏览 
2017-03-31 文章浏览数不变的bug,后期浏览数及评论这些参数放到缓存里去 
2017-04-01 添加druid数据源 
2017-04-02 重写mysql的Dockerfile文件，修改install过程 
2017-04-15 bug修复,footer样式调整 
2017-04-17 logo文件修改,附件上传功能 
2017-04-18 评论功能及页面修改 
2017-04-20 域名及网站的公网备案 
2017-04-25 docker-compose实现多容器部署 
2017-05-09 删除原install过程,改为脚本自动部署及初始化 
2017-05-10 docker容器时区不同步问题修复,文件整理 
2017-05-11 文件整理,排版和文案修改 
2017-05-13 正式上线啦 
2017-05-15 部署文档 
2017-05-21 My-Blog上线过程记录 
2017-06-30 目录调整:docker组件化 
2017-07-20 问题修复:docker-compose重启时mysql容器中数据被删除并初始化的问题 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)