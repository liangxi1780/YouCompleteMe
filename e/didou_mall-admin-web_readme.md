# mall-admin-web

## 说明

> 基于Vue+Element的电商后台管理系统，完整实现了整个流程。

> 该项目为前后端分离项目，搭建步骤具体参考后端项目[传送门]https://github.com/macrozheng/mall)。

> 如果该项目对您有帮助，您可以点右上角 "Star" 支持一下，谢谢！

> 该项目已由`CODING`特别赞助，支持的可以点下赞助商链接，谢谢！

> 项目交流QQ群：[553018255]http://qm.qq.com/cgi-bin/qm/qr?k=M5Edq2TiJL_ShcOEeYjwcmdGmq4zZrd_)、[959351312满)]http://qm.qq.com/cgi-bin/qm/qr?k=V6xu5c12j9qhnMUNdDRzakNxRKzOxibQ)。

> 码云项目地址：[https://gitee.com/macrozheng/mall-admin-web](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6ed413e6dac79d5ae837bc13284a4aebcc5ad11e3998960272764af599378e5ad5) 

## 前言

`mall`项目后台管理系统的前端项目
[传送门]https://github.com/macrozheng/mall)。

## 特别赞助商

 
 
   
  
 

## 项目介绍

`mall-admin-web`是一个电商后台管理系统的前端项目，基于Vue+Element实现。
主要包括商品管理、订单管理、会员管理、促销管理、运营管理、内容管理、统计报表、财务管理、权限管理、设置等功能。

### 项目演示

项目在线演示地址：[http://39.98.190.128/index.html](http://u.720life.cn/g/602cbbd93ce6eec9ce45e915b1e17775e2e2e89d6d98a1032066f789ffc07370)   

![https://github.com/macrozheng/mall/blob/master/document/resource/mall-admin.gif](https://github.com/macrozheng/mall/blob/master/document/resource/mall-admin.gif)

### 技术选型

技术 | 说明 | 官网
----|----|----
Vue | 前端框架 | [https://vuejs.org/](http://u.720life.cn/g/1c3db3fec6433a3fb191bb48af91f3bb055304712f0641658c814ca15fec0089) 
Vue-router | 路由框架 | [https://router.vuejs.org/](http://u.720life.cn/g/7bedfe02707a57b283aa65bf169b40685a2bcc51af184101de4b71f45db846fa) 
Vuex | 全局状态管理框架 | [https://vuex.vuejs.org/](http://u.720life.cn/g/acea3f53396a46112876052cae0a3648a88a7ed218d2be0ffa10fc982c11ad04) 
Element | 前端UI框架 | [https://element.eleme.io/](http://u.720life.cn/g/5fa51553afae358345e9f20b5a6e741569ec367dcef795a9cc086ceba9a9242d) 
Axios | 前端HTTP框架 | [https://github.com/axios/axios](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304638015ac6a54b1cadf0934b8a0d5637d0) 
v-charts | 基于Echarts的图表框架 | [https://v-charts.js.org/](http://u.720life.cn/g/04bb650c6b9547d2ac7f61bed3e715031e418e4efd3cee1a70120fe3eff14e14) 
Js-cookie | cookie管理工具 | [https://github.com/js-cookie/js-cookie](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304601a18a0a98543c227ccab0f66e611f0076dc75769652863fa8e48c713794768c) 
nprogress | 进度条控件 | [https://github.com/rstacruz/nprogress](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304621051bfe8a14df709920d1b59773b4a1b34b830a15281032ae36824abb143cae) 
vue-element-admin | 项目脚手架参考 | [https://github.com/PanJiaChen/vue-element-admin](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304603c6efa7d0c1ce77680f5b6f938bd6cef861f7dd6d31dc89ca07ef0b5d2b912f) 

### 项目布局

``` lua
src -- 源码目录
├── api -- axios网络请求定义
├── assets -- 静态图片资源文件
├── components -- 通用组件封装
├── icons -- svg矢量图片文件
├── router -- vue-router路由配置
├── store -- vuex的状态管理
├── styles -- 全局css样式
├── utils -- 工具类
└── views -- 前端页面
    ├── home -- 首页
    ├── layout -- 通用页面加载框架
    ├── login -- 登录页
    ├── oms -- 订单模块页面
    ├── pms -- 商品模块页面
    └── sms -- 营销模块页面
```

## 搭建步骤
- 下载node并安装：[https://nodejs.org/dist/v8.9.4/node-v8.9.4-x64.msi](http://u.720life.cn/g/6dd25ec2eceebbb6348ad519a7343cbcc5c8f7ce82ebe0f8d2124294c3523c4f4db1bc94719789402538831ec8d524c4d5d2b4576c700397587d26dc8248cf1a 
- 该项目为前后端分离项目，访问本地访问接口需搭建后台环境，搭建请参考后端项目[传送门](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046792cbfb2e1cb72d9aec12faeaa3f53b493edd723f853ea93b9a80ae2239380cc 
- 访问在线接口无需搭建后台环境，只需将config/dev.env.js文件中的BASE_API改为[http://39.98.190.128:8080]http://39.98.190.128:8080)即可;
- 克隆源代码到本地，使用IDEA打开，并完成编译;
- 在IDEA命令行中运行命令：npm install,下载相关依赖;
- 在IDEA命令行中运行命令：npm run dev,运行项目;
- 访问地址：[http://localhost:8090](http://u.720life.cn/g/e71094f6077cb9592da5b56893f0ad14118c17b6013fd67cd8fa329d270db4b6)  即可打开后台管理系统页面;
- 如果遇到无法运行该命令，需要配置npm的环境变量，如在path变量中添加：C:\Users\zhenghong\AppData\Roaming\npm。

## 许可证

[MIT](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046792cbfb2e1cb72d9aec12faeaa3f53b4f9efd9a81e2cdd5b348c56cc4067ca311dc77a05aaa34ab032a2e40ae5bae915) 

Copyright (c) 2018-2019 macrozheng



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)