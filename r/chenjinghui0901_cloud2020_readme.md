# 尚硅谷2020最新版SpringCloud(H版&alibaba)框架开发教程全套完整版从入门到精通(大牛讲授spring cloud)

## 0. 视频地址

[视频教程](http://u.720life.cn/g/0b2e9c050c16e17e2de17da38fe221e14e891e7f464d808a8bfeaa8b64b73a970e8cf176e09087dbf76a0607292676a0) 

## 1. 笔记
1) doc目录

2) 工具

下载[MindManager 2020](http://u.720life.cn/g/5e614f17fdc975f12cbdb81fec0cbe7b06ce871987736d47787478df92a5b82d9f90198e2213f7d62bdfaea039c4721c02300b3c8a4711ef1a55c1a2d979774a7db714c149db35061d8e06962ba38b682b7d06fe87022e47c8c078f912fc2225) 

激活码
```text
2019: MP19-777-APE8-1162-BD8E

2020: MP20-345-DP56-7778-919A
```

3) github下载失败

[gitee导入github仓库](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e1edbdc1f0b955db0bfc1deeb1cc0e82f85e9d4563c2e694621c0b2148e944e3d) 

## 2. 启动前准备
### 2.1 数据库
* 执行sql脚本 doc/db2019.sql
* 修改数据库的配置

```text
cloud-provider-payment8001\src\main\resources\application.yml中
mysql的用户名和密码
```

### 2.2 修改hosts
找到C:\Windows\System32\drivers\etc路径下的hosts文件,添加

```text
127.0.0.1 eureka7001.com
127.0.0.1 eureka7002.com
```
### 2.3 修改zookeeper的地址

cloud-provider-payment8004\src\main\resources\application.yml

spring.cloud.zookeeper.connect-string=localhost:2181

## 3 软件
* Zookeeper
* consul
* JMeter
* RabbitMq
* [Seata-server](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f64df6c70b66ea8fb38015aacfcceca0d1c44d7cd2fab38c937e048e32531859583f2a894e3876e480c5605e2c3d1ec0bb9846a5df6f7dc07fd416751ca09a61) 
* zipkin-server



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)