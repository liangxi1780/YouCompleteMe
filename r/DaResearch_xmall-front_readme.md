## XMall-Front
### 基于Vue开发的XMall商城前台页面
### 项目已部署，在线Demo
- 前台商城：http://xmall.exrick.cn/
- 后台管理系统：http://xmadmin.exrick.cn/
- 第一次打开可能较慢，请耐心等待
### 感谢 [yucccc](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cd7017a4f1aa1f7d34b7a3c3cee04ce4)  的开源 [vue-mall](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046972527ba0da1295bf647a094e05ea6bd1e24e4d1f8ba19c2f56965bef13b40ec)  项目提供前端页面及框架支持
### 后端全部重新开发接口，实现后台系统管理，后端接口项目请跳转至 [xmall](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304632c7085a3fcc4563a9dbc223763a621d)  项目仓库查看
### 新增与优化
- 优化页脚、增加商品搜索框组件
- 优化登录注册界面
- 新增搜索页面，实现高亮分页搜索
- 新增捐赠页面，捐赠列表显示
- 全部商品页面实现分页
- 优化订单详情，实现查看订单进度，可对订单进行处理
- 实现生成订单接口、优化地址管理编辑选择
    
![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022183906.jpg "首页")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022222841.jpg "页脚")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022223650.jpg "搜索框组件")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171109215656.jpg "搜索结果")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022202842.jpg "无搜索结果")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022223142.jpg "分页")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022190036.jpg "订单详情")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171022190107.jpg "订单进度")

![](http://oweupqzdv.bkt.clouddn.com/QQ%E6%88%AA%E5%9B%BE20171114233321.jpg "登录界面")
    
### 所用技术

- Vue 2.x
- Vuex
- Vue Router
- [Element UI](http://u.720life.cn/g/b283854352f752627fc107baa2884ffda573d5c3dcc96962ff60326357ba94ee) 
- ES6
- webpack
- axios
- Node.js
- 第三方SDK
    - [极验Test-button人机验证码](http://u.720life.cn/g/af1e222ff94b66580ad482e7c89c63f91645bbf5d51ed1f9acc1543666ad2a900dcb96a46c593fa1254958318280eaec) 
- 第三方插件
    - [hotjar]https://github.com/Exrick/xmall/blob/master/study/hotjar.md)：一体化分析和反馈
    - [搜狐畅言评论插件](http://u.720life.cn/g/fb2586c4ecb6075c88b852d82c275a2f765488c6bebaee1c88d0054ab37d3070) 

### 本地开发运行部署
- 启动后端 [xmall](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304632c7085a3fcc4563a9dbc223763a621d)  项目后，在 `config/index.js` 中修改你的后端接口地址配置
- 在 `src/api/goods.js` 中的 `getQuickSearch` 方法里修改你的Elasticseach服务器IP以及RESTful快速查询提示接口配置
- `index.html` 中复制粘贴替换你的 [hotjar](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046621f393e65c5d1a83526fbee5e95f767b84b880ad658a76463126efd4ccd71f2e67d29ba82c26b1b68f2695835aa35f4)  代码
- 若不启动后端项目，预览运行此前端项目可注释掉 `src/main.js` 中第 `8、10、21-43` 行代码即可
- 在项目根文件夹下先后执行命令 `npm install` 、 `npm run dev`
- 商城前台端口默认9999 http://localhost:9999
### 技术疑问交流
- 给作者项目Star或捐赠后可加入交流群 `475743731`，还可免费获取最新源码和 [UI框架](https://github.com/Exrick/xmall/blob/master/study/FlatLab.md) [![](http://pub.idqqimg.com/wpa/images/group.png)](http://shang.qq.com/wpa/qunwpa?idkey=7b60cec12ba93ebed7568b0a63f22e6e034c0d1df33125ac43ed753342ec6ce7)
- 个人博客：[http://blog.exrick.cn](http://u.720life.cn/g/d9facb80ece1075627c5e84d9677b2c19a52006991cae3006c3cacccaf404d77) 
### 捐赠
![](http://oweupqzdv.bkt.clouddn.com/FgwHSk1Rnd-8FKqNJhFSSdcq2QVB.png)


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)