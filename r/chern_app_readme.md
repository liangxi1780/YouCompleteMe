## FossApp快速开发平台
===================================
FossApp快速开发平台，是一个通用的移动端快速开发系统，是基于vue实现的app、微信开发框架，包括基础技术架构、组件、插件、模块规范、常用业务模块等部分。
在项目启动时，可以在此平台上进行技术选型剪裁、配置，快速生成项目，在此基础上只需补充业务模块，即可完成具体业务。

## FossApp的特点
-----------------------------------
1. 强大的基础架构，基于vue，组件化开发思想。
1. 完善的使用指南，代码规范，插件、模块接口规范，二次开发简单迅速。
1. 基于restful接口规范的后端mock示例项目，包含常用业务模块接口，方便前端人员独立完成开发，易于接入现有业务平台。
1. 可在NPM中一键生成项目，增加项目插件、常用业务模块。
1. 完善的GUI项目配置工具，只需在页面配置即可生成、配置项目组件、业务模块。
1. UI组件，布局整洁精致，文档齐全。
1. 适配各种轻应用框架，支持移动端iOS 7.1、Android 4.0以上手机系统，方便接入微信、企业微信、钉钉、金蝶K3WISE、用友等WebAPP平台。
1. Android项目使用基于 Chromium/Blink 的Crosswalk作为应用运行环境.

## FossApp的技术堆栈
-----------------------------------
1. 前端MVVM框架：
    1. Vue 1.0.x
1. UI框架：
    1. [Vux](http://u.720life.cn/g/453bc3b594cc76eeb90f355bd2bbbfb2517dac366bf0fe5120b9684bc5285caf9812e7855772d8cd422cdfef0110df5b)  基于Vue和WeUI的组件库
1. Cordova
   1. [Plugin](http://u.720life.cn/g/2108b3aba4f31533007e8fbe3873c14e7332c059680ef1582fad103077077d05c8af8b8d2bd96092b8ad7ae14a0748992f99dea4d46b037bc4eb612041e8bb8c71caf8f50e306824fc212d706cacfb50) 
   1. Sqlite
   1. [Hotcodepush](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046087fc6e7b9e9c9ef2ef3503a3c4616f6e93c9c734e93d47fdd76f87c28e1d000) 
   1. PUSH：极光推送（个推、小米）
   1. 友盟统计
   1. Crosswalk
1. Mock
1. Vue plugins:
    1. [vue-validator](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046889865a0cd07baca8b87b3effe929a4d64204ad9e0f7bdec1f3c07966240dc9f)  [2.1.7](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046591557195c5b2d4e14aa35b97ea315d50c2720a6db76c5325cf3f0d45a7f86d3af2e99df1da825dbf10fe85ba00aa3c8) 
    1. [vue-router](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304606fb5995514a592d0358d69de03eba11587624a2443f25b40b14ec7210b1c182)   [0.7.x](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304606fb5995514a592d0358d69de03eba110f8b0478d9a9dee5932d1e0f147c56478593ace7535a40af40b78609d1040f90) 
    1. [vue-resource 1.0.x](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046b73833f73c9c0ed61fe234c6ba1fb536542322b688e5a6316c90006474f1c628) 
    1. [vuex 0.8.x](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468906e125044176e26706de8c385ce3679c1a007a63b4bbfdc056d44b23c96a09a74b7eaff746f0049914df4c3a24bb31) 
    1. [vue-cookie](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cf5367c3e23b8e3d51a389b6a998c787fbcef539ad570f6d17ab0c71bab5dbd4) 
    1. [vue-touch](http://u.720life.cn/g/54145d0471d91890860f7f8463c030462ef183b4875fdd2dd130b1e71069b5d16635d23324b99dfb3a1cb0d76df61685) 
    1. i18n
    1. [List of User Contributed Tools](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468352cb05207a56c1a43a37b28903a67f7f2cd63a1f14dd92815bd1cfbb067c49922267535e8738f74805a80b2ba4e049) 
1. WXSDK
1. Webpack
1. LESS、SASS
1. [ES6](http://u.720life.cn/g/c7e32d8c72c7a7f0f5b5c90906d584013776b8c9d4fe523c32a32c029033d867) 
1. [ESLint](http://u.720life.cn/g/41c8ab57bcee77c9fe124c28b5f771b83408cc6c9f1825b551e1d55e311df02043d7691193d2b0ccd4c6b3d22b2aad9e) 
1. 开发工具： 
    1. [vue-devtools](http://u.720life.cn/g/011bcbff60d4bdcdf5b89348f1b4fec4ea1629e5a5711d79823204fb51bba15e20b65ccdd79366564143cbbc60fa8c54e55307f2c25897c995ab2411cf28d2267a66c20484917d444b94e0600f48ea3c)  Chrome devtools
    1. [vue-cli](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046521cadb82ab6b46bcadb5dbc00f05b7e)  脚手架
    1. [WebStorm 高亮插件](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046795c4385bcc12c5ccd166c7e754ed7830411f6009d2b549c7bae2a0e18208955) 
    1. [VS Code 高亮插件](http://u.720life.cn/g/61df49c8dfe6497e1d755535043d5993f084ad4bb2562a93ce813aeeb8e143e3fb328047d4cf3a7586778bccf703cdf52e6a7f398c2c392ad0cc800105ea9b14) 
    

## FossApp的模块编码规范
-----------------------------------
参考：http://blog.csdn.net/lihongxun945/article/details/49031383

## 移动端离线文档

1. 安卓 
    1. [ES6 入门](docs/assets/apk/ES6Tutorial.apk)
    1. [Vuejs1 文档](docs/assets/apk/vuejs1docs.apk)


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)