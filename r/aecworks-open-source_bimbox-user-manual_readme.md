# BIMBox产品帮助中心

本项目采用[mkdocs])(http://u.720life.cn/g/38ce4248d7a698d73680384f00d7569db304f1ad3a1380a0a9c1ab1f1b7bf6b7eb2374c7cc111a699b952cac9f83a2de792e9e9d845007840e71c10d1ccfe397586d25e84eb4ed90ccc0329e0bd9e2b78d3eac182f68fb4b4017575e41bdad28 
一般步骤如下

* 安装[python 3](http://u.720life.cn/g/74e7b7c595201f48e3f4da7562c1a8265391d71b10b58cef78feb3ff65d1b8965569845551cfcd960ecd02eb394b3b42  最新版即可，安装时一定要选择将 python 加入到环境变量 `PATH` 中。
* 安装 `mkdocs`，打开一个新的 cmd 窗口，运行 `pip install mkdocs` 即可。 `pip`一个 python 的包管理工具，跟pyton3一起安装。

安装和发布时，需要进入到 `help` 目录运行以下命令 

* 编辑文档并实时看到效果：`mkdocs serve -a localhost:8200`, 访问`http://localhost:8200` 即可。
* 打包发布：`mkdocs build --clean --strict`

## 常见问题

### Linux系统上 gulp watch 的 ENOSPC error

* 解决方案：https://stackoverflow.com/questions/16748737/grunt-watch-error-waiting-fatal-error-watch-enospc
* 运行命令： `echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p`

## mkdocs 快速入门

### markdown 的语法

* 基本语法：https://www.jianshu.com/p/b03a8d7b1719

### 如何新增导航页面

以添加“关于”页面`docs/about.md`为例

* 在`docs`目录中创建新的Markdown文件:
	* 使用命令： `mkdocs new docs/about`

* 在`mkdocs.yml`中为一个导航增加页面：

>```
pages:
  - 关于: about/docs/index.md
>```

### 如何新增支持二级菜单的导航页面

* 以本项目中的“管理员指南”导航页面`docs/admin.md`为例

* 添加第一个二级导航菜单“组织管理员”页面：

* 使用命令：`mkdocs new docs/admin/docs/organization`

* 添加第二个二级导航菜单“项目管理员”页面：

* 使用命令：`mkdocs new docs/admin/docs/items`

* 在`mkdocs.yml`中为一个导航页面增加二级导航

>```
nav:
   - 管理员指南: 
    '组织管理员' : 'admin/docs/organization/docs/index.md'
    '项目管理员' : 'admin/docs/items/docs/index.md'
>```

### 图片的路径

* 在“关于”页面`docs/about.md`添加`images`

* 使用命令：`mkdocs new docs/about/docs/images`

	>图片存放在`docs/about/docs/images`即可，使用时引入相对路径

### 编辑工具
* [Haroopad](http://u.720life.cn/g/00b1a9b8311222833e5e2496d515d7f06286637d8b29fe7720e4f481988e4ad769190b9cfcd2cdb9ed913009797b8827) 





 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)