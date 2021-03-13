#LunarCalendar

基于 [electron](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046f6da0bb0f1fa96ca7a8b814036349af2)  + [menubar](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304660eb41948b54229ad605944fad3cee6bf30d62d7ff0b5898dd8c4e4f11d14337)  + [react](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046405e3357754798ba3fdb28fb956ae71f3f95f97337fa9f7933c903f0b8a28f5b)  + [materialize](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dfc066dda7e6721d980cc8ed418dad645665fba06de63e3cf1437622d2bbeea8)  
构建的`工具栏日历应用`，适用于Mac，Windows，Linux平台。


日历数据由 [LunarCalendar](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304664b60fcdcdb3a78a4b96e113cc9eb480015ea5db580102656f5289559b270c0d)  提供。


======

**MAC 版下载链接** [LunarCalendar.app](http://u.720life.cn/g/a109a0615ed740cf52cdd9f7a4793a41a3725700fefdedfe4d3409a6b826c317)  

======

![lc](http://i1.tietuku.com/6cc696c379811560.gif)

## 开发和构建

依赖于node.js环境，请预先安装。

可直接在浏览器中打开`index.html`进行预览测试，但注意jQuery的引用问题。

```
git clone https://git.oschina.net/sinceow/LunarCalendar.git

cd LunarCalendar
```

> 第一步，安装Node.js依赖和利用Bower下载前端依赖

```
npm install
```

> 第二步，利用Gulp构建项目并 Watch SASS 和 JS

```
npm start
```

进行本地测试（可选）

```
npm run-script electron
```

> 第三步，生成APP

```
#生成osx状态栏日历
npm run-script build

#生成win32菜单栏日历
npm run-script build-win
```


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)