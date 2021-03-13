 
   
 


 
   
     
   
   
     
   
     
     
   
 


  [English](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cd3b6a876ba1c05ae60a2f3ba3db9d95dfb0fb413a15dfdf98248b4ef7aef1124ac92dd68e2f2b203ec1ebf593251dfb63ee4e2bd867800ac2532890dbb1ddd3)  | 简体中文
  

##### 基于Gin + Vue + Element UI的前后端分离权限管理系统 

系统初始化极度简单，只需要配置文件中，修改数据库连接，系统启动后会自动初始化数据库信息以及必须的基础数据

[在线文档](http://u.720life.cn/g/f561cc518ab4b3eb17e072bc4a1cb4ebbd0e08ba191d5e62c1c47b14921dd2a1b7dfe42a1c2d309b91e0a1bcdb0b3b93) 

[视频教程](http://u.720life.cn/g/53d965c89cfaa89e69480af221ad5eb1ae34957e36b22d259ea2dad18ce05b01e9432b3d2d76b30b5fe1db30230faffe32281df90b230e1d0a1a8aa231eb5da6) 

## ✨ 特性

- 遵循 RESTful API 设计规范

- 基于 GIN WEB API 框架，提供了丰富的中间件支持（用户认证、跨域、访问日志、追踪ID等）

- 基于Casbin的 RBAC 访问控制模型

- JWT 认证

- 支持 Swagger 文档(基于swaggo)

- 基于 GORM 的数据库存储，可扩展多种类型数据库 

- 配置文件简单的模型映射，快速能够得到想要的配置

- 代码生成工具

- 表单构建工具

- 多命令模式

- TODO: 单元测试


## 🎁 内置

1.  用户管理：用户是系统操作者，该功能主要完成系统用户配置。
2.  部门管理：配置系统组织机构（公司、部门、小组），树结构展现支持数据权限。
3.  岗位管理：配置系统用户所属担任职务。
4.  菜单管理：配置系统菜单，操作权限，按钮权限标识等。
5.  角色管理：角色菜单权限分配、设置角色按机构进行数据范围权限划分。
6.  字典管理：对系统中经常使用的一些较为固定的数据进行维护。
7.  参数管理：对系统动态配置常用参数。
8.  操作日志：系统正常操作日志记录和查询；系统异常信息日志记录和查询。
9.  登录日志：系统登录日志记录查询包含登录异常。
10. 系统接口：根据业务代码自动生成相关的api接口文档。
11. 代码生成：根据数据表结构生成对应的增删改查相对应业务，全部可视化编程，基本业务可以0代码实现。
12. 表单构建：自定义页面样式，拖拉拽实现页面布局。
13. 服务监控：查看一些服务器的基本信息。

## 准备工作

你需要在本地安装 [go] [gin] [node](http://u.720life.cn/g/c47729c1c499a00d6e30af9fa18eaddd7b41ca24e187ea438549a271175cdbab)  和 [git](http://u.720life.cn/g/0699e533b96232c5e210af6ab5668134e6f26f1fc99a343a9eacc50fbfcb0e97)  

同时配套了系列教程包含视频和文档，如何从下载完成到熟练使用，强烈建议大家先看完这些教程再来实践本项目！！！

### 轻松实现go-admin写出第一个应用 - 文档教程

[步骤一 - 基础内容介绍](http://u.720life.cn/g/b794eac17d27ee9715142db702c33bbd6fda72d4788ea5dee9478b827675c37a00617c2d16384df0f40b52f42fe46826e3aa2d5cf3ca7d89586e68d7c617324b) 

[步骤二 - 实际应用 - 编写增删改查](http://u.720life.cn/g/b794eac17d27ee9715142db702c33bbd6fda72d4788ea5dee9478b827675c37a00617c2d16384df0f40b52f42fe4682694aa622e473d43f069c8d7c13f5acd72)  

### 手把手教你从入门到放弃 - 视频教程 

[如何启动go-admin](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e1f29e3db200d2f8cfc1fc408d18455317af5a5b0a4741939de2953b2f5c4ce6e6) 

[使用生成工具轻松实现业务](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e1f29e3db200d2f8cfc1fc408d18455317e484a112e280ef898ee6215b997e24e1) 

[go-admin菜单的配置说明](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e1f29e3db200d2f8cfc1fc408d184553172946dc19bef8c173f8d89d4269e54eba) 

[多命令启动方式讲解以及IDE配置](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e1f29e3db200d2f8cfc1fc408d1845531719a4f3d33b2862d9ad2b1826a646f40b) 

**如有问题请先看上述使用文档和文章，若不能满足，欢迎 issue 和 pr ，视频教程和文档持续更新中**

## 📦 本地开发

### 首次启动说明

```bash
# 获取代码
git clone https://github.com/wenjianzhang/go-admin.git

# 进入工作路径
cd ./go-admin

# 编译项目
go build

# 修改配置 
# 文件路径  go-admin/config/settings.yml
vi ./config/setting.yml 

# 1. 配置文件中修改数据库信息 
# 注意: settings.database 下对应的配置数据
# 2. 确认log路径

```

### 初始化数据库，以及服务启动
```
# 首次配置需要初始化数据库资源信息
./go-admin init -c config/settings.yml -m dev


# 启动项目，也可以用IDE进行调试
./go-admin server -c config/settings.yml -p 8000 -m dev

```

### 文档生成
```bash
swag init  

# 如果没有swag命令 go get安装一下即可
go get -u github.com/swaggo/swag/cmd/swag
```

### 交叉编译
```bash
env GOOS=windows GOARCH=amd64 go build main.go

# or

env GOOS=linux GOARCH=amd64 go build main.go
```


## 🎬 在线体验
> admin  /  123456

演示地址：[http://www.zhangwj.com](http://u.720life.cn/g/9de410eefb2e8800a0633adea37e119dced96ff4b048a626607f493aee119330) 


## 📨 互动

 
   
       
       
       
   
   
     微信 
     此群已满 
         
   
 
  

## 🤝 特别感谢
[chengxiao](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c7e442cdfac58bb50b2dcb21b310d2a7) 
[gin](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58e44c7b16b1ea7d34670c8c0a23cb0) 
[casbin](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c780c9cff43791c99b3f75b50fcc5663) 
[spf13/viper](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304649ef09b7201fe77b43e1bbb5c1234e37) 
[gorm](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304602ff7e8b94ad4dc36c0b36719e41af31) 
[gin-swagger](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461de1b9a11e8cc0695b1528342272cc1b2b01095b908d884c6df88b01556c6123) 
[jwt-go](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465767d14a9dbc49e037097816375c851965b59a361789da6e86860712b043c8cb) 
[vue-element-admin](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304603c6efa7d0c1ce77680f5b6f938bd6cef861f7dd6d31dc89ca07ef0b5d2b912f) 
[ruoyi-vue](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e4efbf9a2018792702bfb8d2f94b55c6d7a2c36c7bc4d3e3beccaae130c5d21a5) 

## 🤟 打赏

> 如果你觉得这个项目帮助到了你，你可以帮作者买一杯果汁表示鼓励 :tropical_drink:


 

## ❤️ 赞助者

zhuqiyun LLL狐

## 🔑 License

[MIT](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cd3b6a876ba1c05ae60a2f3ba3db9d95dfb0fb413a15dfdf98248b4ef7aef112138aa3a0ce2ddfaea072e551223da3b9) 

Copyright (c) 2020 wenjianzhang




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)