
## Neditor富文本编辑器介绍

Neditor 是我们团队基于 Ueditor 的一款富文本编辑器。
不论从功能还是从其它各方面来讲， Ueditor 都是一款无以替代的编辑器产品。
只是已经不符合现代化样式的需求，于是我们修改它的样式，实现了这样的效果：

![image](https://www.notadd.com/src/neditor.webp)

Demo:  https://neditor.notadd.com/demo/

## 入门部署和体验 ##

### 第一步：下载编辑器 ###

下载 Neditor 最新版

或从源码编译：

```shell
git clone 仓库地址
npm install
grunt notadd
```

### 第二步：创建 demo 文件 ###

解压下载的包，在解压后的目录创建 demo.html 文件，填入下面的 html 代码

```html
 
 
 
	 
	 ueditor demo 
 
 
	 
	 这里写你的初始化内容 
	 
	  
	 
	  
	 
	 
	    var ue = UE.getEditor('container');
	 
 
 
```

### 第三步：在浏览器打开demo.html ###

如果看到了下面这样的编辑器，恭喜你，初次部署成功！

![部署成功](https://www.notadd.com/src/neditor-demo.webp)

### 自定义的参数

编辑器有很多可自定义的参数项，在实例化的时候可以传入给编辑器：

```javascript
var ue = UE.getEditor('container', {
    autoHeight: false
});
```

配置项也可以通过 neditor.config.js 文件修改，具体的配置方法请看[前端配置项说明](http://u.720life.cn/g/2ec7fed527cfc306d0ab68523b3da8a60bb3ee1a45112db8c2c507e61644b4486269aab195cfaaa4ba7f65412661294c  前端配置项说明.md)

### 设置和读取编辑器的内容

通 getContent 和 setContent 方法可以设置和读取编辑器的内容

```javascript
var ue = UE.getContent();
ue.ready(function(){
    //设置编辑器的内容
    ue.setContent('hello');
    //获取html内容，返回:  hello 
    var html = ue.getContent();
    //获取纯文本内容，返回: hello
    var txt = ue.getContentTxt();
});
```

Ueditor 的更多API请看[API 文档](http://u.720life.cn/g/42a1ca100b4595a59a3d89218edc843246c238d2c19eef2617b5924ddf6ba608  "ueditor API 文档")

## 相关链接 ##

Ueditor 官网：[http://ueditor.baidu.com](http://u.720life.cn/g/42a1ca100b4595a59a3d89218edc84320a352e4d2bd2df1f21f1e3184aa659ee  "ueditor 官网")

Ueditor API 文档：[http://ueditor.baidu.com/doc](http://u.720life.cn/g/42a1ca100b4595a59a3d89218edc843246c238d2c19eef2617b5924ddf6ba608  "ueditor API 文档")

Ueditor github 地址：[http://github.com/fex-team/ueditor](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d35b5f628f8cf0586607d6feaa54f8760f2d349a02ee4c5694e8b2d5e31f83afea  "ueditor github 地址")

Neditor github 地址：[http://github.com/notadd/neditor](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d35b5f628f8cf0586607d6feaa54f8760f2d349a02ee4c5694e8b2d5e31f83afea  "Neditor github 地址")

## 详细文档

Ueditor 文档：[http://fex.baidu.com/ueditor/](http://u.720life.cn/g/2ec7fed527cfc306d0ab68523b3da8a69027d3003dd3c350ab9216c8c140cdd2) 

注: 对IE8以下版本不再承诺兼容

## 联系我们 ##

QQ 群： 321735506
issue：[github issue](http://u.720life.cn/g/f6754e90a70fcffec3c12b5e1e01b2d3b9a88bd3eef99da5d13ddbdaf7c54dbe8228a245e7b3ac3c2a94259549b59527  "ueditor 论坛")

## 捐赠 


[捐赠](http://u.720life.cn/g/3e7e8f170da15d1979f4c6b1321cc36b6eae409087c1ebfca4fdbe98f2f164b62b72aec577e14f505d3e4bda0214159fe9aed004dd6548244d0b1bc9a1387070) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)