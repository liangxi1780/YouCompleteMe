FairyGUI Cocos2dx SDK
====

A flexible UI framework for Cocos2dx, working with the FREE professional Game UI Editor: FairyGUI Editor.  
Download the editor from here: [www.fairygui.com](http://u.720life.cn/g/44c65aac00e8c6dbf3384411eaed98c5ed9ca5bdb43b721c6ca474c50a061c8d)   

FairyGUI编辑器操作简单，使用习惯与Adobe系列软件保持一致，策划和美术设计师可以轻松上手。在编辑器即可组合各种复杂UI组件，以及为UI设计动画效果，无需编写任何代码。可一键导出到Unity，Cocos2dx, Starling, Egret, LayaAir, Pixi, Haxe, Flash等多个主流应用和游戏平台。

下载UI编辑器：[www.fairygui.com](http://u.720life.cn/g/44c65aac00e8c6dbf3384411eaed98c5ed9ca5bdb43b721c6ca474c50a061c8d) 

Get Started
====

目录结构：
- libfairygui 这里是fairygui库的源码。
- Examples 这里是示例的源码。
  - UIProject 这里是示例用到的UI界面的源码，使用FairyGUI编辑器打开。

请下载3.x版本cocos2dx命名成cocos2d放在Example根目录。cocos2dx源码需要改动一处地方才能通过编译，打开2d/CCLabel.h，大约在672行，为updateBMFontScale函数打上virtual修饰符。即
  ```
    virtual void updateBMFontScale();
  ```
  因为这个方法里有强制字体对象指针为FontFnt类型的代码，但我们不使用FontFnt（FontFnt只支持从外部文件中载入配置，更糟糕的是BMFontConfiguration是定义在cpp里的。）, 所以需要重写这个方法。

Learn
====

[教程](http://u.720life.cn/g/44c65aac00e8c6dbf3384411eaed98c5fcbf29b9c5f3a582befb8d83c4c8c3ff2677daf0a03a7dc5d74783732f3e0723)   

License
====

MIT



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)