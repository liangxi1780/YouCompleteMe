# My Blog

My Blog是由Docker+SpringBoot+Mybatis+thymeleaf等技术实现的Java博客系统，博客模板是[@biezhi]https://github.com/biezhi)大神的开源项目[tale]https://github.com/otale/tale)，本来是一个docker和springboot的实战练习项目，目前已经开源，功能齐全、部署简单及完善的代码，一定会给使用者无与伦比的体验，如果觉得这个项目不错，请为它[点赞]https://github.com/ZHENFENG13/My-Blog/stargazers)支持。

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

* [x] [GitChat达人课-SSM搭建精美实用的管理系统](http://u.720life.cn/g/9e13c3bc7ca56898c79d8e9530ab3ebbad3b3d1fde243304260743ee498604762a4a8a3aa10c2533c5e823d7c91aed838b9fc67552f47c237e61232be5c65d25) 

![gitchat](https://raw.githubusercontent.com/ZHENFENG13/resource/master/images/2018-07-19/gitchat.png)

#### 相关博客文章

* [x] [Docker+SpringBoot+Mybatis+thymeleaf的Java博客系统开源啦](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f62bb507a8fa8011d6cd99fe609acbfaaf53ed2301890ce016db1d2f441fceda425f9089df90820bf64fbb83e2f0a362c) 
* [x] [My-Blog搭建过程：如何让一个网站从零到可以上线访问](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f62bb507a8fa8011d6cd99fe609acbfaa28502014bc7a06ed2145e02573493c44078e9d65da77c8ba62c89ede05b2e959) 
* [x] [利用Dockerfile构建mysql镜像并实现数据的初始化及权限设置](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f62bb507a8fa8011d6cd99fe609acbfaaef6aeee4adddae10a8c43e8bfdeff4eac474abd28ff84fcca6f41b3b382b472c) 
* [x] [Java开源博客My-Blog之docker容器组件化修改](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f62bb507a8fa8011d6cd99fe609acbfaa9454ab1001aab5c76d7d4d5690eee9c04aa581f349e6f2b2f4ee9fc9fe779829) 
* [x] [Java开源博客My-Blog之mysql容器重复初始化的严重bug修复过程](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f62bb507a8fa8011d6cd99fe609acbfaa94eae46a2835b995d96bc2be27c7937019f7f7c4cdb8a0d26a875e2deb8b532e) 
* [x] [Springboot与Thymeleaf模板引擎整合基础教程](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f62bb507a8fa8011d6cd99fe609acbfaaa0c937d7319cf659a0d53423e6d223f2a08975ea5e6393c1f5c5553bbdf9c463) 
* [x] [thymeleaf模板引擎调用java类中的方法](http://u.720life.cn/g/94c1d8931f8bedcd3eeaf8cdeb6a662f62bb507a8fa8011d6cd99fe609acbfaa47124bdad01ace990ce281750932e1bd8f5c418e6241233495510503b47392c6) 

#### 捐赠

**网站的持续运行需要各项基础设施的搭建，而服务期的续费和维护及各种配套服务的购买也需要一定的费用，希望朋友们给予一点支持，谢谢！**

**支付宝：** **微信支付：** 

# Quick Start

* [x] [1.如何部署My Blog](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece9af9087d5505616219e304961d3f5b094750f6785d3336a5135c02200430506c089ce65eb11751c3591ce080d804dea080083de048f4cf4ea1b030e73af317ef9) 
 - [1.0 基础环境搭建](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece9532fea8abdf94d039b392ce6e76a340ced078fd89b2edb09713f8ef8c3925099450f4a077f16a04e5498c9e7196b737539df4ca7ffc362feb0220e483294560b) 
 - [1.1 安装Docker环境]https://github.com/ZHENFENG13/My-Blog/wiki/1.1-安装Docker环境
 - [1.2 安装docker-compose](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece93dfa78994bb0c7ebffa9c876f6b243f910100bc8c21c14197578309697281670bcce951f33964d079b8a3ee1e282e4e0) 
* [x] [2.通过共享镜像直接部署My Blog](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece98a0320e1805a5dccf2c60bece215438077ae4ded4b7b3f7220881da16d026c1240d5909bfc642f928430df970cdc2d63daa02ea45390094a6a889152d9c443f45225e77ac8a4390993bcc46101d326912b3fc924911fae7b2ebaff8fb0fb24db48c823509e4ef30756c1662540d1dde2) 
* [x] [3.1 非docker环境运行My Blog](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece9bd643b0b1bb5cea12331d24c515c43f57e060627327bb54e798af9bcc171fe8f5315055d9d62e5f6557dfd1eacbd6788287b1a8120a792c6fa05bb6be5a2e35c2f91a110fcf4b96aaf32f5468f656f77) 
* [x] [3.2 将My Blog部署到tomcat(非docker环境)](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece9865051157c76ae054b376a62c86fd7c177a350b149f301a57d904ebf394fbf621b87951d1a119e740c7cac2e9d5d4003b118fc351b3b5bf8b14db7d991db5713f7d3029c421287d32146e917d865ff361db48378e060b62ab52104bf3cbd1b40ca0d8c8e15a1248a1d88aa84e5956025) 
* [x] [4.开发环境运行代码](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece930ae6ed5e6ffb3e2e87da420f532f6f1fabc422861f20ab9f38bca63969252bc9c2356e11700a5072366cbfd5e554cad563a4eccbcba25bf61f8b3fdca481c28a68f085a6e11cef69f23bf7d3c224e1930433eb5ab766004087de6e9717d758d) 
* [x] [5.博客上线及备案相关流程](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece9eab3c1336f5b77bbf2d2544e28afabadabc46898d8659702c02c6bb5d330507d27687b76c661f745f95629e97e1392abc9cdaa46bf8ffbb52fd0e99dda45ab140aef1f948fb11e3b0ca229a4cbb48689) 

[**常见问题**](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a23cd1924905cb0a17df0c25766eece99e91277c98c3f01f7e8b27bf3a217acec07d437d74d00c1d0e3d1f3295c18045f58210ef46350d81611316500e0aa3b1) 

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