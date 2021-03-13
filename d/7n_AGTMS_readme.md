# Auto-Generate Template Management System

           d8888  .d8888b. 88888888888 888b     d888  .d8888b.  
          d88888 d88P  Y88b    888     8888b   d8888 d88P  Y88b 
         d88P888 888    888    888     88888b.d88888 Y88b.      
        d88P 888 888           888     888Y88888P888  "Y888b.   
       d88P  888 888  88888    888     888 Y888P 888     "Y88b. 
      d88P   888 888    888    888     888  Y8P  888       "888 
     d8888888888 Y88b  d88P    888     888   "   888 Y88b  d88P 
    d88P     888  "Y8888P88    888     888       888  "Y8888P"  

[![CircleCI](https://img.shields.io/circleci/build/github/Saisimon/AGTMS/dev.svg)](https://circleci.com/gh/Saisimon/AGTMS/tree/dev)
[![Codecov branch](https://img.shields.io/codecov/c/github/Saisimon/AGTMS/dev.svg)](https://codecov.io/gh/Saisimon/AGTMS)
[![Codacy branch grade](https://img.shields.io/codacy/grade/13d287dc9b6c4d1d9e219369a890d385/dev.svg)](https://www.codacy.com?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Saisimon/AGTMS&amp;utm_campaign=Badge_Grade)
[![Total Lines](https://tokei.rs/b1/github/Saisimon/AGTMS)](https://github.com/Saisimon/AGTMS)
![GitHub](https://img.shields.io/github/license/Saisimon/AGTMS.svg)

AGTMS 是一个基于 Spring Cloud 和 Vue.js 的自定义配置对象管理系统，支持 Oracle、MySQL、MariaDB、SQL Server、PostgreSQL、MongoDB、RESTful 等方式获取数据。

## 分支
* [dev](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e8e3ad574efc69386e91aab74cccffb3019316d5740f7eb3408a25465181e1c)  - 开发分支
* [master](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e8e3ad574efc69386e91aab74cccffb0b51f8514464de22aa7bd54e90a08c31)  - 分布式环境
* [standalone](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460e8e3ad574efc69386e91aab74cccffb8f253431b3064d9b4f74f6f4062a2cb476408c33e37aba3d8eba4110f0b90bc8)  - 单机环境

## 项目结构
```
.
├── agtms-admin         Spring Boot Admin 服务 (可选)(默认端口：7890, 默认用户：agtms， 密码：agtms7890)
├── agtms-autoconfigure 自动配置支持类库
├── agtms-autotest      自动化测试
├── agtms-example       远程调用示例服务 (默认端口：7899)
├── agtms-parent 
│   ├── agtms-api       内部接口类库
│   ├── agtms-config    配置类库
│   ├── agtms-core      核心类库
│   ├── agtms-jpa       JPA 实现支持类库 (默认为 H2，支持 Oracle、MySQL、MariaDB、SQL Server、PostgreSQL 数据库)
│   ├── agtms-mongodb   MongoDB 实现支持类库 (可选)
│   ├── agtms-redis     Redis 支持类库 (可选)
│   ├── agtms-remote    远程调用实现支持类库 (可选)
│   └── agtms-web       Web 服务 (默认端口：7892, 默认用户：admin， 密码：123456)
├── agtms-record        集成测试报告聚合模块
├── agtms-vue           前端页面 (默认端口：8080)
├── agtms-zuul          Zuul 网关服务 (默认端口：7891)
├── data                Docker 相关数据
│   └── web
|       ├── config      Web 服务额外配置
|       ├── files       Web 服务文件（图片、导入、导出）路径
|       └── libs        Web 服务额外 jar 库路径
├── .env                Docker Compose 环境变量配置
├── docker-compose.yml  Docker Compose 配置
├── README.md           README 文件
├── start.cmd           一键启动脚本 (Windows)
├── stop.cmd            停止脚本 (Windows)
├── start               一键启动脚本 (Unix)
└── stop                停止脚本 (Unix)
```

## 先决条件
1. [JRE(JDK) 8+](http://u.720life.cn/g/c53b0b72f0b9b611a7730ceefc47d4ea24729298bd586cfed472b72f962df696) 
2. [Node.js](http://u.720life.cn/g/6dd25ec2eceebbb6348ad519a7343cbc690041c96fefc0320d9aace915151649) 
3. [Apache ZooKeeper](http://u.720life.cn/g/9036bb30203a9192b0bca1ff23f6480f71d7ad868c7c8d1a9b3c2b9a91b88dd3) 
4. RAM 4G+
   
或

1. [Docker](http://u.720life.cn/g/d13d2b0ef4a5c92b4f4a6e9ed4270e65b90c4c1e1b506e1a501feef81ad769e9) 

## 安装并启动
### 一键启动
`默认使用 H2 内存数据库，每次重启数据会重制。要想保存数据，请自行配置数据库连接`
1. 准备 [Zookeeper](http://u.720life.cn/g/9036bb30203a9192b0bca1ff23f6480fcc0ca0457836a7b9f60327021c8a517cd2f60d89796ff6367725f86c7d00146a20ddec484b0c93f603790cec1ba66214)  并配置 hosts
* `/etc/hosts` (Unix)
* `c:\windows\system32\drivers\etc\hosts` (Windows)
```
    zookeeperserver
```
2. 执行启动脚本
* **`start.cmd 默认会杀掉占用 7890、7891、7892端口的进程，请确认以后再执行操作`**
```sh
# Unix
./start

# Windows
start.cmd
```
1. 访问
```html
http://localhost:8080
```
4. 日志
```
data
├── admin 
|   └── agtms-admin.log   Spring Boot Admin 服务日志
├── web 
|   └── agtms-web.log     Web 服务日志
└── zuul
    └── agtms-zuul.log    网关日志
```

### 分步启动
`默认使用 H2 内存数据库，每次重启数据会重制。要想保存数据，请自行配置数据库连接`
1. 准备 [Zookeeper](http://u.720life.cn/g/9036bb30203a9192b0bca1ff23f6480fcc0ca0457836a7b9f60327021c8a517cd2f60d89796ff6367725f86c7d00146a20ddec484b0c93f603790cec1ba66214)  并配置 hosts
* `/etc/hosts` (Unix)
* `c:\windows\system32\drivers\etc\hosts` (Windows)
```
    zookeeperserver
```
2. 打包
```sh
# Unix
./mvnw clean package -Ddockerfile.skip=true

# Windows
mvnw.cmd clean package -Ddockerfile.skip=true
```
3. 启动Web 服务 (agtms-web)
```sh
java -jar agtms-parent/agtms-web/target/agtms-web.jar
```
4. 启动网关服务 (agtms-zuul)
```sh
java -jar agtms-zuul/target/agtms-zuul.jar
```
5. 启动前端页面 (agtms-vue)
```sh
cd agtms-vue
npm install
npm run serve
```
6. 访问
```html
http://localhost:8080
```
7. 启动 Spring Boot Admin 服务 (agtms-admin)
```sh
java -jar agtms-admin/target/agtms-admin.jar
```
8. 日志
```
data
├── admin 
|   └── agtms-admin.log   Spring Boot Admin 服务日志
├── web 
|   └── agtms-web.log     Web 服务日志
└── zuul
    └── agtms-zuul.log    网关服务日志
```

### Docker 容器启动
1. 安装 [Docker CE](http://u.720life.cn/g/fe36d46bcf13791bdad89a5e154210d96d905095cc34802ef171f399860c0255)  或者 [Docker EE]https://docs.docker.com/ee/supported-platforms/)，请参考官方文档下载安装
2. 安装 [Docker Compose]https://docs.docker.com/compose/install/)，请参考官方文档下载安装
3. 编译 Java 项目并生成 Docker 镜像
```sh
# Unix
./mvnw clean package

# Windows
mvnw.cmd clean package
```
4. data/web/libs 路径下添加对应数据库驱动 jar 包
* 默认使用 MySQL 5.7
```sh
# mysql-connector-java-8.0.16.jar
wget -P data/web/libs http://central.maven.org/maven2/mysql/mysql-connector-java/8.0.16/mysql-connector-java-8.0.16.jar
```
5. 启动容器
* WEB_CONFIG_HOME：Web 服务额外配置，默认为 ./data/web/config
* WEB_LIBS_HOME：Web 服务额外 jar 库路径，默认为 ./data/web/libs
* REVISION:：版本号，默认为最新版本
```sh
# Docker Compose
docker-compose up -d

# Docker Swarm
docker stack deploy -c docker-compose.yml agtms
```
6. 访问
```html
http://localhost:8080
```

## 远程调用示例
1. 准备 [Zookeeper](http://u.720life.cn/g/9036bb30203a9192b0bca1ff23f6480fcc0ca0457836a7b9f60327021c8a517cd2f60d89796ff6367725f86c7d00146a20ddec484b0c93f603790cec1ba66214)  并配置 hosts
* `/etc/hosts` (Unix)
* `c:\windows\system32\drivers\etc\hosts` (Windows)
```
    zookeeperserver
```
2. 启动 agtms 服务
```sh
# Unix
./start

# Windows
start.cmd
```
3. 启动 agtms-example 服务
```sh
java -jar agtms-example/target/agtms-example.jar
```
4. 访问
```html
http://localhost:8080
```

## 自动化测试

### Chrome
1. 下载与 Chrome 浏览器对应版本的 [Chrome Driver]https://sites.google.com/a/chromium.org/chromedriver/downloads)，并解压缩
2. 配置 Chrome Driver 路径
* `agtms-autotest/src/main/resources/autotest.properties`
```properties
auto.test.chrome.driver=/Users/saisimon/Downloads/chromedriver
```
3. 运行测试用例
* `agtms-autotest/src/test/java/net/saisimon/agtms/autotest/ChromeTest`

### Firefox
1. 下载最新版本的 [Gecko Driver]https://github.com/mozilla/geckodriver/releases)，并解压缩
2. 配置 Gecko Driver 路径
* `agtms-autotest/src/main/resources/autotest.properties`
```properties
auto.test.firefox.driver=/Users/saisimon/Downloads/geckodriver
```
3. 运行测试用例
* `agtms-autotest/src/test/java/net/saisimon/agtms/autotest/FirefoxTest`


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)