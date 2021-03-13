# KeeDiary

日记编辑器，使用 kdbx 作为数据库加密存储你的日记。

> 配合 Syncthing 使用，可以方便的在不同设备同步数据库。

## Screenshots · 截图

![demo](./public/screenshots/01.png)

![demo](./public/screenshots/02.png)

![demo](./public/screenshots/03.png)

![demo](./public/screenshots/04.png)

## TechStack · 技术栈

- Electron
- React (create-react-app、react全家桶，新手学习 React 中，存在诸多性能问题等待后期优化...)
- [kdbxweb](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e905da72032144e030f604da9731945a7a0a08daea4e62db8b986ac455ddb52c)  (用于操作数据库，由于网络问题使用了拷贝的国内源)

## Features · 特性

- [X] 打开数据库（`密码`/`密码+密钥`）
- [X] 浏览群组(groups)和群组里面的条目(entries)
- [X] 保存数据库/关闭数据库
- [X] 使用一个变量判断数据库是否被改动
- [X] 加密存储本地密码
- [X] 全数据库搜索功能
- [X] 实现日历视图
- [X] 支持黑暗模式
- 群组(groups)
    - [X] 重命名群组
    - [X] 移动至回收站（如果关闭了回收站则直接删除群组）
    - [X] 清空回收站
    - [X] 移动群组
    - [X] 新建群组
    - [ ] 列表的展开与收缩
    - [x] 渲染性能优化
- 条目(entries)
    - [X] 标题(Title)和内容(Note)的查看与编辑
    - [X] 创建新条目
    - [X] 删除条目
    - [X] 移动条目
    - [X] 列表性能优化
    - [X] 排序（按创建或修改日期排序）
    - [ ] 搜索/过滤
    - [X] Markdown 支持
    - [X] 修改图标

## Run · 运行

```sh
# 安装依赖
yarn install

# 开发模式 
npm run dev
```

## Build · 构建

```sh
# 全局安装 electron-builder
npm -i -g electron-builder

# 首先构建 React
npm run build:react

# 构建 electron 生成可执行文件
npm run build:electron
```

## 备注

- 如果在开发过程中出现 electron 无法启动的问题，请删除应用缓存：`C:\Users\ \AppData\Roaming\ ` （已查明是 `electron-devtools-installer` 插件的问题，已禁用插件）
- 安装**前端**依赖时请务必安装在 `devDependencies`（`yarn add axios --D`），否则，如果安装在 `dependencies` 会一并打包进发行版，从而增大 electron 体积。

## Reference · 参考

- [Building an Electron application with create-react-app](http://u.720life.cn/g/7f1e0d28f8ce20e4916f5ff7cf1b3151329bd4a5ee5e8898604877a9d6efd306afa8f7b4d002fba91f3e2aa5da0db351b3aeaa27554fb7ce00c873f3d9ec7057f2a10b11f009a728a958aa37ccd8a4ee44ad917608ad7512fca50fc9afe7dac0ad20722b07123384a0e2d48d563e72dd) 
- [Electron.js 快速入坑指南 - Windows 下的打包](http://u.720life.cn/g/0f36e2777f446ac50f1acde31e377aeebfbcbafdff96c4b124e38ce8caf772a1016970b5bc4168a7dd1b706b0cee83c58b5f482c166e24d8713ef83c20712d5802edf41e59f17b37de41981e84a59c8631665a58f07faa4ec576b6a9004e8d6369f983c0568c70a91fcd4976eebc7c59) 
- [KdbxWeb 国内拷贝并修改依赖源](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e461baa48c08ab89cc588c2883fd8fca529bd8aaf20c0d234d89258e474a72be7) 
- [Electron 打包优化 - 从 393MB 到 161MB](http://u.720life.cn/g/fba0353455c429dd640cd74069616601336ba14b6f0aeb912e38a0f69bcb31e7ecf3d1c0a312277ad1e792e09857ab30) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)