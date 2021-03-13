# Milog

一基于 [ Ruby on Rails ](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460c1c84ea4619c49d836ca25f762f26e2)  的个人博客网站. http://milog.jimcheung.me

游客账号： Email aguest@milog.com | Password 123456

静态页面： https://github.com/jinhucheung.me/milog/tree/static_pages

## 特点

+ 支持 [Bootstrap](http://u.720life.cn/g/e23be2821e5181a1a46a005bc6e93d9dc1c8dad0ef41593aa593e12a30fc455b)  ，实现响应式设计

+ 使用 [Markdown](http://u.720life.cn/g/fa1db2c4a526903522dec7b8417f89d18b454c7037b63461cb52a9b26673afcc50ef3ed418a4155a4b925211014445c8)  作为编辑文本格式，主要由 [Markdown-it](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466f51b09e9373ecce8f8382afb59f6645fdb861fc7761795e811d865ea718502f)  在客户端进行解析渲染， [motion-markdown-it](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460133385d087e8b1382937b8b948098167d8b5f4d67a54f6f190876e3f20bbbf0bb4e81dd799753f74c055b40098dd9ec)  负责后端解析

+ Markdown 支持 [Emoji](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c8612e00c4c415c31061b76e2015ce787d94744f3d91cde86fd6b1c476d35ff3) 

+ 实现 Markdown 工具栏

+ 使用 [bcrypt](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e38d8dae95915ebe7cf33b549cd654e7b2120c01c031c1846420b254a4ebe632)  加密用户重要资料

+ 可暂存用户编辑中的文本

+ [Elasticsearch](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e836c5dd85610d86e6f01486f462e2c0d9e4b426066af1ff2b4626bce8b1132)  作为全文搜索引擎，可根据关键字搜索文章

+ 支持上传图片，使用[七牛]http://www.qiniu.com/)存储

## 更新

### 2016/12/20

+ 增加社区模块

+ 修改用户主页，增加用户关注功能

+ 增加消息通知系统

### 2017/1/30

+ 使用 [Letter Avatar](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c331242f50b6e25b1cd745a921ccbedab8489e92d5f5bfe16e1b3452576abd71)  ，代替原本的用户默认头像模块

+ 使用 [Rails Settings Cached](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469304bfea73c47a26861353dae973fe5ddad397637841d932ac9b66b6e6fed317e762a972cd87c066f1d7e1f001d898e8)  保存系统设置

### 2017/3/14

+ 实现 Milog Android 客户端 [Milog-Android](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046fdbf6f0e6c6d1d29c3142ca6f4034bb1707094118286183b12a4546cf6453661) 

+ 修复文章中图片尺寸过大，溢出页面

### 2017/5/7

+ 将原先的 `afeld.github.io/emoji-css` 文件导入本地

+ 修复客户端用户未登录访问消息通知 404

### 2017/5/15

+ 后台添加用户后发送密码激活邮件至用户邮箱

+ 修复测试用例

## Thanks

+ [Ruby on Rails](http://u.720life.cn/g/7c10e84df7ff3d1064713a214537671e55235468e6d4c549d415679e07614da4) 

+ [Ruby China](http://u.720life.cn/g/ba56fb5c32247fb156ba816bc612ca17e553e0f5a8ea44b583a0cff0c7e6bba5) 

+ [Hexo-theme-next](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046072e7aa8a003b6d5f3aa964707a979561736ed848a7f9ee864b20e0ae1dd5729) 

+ [Bootstrap](http://u.720life.cn/g/e23be2821e5181a1a46a005bc6e93d9dc1c8dad0ef41593aa593e12a30fc455b) 

+ [Markdown-it](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466f51b09e9373ecce8f8382afb59f6645fdb861fc7761795e811d865ea718502f) 

+ [Elasticsearch](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466e836c5dd85610d86e6f01486f462e2c0d9e4b426066af1ff2b4626bce8b1132) 

## 部署

### 环境
```
Ubuntu 14.04 / Git / Ruby 2.3.1 / Rails 5.0.0 / MariaDB 5.5.52
```

### 下载
```
git clone git@github.com:Hikumho/milog.git
```

### 数据库

安装 [MariaDB](http://u.720life.cn/g/af80db58447e659546f823f2a34ed82fda324f7752e6236036060ac9c6a191e9) 

```sh
sudo apt-get install software-properties-common
sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xcbcb082a1bb943db
sudo add-apt-repository 'deb http://sfo1.mirrors.digitalocean.com/mariadb/repo/10.0/ubuntu trusty main'

sudo apt-get update
sudo apt-get install mariadb-server
```

### 项目配置

1. 更新配置文件

```
cp config/local_env.yml.example config/local_env.yml
cp config/email.yml.example config/email.yml
```

修改 `config/local_env.yml` 中的 `MYSQL` 信息

2. 安装 Gem

```
bundle install
```

其他问题可见 [#FQA](#FQA)

3. 迁移数据

```
rails db:create

rails db:migrate

rails db:seed
```

至此， 项目可在开发环境中运行

以下进行生产环境的部署

1. 生成 App 密钥

```
require 'secretrandom'

SecureRandom.hex(64)
```
并将密钥写入 `config/secrets.yml` 的 `production` 节点


2. 部署七牛云

修改 `config/local_env.yml` 中的 `QINIU` 信息

具体配置请看 [carrierwave-qiniu](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304644b86fa943dedacf88abe10cda7559d426907a71b4ecf9c04360621f1e880dea) 

3. 部署邮件

修改 `config/email.yml`

### FQA

1. Imagemagick

本地可能由于没有安装  [Imagemagick](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466402ebc59f2ae29b3377f3316690029326448630f705feb772aa763971f02d4b)  导致 `bundle install` 出错

安装 Imagemagick： `sudo apt-get install imagemagick`

2. Elasticsearch

安装 Elasticsearch： [教程](http://u.720life.cn/g/93e30238e47de776c7e058ce98b95c6bebe0821448beb652bb83e5950d792d81cfedcf296a456463f78ed82c71a42aba27f03b20607a0af4ebca1d76ef50f97a51ef4907ca4d543a419228af67c12eb9da627b1502feabb00c32288c786d6176) 

配置 Elasticsearch： `bundle exec rake environment elasticsearch:import:model CLASS='Article' SCOPE='posted'`


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)