# PureLoveForTypecho简介

### 演变历程

- `PureLoveForTypecho`前身是`Purelove` (`Wrodpress`主题)
- `Purelove`是梦月酱设计的[`Wrodpress`]https://cn.wordpress.org/)主题, 页面设计简洁美观 完美支持移动设备端, 支持响应式, 兼容主流游览器
- 而本主题是在[`PureLove主题梓喵出没修改版`]https://www.azimiao.com/purelovethemes)基础上再次改版, 并从`Wrodpress`移植到`typecho`上

### Demo

- [演试地址:www.hoehub.com](http://u.720life.cn/g/08ef222d902b94a4eaba9d0f7850c882f2115beed1b5d0f7593374d4750d6791) 
- [主题源码](http://u.720life.cn/g/2e71d0f0a5c601172267ba20d3a43c6e9ff63eb9bdef25534dd94069530dc705614279fcbd8a20ebfa6c61967daf3be5) 

### Description

- 仿全站`Pjax` (除评论提交外)
- 自定义首页轮播图/侧边栏显示/Logo等
- 代码高亮显示
- 评论区显示系统及浏览器信息 博主标识
- 新增归档页面
- 自动获取文章第一张图片做为缩略图, 如文章无图, 则随机显示8张来自[站酷 (ZCOOL)]http://www.zcool.com.cn)的缩略图
- 设备小于`860px`时, 侧边栏和页脚会隐藏
- 页脚调用金山每日一句接口

### Use

- `git clone https://gitee.com/HoeXhe/PureLoveForTypecho.git`
- 将主题放入`/usr/themes/`目录下
- 登录控制台使用和配置外观即可

### Link

- 主题作者梦月酱
- [梦月酱`PureLove`主题原版](http://u.720life.cn/g/774653b2babb329eb5ca9f4f9b9068549dfdc342a0588d01e7211577678d3b23dfd91c591c56e4d677dc1a5cb22ed12d) 
- [`PureLove`主题梓喵出没修改版](http://u.720life.cn/g/e5ed8d90ff7e1d530aa1f7f7256aeab2bd87d1e64cedd3d64b84201504b3b5f2845be8d8443e311a5e46e9dc4f49c040) 

### Thanks

- 梦月酱
- [野兔](http://u.720life.cn/g/e5ed8d90ff7e1d530aa1f7f7256aeab23fe3b629da02661c7fa7eddf7b28c851) 
- [熊猫小A](http://u.720life.cn/g/bf7112091e317c361feddaeac53f6c2e9770cd890cd59621762364e0d22e350f) 
- [typecho社区](http://u.720life.cn/g/2415ee134da147687c1775d970988587934e6ae3469fbc5772300f92f8a9dd70) 

### Defect

- 小尺寸设备时菜单会被截取而不是缩放
- 如使用`Pjax`提交评论后, 当前URL会有后缀`/comment` 如按`F5`刷新页面会报错
- 如使用`Pjax`提交评论后, 无法再次提交评论

### 类库 [使用BootCDN加速](http://u.720life.cn/g/9092c149b63e18c595e68392f967b833bbf8029c1d72e3476f5655d1fb526f1c) 

- `jquery.js` v1.12.2
- `jquery.pjax.js` v2.0.1
- 字体图标 `font-awesome.css` v4.7.0
- 代码高亮 `highlight.js`使用`vs`样式 v9.13.1
- 进度条 `nprogress.js` v0.2.0
- 幻灯片 `responsiveslides.js` v1.55
- 输入动画库 `typed.js` v2.0.9
- 评论表情库 `emojionearea` v3.4.1

### 参与贡献

1. Fork 本项目
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request

### 许可证 License

- 本项目遵循GPL-3.0开源协议发布。
- 版权所有Copyright © 2018 by Hoe (http://u.720life.cn/g/08ef222d902b94a4eaba9d0f7850c882f2115beed1b5d0f7593374d4750d6791) 
- All rights reserved。

### 日志

- 2019-12-20 1.取消默认项，统一在后台设置外观里配置 2.优化菜单 3.主题取消[疯狂打字机]https://www.hoehub.com/PHP/typecho-ActivatePowerMode.html)效果

- 2018-12-26 改版归档页面

- 2018-12-09 侧边栏&底部响应式显示

- 2018-12-07 评论头像如果没有定义__TYPECHO_GRAVATAR_PREFIX__, 默认使用V2EX服务器

- 2018-12-02 重置文章内容页 ul ol 样式

- 2018-12-02 防止html标签意外闭合而导致的页面布局混乱	

- 2018-11-30 解决按tab键 无法定位到评论框	

- 2018-11-29 修复文章列表标题超长	

- 2018-11-29 感谢只留下用户名的:jiffei反馈问题	

- 2018-11-26 侧边栏最近回复不显示博主评论	

- 2018-11-25 菜单&文章部分字体调整14px	

- 2018-11-22 评论表情emojionearea库

- 2018-11-23 最新回复做成图片墙

- 2018-11-20 调取金山每日一句

- 2018-11-21 评论暂时不使用Pjax
- ...

### 演示图

- 首页

    ![首页图片](demo/index.jpg)
    
- 时间轴(归档)页
    
    ![时间轴(归档)页](demo/timeline.jpg)
    
- 文章页

    ![首页图片](demo/article.jpg)


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)