 
 
 
 链滴笔记，连接点滴 
  
   
   
   
 
   
   
   
 
   
   
   
   
  
     
     
     
   
 

## 💡 简介

链滴笔记是一款开源的桌面端笔记应用，支持 Windows、Mac 和 Linux。

### ✨  特性

* 为 Markdown 而生
  * 支持传统的分屏编辑预览模式
  * 支持类似 Typora 保留标记符的实时渲染模式 `TBD`
  * 支持所见即所得编辑模式
  * 支持数学公式、图表、流程图、甘特图、时序图、五线谱等
  * Markdown 文本格式化
  * 粘贴 HTML 自动转换为 Markdown
  * 配置 Markdown 解析渲染细节参数
    * 是否启用脚注支持 `TBD`
    * 是否启用 [ToC] 支持 `TBD`
    * 是否需要中西文间自动插入空格
    * 是否进行自动术语修正
    * 中文后跟英文逗号句号等标点是否自动替换为中文对应标点
    * 内联数学公式是否允许起始 $ 后紧跟数字
    * 数学公式引擎切换 MathJax、Ketax
* WebDAV 挂载远程目录
* Double Shift 快速导航
* 全文搜索
* 明亮、暗黑两套主题
* 标签聚合分类 `TBD`
* 导出静态站点，内置多套主题 `TBD`

## 📸 截图

### 明亮主题

![white](https://user-images.githubusercontent.com/873584/74507339-11e16080-4f37-11ea-8700-e9d4ebfa9787.png)

### 暗黑主题

![dark](https://user-images.githubusercontent.com/873584/74507336-0ee67000-4f37-11ea-827c-903644d0de3e.png)

### Markdown 配置

![dark-md](https://user-images.githubusercontent.com/873584/74507501-89af8b00-4f37-11ea-9de2-534aed8c2c78.png)

### 全文搜索

![dark-search](https://user-images.githubusercontent.com/873584/74507506-8c11e500-4f37-11ea-9ff2-b1c41b3be225.png)

## 🛠️ 安装

### 安装包

* [GitHub](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c3ab5c72fd8c57594492780fb19f56f8085d50d14230c726309a596c54a260d6) 
* [码云](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e6ebc2ff18419affa556a161fbde56ef16af8f1b2ce9127ae75a4fe92ca097c12) 
* [本地下载](http://u.720life.cn/g/f42fc0f28ccdb0c82199f675736ecd49872c0e4ea350016adb18960c9594795c91a16c4c4450c676ba3ee10718f29f08) 

#### 源码构建

1. 安装 Go、Node 环境
2. 运行项目根目录下的 build 脚本 
3. 构建成功后将在 app/build 下生成安装包

如果你要修改源码，请按如下步骤搭建开发环境：

1. 在 kernel 目录下构建内核并启动
   * Windows：`go build -o kernel.exe && kernel.exe`
   * Mac：`go build -o kernel-darwin && ./kernel-darwin`
   * Linux：`go build -o kernel-linux && ./kernel-linux`
2. 在 app 目录下构建前端 `npm run dev` 并启动主进程 `npm run start`

## 🏗️ 技术架构

![链滴笔记架构图](https://user-images.githubusercontent.com/873584/73417483-2e847280-4353-11ea-9e4c-2594c4b08b35.png)

* 通过 Electron 实现主进程，启动后拉起 golang 实现的内核进程
* 内核实现 WebSocket 服务端和主进程交互
* 内核实现 WebDAV 服务端和客户端
* 文件存取（包括操作本地文件）通过 WebDAV 客户端进行
* Markdown 文件启动和挂载时加载到内存实现全文搜索
* 通过 Vditor 编辑器实现 Markdown 所见即所得编辑模式

## 📜 文档

* [链滴笔记路线图](http://u.720life.cn/g/a403b9f09ec47bda0547a75d1a5e3d409b4b9d1c6d92669ef6751925bb6df2282c95e5aa96d48865a9467e36de76650f) 

## 🏘️ 社区

* [讨论区](http://u.720life.cn/g/a403b9f09ec47bda0547a75d1a5e3d40867640c2dc4da7618827d256a874e1aff4f1f41cd24c1e383aad487180b971cc) 
* [报告问题](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c3ab5c72fd8c57594492780fb19f56f8a1a907a725d00e3826b1dbd450d9bcf6) 
* 欢迎关注 B3log 开源社区微信公众号 `B3log开源`  
  ![image-d3c00d78](https://user-images.githubusercontent.com/873584/71566370-0d312c00-2af2-11ea-8ea1-0d45d6f0db20.png)

## 📄 开源协议

链滴笔记使用 [木兰宽松许可证, 第2版](http://u.720life.cn/g/cc97cb0a89a2ec0d6b5fc2a79fc140e236037bd68a8e84069e0ae672e6c5b30f0956e4030f132effb1379e8e760edfee)  开源协议。

## 🙏 鸣谢

* [浏览器端的编辑器 Vditor](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461f6ddebc7a4d57f724433079f0c3c5483d51d1b4e62a3b9ed24620bd297a0626) 
* [对中文语境优化的 Markdown 引擎 Lute](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046913830df16b8eb8db2e55598a932fb48) 
* [Go WebDAV 客户端库](http://u.720life.cn/g/54145d0471d91890860f7f8463c030469bbe5af589545220d956d823ee31c0c52a542f942addec2fa2cbcdbaba2c84a4) 
* [Go 常用工具库](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bcb951b36da6e2db1b610bbcf849ee6c) 
* [Go Web 框架 Gin](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046a58e44c7b16b1ea7d34670c8c0a23cb0) 
* [Go WebSocket 框架 melody](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046aa91a40ba78e4481cc7b82a2750ab919) 
* [跨平台桌面应用框架 Electron](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304637d42c0ea91f92b54e3d94e70c57cf620dadfce8cd32b190196c88b023b5e62a) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)