# Introduction

作为 [Humpback](http://u.720life.cn/g/90ae92e9fe8570b04fe6e458bbed6ea55170410703522198f94429a5691007e96ae35d6e8f79202b661de752fb53bd6a)  的直观展现，基于 [Angular2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469fb2c5f2150d8d592c0546566cf3dfb635066b3867b2d2d7b8044d0dd39953b1)  和 [AdminLTE](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469938d875cf47e5488f379f965eb2a0745e6b8f3c0029e0f6d8e8db173b9167bf)  构建的用于管理 `docker ` 的网站。

# Usage
```bash
git clone https://gitee.com/humpbacks/humpback-web.git
cd humpback-web
npm install
npm start
```
Open [http://localhost](http://u.720life.cn/g/e71094f6077cb9592da5b56893f0ad14) 

Default Account    
>UserID: `admin`   
Password: `123456`    

# Docker image
[![](https://images.microbadger.com/badges/image/humpbacks/humpback-web:1.3.0.svg)](https://microbadger.com/images/humpbacks/humpback-web:1.3.0 "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/humpbacks/humpback-web:1.3.0.svg)](https://microbadger.com/images/humpbacks/humpback-web:1.3.0 "Get your own version badge on microbadger.com")
```bash
$ docker pull humpbacks/humpback-web:1.3.0

$ docker run -d --net=host --restart=always -e HUMPBACK_LISTEN_PORT=8012 \
  -v /opt/app/humpback-web/dbFiles:/humpback-web/dbFiles \
  --name humpback-web \
  humpbacks/humpback-web:1.3.0
```

# Functions
- 服务器分组管理
- 容器及镜像管理
- 容器批量操作
- 容器实时监控
- 容器日志查看
- 私有仓库管理
- etc.

# Sample Page
#### Login Page
![image](https://cloud.githubusercontent.com/assets/9428909/22197325/73c2aba4-e18c-11e6-9c9a-c00318abf6f5.png)

#### Server Overview
![image](https://cloud.githubusercontent.com/assets/9428909/22238288/9fc10bc8-e24b-11e6-840a-87699929063f.png)

#### New Container
![image](https://cloud.githubusercontent.com/assets/9428909/22238315/b8292790-e24b-11e6-84ba-58e97288a104.png)

#### Private registry explore - docker image detail
![image](https://cloud.githubusercontent.com/assets/9428909/22238333/ca0debee-e24b-11e6-871b-a1134ed8af46.png)
etc.

## License

Apache-2.0



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)