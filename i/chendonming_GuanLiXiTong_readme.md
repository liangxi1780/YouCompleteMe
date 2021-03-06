 
     
         
     
 

# iView Admin
[![](https://img.shields.io/travis/iview/iview-admin.svg?style=flat-square)](https://travis-ci.org/iview/iview-admin)
[![vue](https://img.shields.io/badge/vue-2.5.2-brightgreen.svg?style=flat-square)](https://github.com/vuejs/vue)
[![iview ui](https://img.shields.io/badge/iview-2.5.0-brightgreen.svg?style=flat-square)](https://github.com/iview/iview)

## 当前版本：v1.1.4
[更新日志](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464acd1bc69bca9dfde1b71ae150cc182cc0a955cc9601a6818dc0530991e4c9ba) 

[使用教程](http://u.720life.cn/g/54145d0471d91890860f7f8463c030464acd1bc69bca9dfde1b71ae150cc182c91811631dc0440c205016f82959a2114) 

[在线访问](http://u.720life.cn/g/5faed70325ac704b47c4388fcffedc2a3b624b6527ca8ffa90dd4a3c07ba8912c1391086192f2df610e5fdde0330e090) 

`注：在线版本会在开发版本新小版本发布后更新到相应版本，所以如果想体验最新版本iview-admin，请clone完整项目代码到本地运行。`

## Run

```
npm run dev
```

## 简介
&emsp;&emsp;iView admin是基于Vue.js，搭配使用[iView](http://u.720life.cn/g/042b48c1b518af8039860c9df004b13cb855bd704dab6d9eda4b7866cab288c8)  UI组件库形成的一套后台集成解决方案，由TalkingData前端可视化团队部分成员开发维护。iView admin遵守iView设计和开发约定，风格统一，设计考究，并且更多功能在不停开发中。
如果您想查看iview-admin的更新动态，您可以到[更新日志]https://github.com/iview/iview-admin/releases)查看了解最新更新；如果您是新手，想快速入手iview-admin，您可以到[使用教程]https://github.com/iview/iview-admin/wiki)查看讲解；如果您想在线体验iview-admin，您可以到[在线访问]https://iview.github.io/iview-admin)体验。

## 功能

- 登录/登出
- 权限管理
    - 列表过滤
    - 权限切换
- 多语言切换
- 组件
    - 富文本编辑器
    - Markdown编辑器
    - 图片预览编辑
    - 可拖拽列表
    - 文件上传
    - 数字渐变
- 表单编辑
    - 文章发布
    - 工作流
- 表格
    - 可拖拽排序
    - 可编辑表格
        - 行内编辑
        - 单元格编辑
    - 可搜索表格
    - 表格导出数据
        - 导出为Csv文件
        - 导出为Xls文件
    - 表格转图片
- 错误页面
    - 401页面
    - 404页面
    - 500页面
- 高级路由
    - 动态路由
    - 带参页面
- 换肤
- 收缩侧边栏
- tag标签导航
- 面包屑导航
- 全屏/退出全屏
- 锁屏
- 消息中心
- 个人中心

## 文件结构
```shell
.
├── dist
│   ├── langs    TinyMCE富文本编辑器语言包
│   ├── plugins    TinyMCE富文本编辑器组件
│   ├── skins    TinyMCE富文本编辑器皮肤
│   └── themes    TinyMCE富文本编辑器主题
└── src
    ├── config    项目配置
    ├── images    图片文件
    ├── libs    工具方法
    ├── styles    样式文件
    ├── template    ejs模板
    └── views    视图组件
        ├── access    权限管理
        ├── error_page    错误页面
        ├── form    表单
        │   ├── article-publish    文章发布
        │   └── work-flow    工作流
        ├── home    首页
        ├── international    多语言切换
        ├── main_components    主框架
        ├── message    消息中心
        ├── my_components    组件
        │   ├── count-to    数字渐变
        │   ├── draggable-list    可拖拽列表
        │   ├── file-upload    文件上传
        |   ├── image-editor    图片预览编辑
        │   ├── markdown-editor    markdown编辑器
        │   └── text-editer    富文本编辑器
        ├── own-space    个人中心
        ├── screen-shorts    锁屏
        └── tables    表格
```

## Links

- [TalkingData](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a6b05f598c3817e53335135bafff79d6) 
- [iView](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c77dfb115f76a8da39c86e27313b7fe5) 
- [Vue](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a66c77cd0911e5527fb3fc591bfc25f5) 
- [Webpack](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467fcc54064697beb3b7b3df6e06eef298df4c1c58c8a6fda9268979495e98dbb2) 

## 效果展示

- 登录
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/home.gif)

- 标签导航
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/page-tags.gif)

- 权限管理
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/access.gif)

- 可拖拽列表
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/dragable-list.gif)

- 图片预览编辑
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/image-editor.gif)

- 文件上传
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/upload.gif)

- 数字渐变
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/count-to.gif)

- 文章发布
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/article-publish.gif)

- 工作流
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/workflow.gif)

- 可拖拽表格
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/dragable-table.gif)

- 可编辑表格
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/editable-table.gif)

- 表格导出数据
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/exportable-table.gif)

- 表格转图片
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/table2image.gif)

- 错误页面
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/error-page.gif)

- 锁屏
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/locking.gif)

- 可收缩侧边栏
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/sidebarmenu.gif)s

- 主题切换
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/theme.gif)

- 消息中心
![image](https://github.com/iview/iview-admin/raw/dev/github-gif/message.gif)

## License
[MIT](http://u.720life.cn/g/ba059582536a397f7c573b87c8bea647045b0ef049248233b6f76e909e70200fe7048b25e29c8bab79aeff32ea74556a) 

Copyright (c) 2016-present, iView



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)