  
       
       
   
    
    
    
    
  
  
    
  
    

## SpringBlade微服务开发平台
* 采用前后端分离的模式，前端开源两个框架：[Sword](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e3f06a8ff808883495d0c666de7366852)  (基于 React、Ant Design)、[Saber](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb45756d3fb107733267a8309a173eb84)  (基于 Vue、Element-UI)
* 后端采用SpringCloud全家桶，并同时对其基础组件做了高度的封装，单独开源出一个框架：[BladeTool](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465d7fae41e59aef8f755694da1e75d01333391ed8d85b1b0d710703a19476207a) 
* [BladeTool]https://github.com/chillzhuang/blade-tool)已推送至Maven中央库，直接引入即可，减少了工程的臃肿，也可更注重于业务开发
* 集成Sentinel从流量控制、熔断降级、系统负载等多个维度保护服务的稳定性。
* 注册中心、配置中心选型Nacos，为工程瘦身的同时加强各模块之间的联动。
* 使用Traefik进行反向代理，监听后台变化自动化应用新的配置文件。
* 极简封装了多租户底层，用更少的代码换来拓展性更强的SaaS多租户系统。
* 借鉴OAuth2，实现了多终端认证系统，可控制子系统的token权限互相隔离。
* 借鉴Security，封装了Secure模块，采用JWT做Token认证，可拓展集成Redis等细颗粒度控制方案。
* 稳定生产了一年，经历了从Camden -> Greenwich的技术架构，也经历了从fat jar -> docker -> k8s + jenkins的部署架构
* 项目分包明确，规范微服务的开发模式，使包与包之间的分工清晰。

## 架构图
 

## 工程结构
``` 
SpringBlade
├── blade-auth -- 授权服务提供
├── blade-common -- 常用工具封装包
├── blade-gateway -- Spring Cloud 网关
├── blade-ops -- 运维中心
├    ├── blade-admin -- spring-cloud后台管理
├    ├── blade-develop -- 代码生成
├    ├── blade-resource -- 资源管理
├    ├── blade-seata-order -- seata分布式事务demo
├    ├── blade-seata-storage -- seata分布式事务demo
├── blade-service -- 业务模块
├    ├── blade-desk -- 工作台模块 
├    ├── blade-log -- 日志模块 
├    ├── blade-system -- 系统模块 
├    └── blade-user -- 用户模块 
├── blade-service-api -- 业务模块api封装
├    ├── blade-desk-api -- 工作台api 
├    ├── blade-dict-api -- 字典api 
├    ├── blade-system-api -- 系统api 
└──  └── blade-user-api -- 用户api 
```

## 官网
* 官网地址：[https://bladex.vip](http://u.720life.cn/g/e880dc0155786da80a323ca51fc84cb1bfebbc18fcceb4095983e3a1fd626d7d) 
* 问答社区：[https://sns.bladex.vip](http://u.720life.cn/g/6d08c7017bd2aa4f5a480efff2c95dbb1796c8f53327f40b5b872ad79c7c03a2) 
* 会员计划：[SpringBlade会员计划]https://gitee.com/smallc/SpringBlade/wikis/SpringBlade会员计划
* 交流一群：`477853168`
* 交流二群：`751253339`

## 在线演示
* Saber-基于Vue：[https://saber.bladex.vip](http://u.720life.cn/g/a2067056ae624cfae81175ec598dc15bdc6c61bbdd200abdd681a1ae366d9e73) 
* Sword-基于React：[https://sword.bladex.vip](http://u.720life.cn/g/8c06daca92564bb98ac9291bb05f792a10d4b8507f6552e1bc9483625dd243c0) 
* Archer-全能代码生成系统：[https://archer.bladex.vip](http://u.720life.cn/g/4b9ccc3e90ac082b9d58131e96691fec429c3ed84f62bcccb79f1956a334fcb4) 

## 技术文档
* [SpringBlade开发手册一览]https://gitee.com/smallc/SpringBlade/wikis/SpringBlade开发手册
* [常见问题集锦](http://u.720life.cn/g/6d08c7017bd2aa4f5a480efff2c95dbb45fa5e679adf555cd44461de22187c1e22984b8b53c44e69a60f2ab3918c5be7) 

## 项目地址
* 后端Gitee地址：[https://gitee.com/smallc/SpringBlade](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e3546460c0cd5dba4cbac39602ce9c18cfb9683eaf44923e5c878f4ad4056bdf6) 
* 后端Github地址：[https://github.com/chillzhuang/SpringBlade](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468a101b2ec06b992f29493ffda32a7f3daf3b99cc67dd7171893332cab2aab16a) 
* 后端SpringBoot版：[https://gitee.com/smallc/SpringBlade/tree/2.0-boot/](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e3546460c0cd5dba4cbac39602ce9c18c3f744bb9c792438b4057e701dbfe6f55ad7d242ad7ff833a32dd47ee9ddd3124) 
* 前端框架Sword(基于React)：[https://gitee.com/smallc/Sword](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e3f06a8ff808883495d0c666de7366852) 
* 前端框架Saber(基于Vue)：[https://gitee.com/smallc/Saber](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb45756d3fb107733267a8309a173eb84) 
* 核心框架项目地址：[https://github.com/chillzhuang/blade-tool](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465d7fae41e59aef8f755694da1e75d01333391ed8d85b1b0d710703a19476207a) 

# 开源协议
Apache Licence 2.0 （[英文原文]http://www.apache.org/licenses/LICENSE-2.0.html)）
Apache Licence是著名的非盈利开源组织Apache采用的协议。该协议和BSD类似，同样鼓励代码共享和尊重原作者的著作权，同样允许代码修改，再发布（作为开源或商业软件）。
需要满足的条件如下：
* 需要给代码的用户一份Apache Licence
* 如果你修改了代码，需要在被修改的文件中说明。
* 在延伸的代码中（修改和有源代码衍生的代码中）需要带有原来代码中的协议，商标，专利声明和其他原来作者规定需要包含的说明。
* 如果再发布的产品中包含一个Notice文件，则在Notice文件中需要带有Apache Licence。你可以在Notice中增加自己的许可，但不可以表现为对Apache Licence构成更改。
Apache Licence也是对商业应用友好的许可。使用者也可以在需要的时候修改代码来满足需要并作为开源或商业产品发布/销售。

## 用户权益
* 允许免费用于学习、毕设、公司项目、私活等。
* 对未经过授权和不遵循 Apache 2.0 协议二次开源或者商业化我们将追究到底。
* 参考请注明：参考自 SpringBlade：https://gitee.com/smallc/SpringBlade 。另请遵循 Apache 2.0 协议。
* `注意`：若禁止条款被发现有权追讨 **19999** 的授权费。

# 界面

## [BladeX](http://u.720life.cn/g/e880dc0155786da80a323ca51fc84cb1ff5b8de4683f6a5f7b4c3c67bfd5fa5a)  工作流一览
 
     
           
           
     
     
           
           
     
     
           
           
     
 

## [Sword](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e3f06a8ff808883495d0c666de7366852)  界面一览
 
     
           
           
     
     
           
           
     
     
           
           
     
     
           
           
     
     
           
           
     
 

## [Saber](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6eb45756d3fb107733267a8309a173eb84)  界面一览
 
     
           
           
     
     
           
           
     
     
           
           
     
 

## 监控界面一览
 
     
           
           
     
     
           
           
     
     
           
           
     
     
           
           
     
     
           
           
     
     
           
           
     
 

## 关注我们
![](https://images.gitee.com/uploads/images/2019/0330/065148_f0ada806_410595.jpeg)


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)