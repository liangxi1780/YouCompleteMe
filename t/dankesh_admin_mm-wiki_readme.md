![brand](./static/images/logo_sm.png)

MM-Wiki 是一个轻量级的企业知识分享与团队协同软件，可用于快速构建企业 Wiki 和团队知识分享平台。部署方便，使用简单，帮助团队构建一个信息共享、文档管理的协作环境。

[![stable](https://img.shields.io/badge/stable-stable-green.svg)](https://github.com/phachon/mm-wiki/) 
[![build](https://img.shields.io/shippable/5444c5ecb904a4b21567b0ff.svg)](https://travis-ci.org/phachon/mm-wiki)
[![license](http://img.shields.io/badge/license-MIT-red.svg?style=flat)](https://raw.githubusercontent.com/phachon/mm-wiki/master/LICENSE)
[![platforms](https://img.shields.io/badge/platform-All-yellow.svg?style=flat)]()
[![download_count](https://img.shields.io/github/downloads/phachon/mm-wiki/total.svg?style=plastic)](https://github.com/phachon/mm-wiki/releases) 
[![release](https://img.shields.io/github/release/phachon/mm-wiki.svg?style=flat)](https://github.com/phachon/mm-wiki/releases) 

>> Demo 网站：http://mm-wiki.phachon.com 账号：admin 密码：123456

# 特点
- 部署方便，基于 golang 编写，只需要下载对于平台下二进制文件执行即可。
- 快速安装程序, 提供方便的安装界面程序，无需任何手动操作。
- 独立的空间，空间是一组文档的集合，一般为公司部门或者团队，空间下的文档相互独立。空间可根据需求设置空间访问级别。
- 完善的系统权限管理，系统可以自定义角色，并为不同角色授予不同的权限。
- 集成统一登录，本系统支持通过外部系统认证用户, 比如与公司的 LDAP 登录融合。具体请看登录认证功能。
- 邮件通知功能，当开启邮件通知，文档更改会通知所有关注该文档的用户。
- 文档具有分享和下载功能，目前只支持下载 MarkDown 源文件。

# 安装
## 1. 自助安装

打开 https://github.com/phachon/mm-wiki/releases 找到对应平台的版本下载编译好的压缩包

- Linux 平台

    ```
    # 创建目录
    $ mkdir mm_wiki
    $ cd mm_wiki
    # 以 linux amd64 为例，下载最新版本压缩包
    # https://github.com/phachon/mm-wiki/releases 自行下载 wget http://
    # 解压到当前目录
    $ tar -zxvf mm-wiki-linux-amd64.tar.gz
    # 进入程序安装目录
    $ cd install
    # 执行安装程序，默认端口为 8090，指定其他端口加参数 --port=8087
    $ ./install
    # 浏览器访问 http://ip:8090 进入安装界面，完成安装配置
    # Ctrl + C 停止 install 程序, 启动 MM-Wiki 系统
    $ cd ..
    $ ./mm-wiki --conf conf/mm-wiki.conf
    # 浏览器访问你监听的 ip 和端口
    # 开始 MM-Wiki 的使用之旅吧！
    ```

- Windows 平台

    ```
    # 以 windows amd64 为例，下载最新版本压缩包
    # https://github.com/phachon/mm-wiki/releases 自行下载
    # 手动解压到当前目录
    # 进入 install 目录
    # 双击点开 install.exe 文件
    # 浏览器访问 http://ip:8090 进入安装界面，完成安装配置
    # 关闭刚刚点开的 install 窗口
    # 使用 windows 命令行工具（cmd.exe）进入程序根目录
    $ 执行 mm-wiki.exe --conf conf/mm-wiki.conf
    # 浏览器访问你监听的 ip 和端口
    # 开始 MM-Wiki 的使用之旅吧！
    ```

## 2. 如果需要，可用 nginx 配置反向代理
```
upstream frontends {
    server 127.0.0.1:8088; # MM-Wiki 监听的ip:port
}
server {
    listen      80;
    server_name wiki.intra.xxxxx.com www.wiki.intra.xxxxx.com;
    location / {
        proxy_pass_header Server;
        proxy_set_header Host $http_host;
        proxy_redirect off;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Scheme $scheme;
        proxy_pass http://frontends;
    }
    # 静态资源交由nginx管理
    location /static {
        root        /www/mm-wiki; # MM-Wiki 的根目录
        expires     1d;
        add_header  Cache-Control public;
        access_log  off;
    }
}
```

# 系统预览

### 1 安装
![install](./static/images/preview/install.png)
### 2 登录
![login](./static/images/preview/login.png)
### 3 系统
![system](./static/images/preview/system.png)
### 4 空间文档
![space](./static/images/preview/space.png)
### 5 编辑文档
![edit](./static/images/preview/edit.png)
### 6 文档分享
![share](./static/images/preview/share.png)

# 使用的一些插件

MM-Wiki 是站在巨人的肩膀上开发的一款软件，是因为系统中使用了非常多优秀的插件，非常感谢这些插件的作者们：

- [bootstrap](http://u.720life.cn/g/54145d0471d91890860f7f8463c030465a8160a390414e5887ea7b27f65f8894df8a88b45f3cfc9c4098552eeb42db05) 
- [awesome-bootstrap-checkbox](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a4caf147bddfd4a21c5e27425a55b8c798b45e1b2811bb212aeb7a044529bd6ab596a2bf5c126a5467801cc887730f2c) 
- [bootstrap-iconpicker](http://u.720life.cn/g/cc1d0826d05a618e539bcd345f104f22998e741eb1238730d005ed1327f379b5dd666ce70b59c821c2a258b8bf8eb78e72373d72c05b6aab44f0eea755f7f5af) 
- [bootstrap-select](http://u.720life.cn/g/abaa726577fe7141431478c223bd65e62f27d91a29e732f8260fb2dbc12ec6a6ab01f958c6291e29a3c3dec8764ec639) 
- [bootstrap-switch](http://u.720life.cn/g/e4cd418b27da6305b7054997a23b7bfd9d5d25f67b267e6e855989dfc8927dd964bef8d885a0fdb8405656d938db56e1) 
- [bootstrap-tagsinput](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046586aa5cfdf736bbfd8d1e91244679d15e81aad3c15e5ed1c0762c95b31fd4f9b87ff14e95e2455948a8c79008ecc0e98) 
- [editor.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c2531d0d62bc04ab421ebd243aa86e7ae67e52b2770e61c62b007b56ee3731ca) 
- [layout](http://u.720life.cn/g/d0ea3845f2567bb26b071ce419f0dab779e4872dbf3388629f73d60fe7ccc13e) 
- [layer](http://u.720life.cn/g/d6276f71012dea0742ec9af0acbaffd3bd2dc9703f25e563fbb8b365fdb374da) 
- [metisMenu](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468ca112927ad45fa04b8c486dad7d4d2045b9b6be0d06e4ab485f34524cf59e45) 
- [morris](http://u.720life.cn/g/74c7ce6b251f986d92be6604977aecc1a8edf99861fb329dfe8b190c96aa3ca0358db18297016a3a632884c455cfe11f) 
- [popover](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ab8d065b38a17e9f5be346dba7bf91a0bb54d63436bdd9457ac8edf94fd33629) 
- [scrollup](http://u.720life.cn/g/78cdd7ceb9f40f0e167156517b7244e0834e5e2527f2ef8c8c0fc532a21f7ad8eb5ee9616cc04f9fb8d1eb25792c9d87) 
- [zTreev3](http://u.720life.cn/g/1adb03b4d49983613c5a03444af006aa195e5591db5ffab98220e909b0554737) 

# 二次开发

环境要求：go 1.8
```
$ git clone https://github.com/phachon/mm-wiki.git
$ cd mm-wiki
$ go build ./
```

## 反馈
- 官方 QQ 交流群：853467682
- 如果您喜欢该项目，请 [Star](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304631cc7f57c0392403f1cb6f347b60d448b70ba5d5fe60f6b31c21ea4fa9ed59d2 
- 如果在使用过程中有任何问题， 请提交 [Issue](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304631cc7f57c0392403f1cb6f347b60d44830620997ba480c6aa3c8a1663e893916 
- 如果您发现并解决了bug，请提交 [Pull Request](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304631cc7f57c0392403f1cb6f347b60d4488b97942729d82aae6a330064fcfdc87b 
- 如果您想二次开发，欢迎 [Fork](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304631cc7f57c0392403f1cb6f347b60d4480cddf66ce0007dc67dfa808750580270ebd727272081bbd2dbd3d4e360ad85ad 
- 如果你想交个朋友，欢迎发邮件给 [phachon@163.com](mailto:phachon@163.com).

## License

MIT

谢谢
---
Create By phachon



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)